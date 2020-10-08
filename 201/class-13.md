# Day Thirteen Notes

# Topic: HTML5 Storage


## Table of Contents

- [Day 1](class-01.md)
- [Day 2](class-02.md)
- [Day 3](class-03.md)
- [Day 4](class-04.md)
- [Day 5](class-05.md)
- [Day 6](class-06.md)
- [Day 7](class-07.md)
- [Day 8](class-08.md)
- [Day 9](class-09.md)
- [Day 10](class-10.md)
- [Day 11](class-11.md)
- [Day 12](class-12.md)
- [Day 13](class-13.md)
- [Day 14](class-14.md), [Day 14 (Extended)](class-14b.md)
- [Day 15](class-15.md)
- [Day 16](class-16.md)
- [Day 17](class-17.md)
- [Day 18](class-18.md)
- [Day 19](class-19.md)
- [Day 20](class-20.md)

# Day Thirteen Reading:

Readings
Below you will find some reading material, code samples, and some additional resources that support today’s topic and the upcoming lecture.

Review the Submission Instructions for guidance on completing and submitting this assignment.

Reading
“The Past, Present, and Future of Local Storage for Web Applications”

# INTRODUCING HTML5 STORAGE


![HTML5](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fwww.codeproject.com%2FKB%2FHTML%2F361428%2Fhtml5.png&f=1&nofb=1)


HTML5 Storage is a specification named Web Storage

Certain browser vendors also refer to it as “Local Storage” or “DOM Storage".

it’s a way for web pages to store named key/value pairs locally, within the client web browser.

this data persists even after you navigate away from the web site, close your browser tab, exit your browser,

this data is never transmitted to the remote web server (unless you go out of your way to send it manually).

it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.

From your JavaScript code, you’ll access HTML5 Storage through the localStorage object on the global window object.

## ↶ check for HTML5 Storage

        function supports_html5_storage() {
          try {
            return 'localStorage' in window && window['localStorage'] !== null;
          } catch (e) {
            return false;
          }
        }


  you can use Modernizr to detect support for HTML5 Storage.

        if (Modernizr.localstorage) {
          // window.localStorage is available!
        } else {
          // no native support for HTML5 storage :(
          // maybe try dojox.storage or a third-party solution
        }

## HTML5 STORAGE IN USE

HTML5 Storage is based on named key/value pairs.

You store data based on a named key, then you can retrieve that data with the same key.

The named key is a string.

The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats.

If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.

        interface Storage {
          getter any getItem(in DOMString key);
          setter creator void setItem(in DOMString key, in any data);
        };

Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

        var foo = localStorage.getItem("bar");
        // ...
        localStorage.setItem("bar", foo);

…could be rewritten to use square bracket syntax instead:

        var foo = localStorage["bar"];
        // ...
        localStorage["bar"] = foo;

There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

        interface Storage {
        deleter void removeItem(in DOMString key);
        void clear();
        };

# TRACKING CHANGES TO THE HTML5 STORAGE AREA

Trapping the storage event works the same as every other event you’ve ever trapped. If you prefer to use jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)

        if (window.addEventListener) {
          window.addEventListener("storage", handle_storage, false);
        } else {
          window.attachEvent("onstorage", handle_storage);
        };

The handle_storage callback function will be called with a StorageEvent object, except in Internet Explorer where the event object is stored in window.event.

        function handle_storage(e) {
          if (!e) { e = window.event; }
        }

# HTML5 STORAGE IN ACTION

        function saveGameState() {
            if (!supportsLocalStorage()) { return false; }
            localStorage["halma.game.in.progress"] = gGameInProgress;
            for (var i = 0; i < kNumPieces; i++) {
          localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
          localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
            }
            localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
            localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
            localStorage["halma.movecount"] = gMoveCount;
            return true;
        }

        function resumeGame() {
            if (!supportsLocalStorage()) { return false; }
            gGameInProgress = (localStorage["halma.game.in.progress"] == "true");
            if (!gGameInProgress) { return false; }
            gPieces = new Array(kNumPieces);
            for (var i = 0; i < kNumPieces; i++) {
          var row = parseInt(localStorage["halma.piece." + i + ".row"]);
          var column = parseInt(localStorage["halma.piece." + i + ".column"]);
          gPieces[i] = new Cell(row, column);
            }
            gNumPieces = kNumPieces;
            gSelectedPieceIndex = parseInt(localStorage["halma.selectedpiece"]);
            gSelectedPieceHasMoved = localStorage["halma.selectedpiecehasmoved"] == "true";
            gMoveCount = parseInt(localStorage["halma.movecount"]);
            drawBoard();
            return true;
        }

        localStorage["halma.game.in.progress"] = gGameInProgress;

        gGameInProgress = (localStorage["halma.game.in.progress"] == "true");

        localStorage["halma.movecount"] = gMoveCount;

        gMoveCount = parseInt(localStorage["halma.movecount"]);

