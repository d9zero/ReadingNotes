# Class 11 - Introduction to EJS

## Navigation ##
 - [class 01](class-01.md)
 - [class 02](class-02.md)
 - [class 03](class-03.md) 
 - [class 04](class-04.md)
 - [class 05](class-05.md)
 - [class 06](class-06.md)
 - [class 07](class-07.md)
 - [class 08](class-08.md)
 - [class 09](class-09.md) 
 - [class 10](class-10.md)
 - [class 11](class-11.md)
 - [class 12](class-12.md)
 - [class 13](class-13.md)
 - [class 14a](class-14a.md)
 - [class 14b](class-14b.md)

# Reading
[Watch EJS tutorial from WalkThroughCode on YouTube, Videos 1-5](https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt)
Note that this series of videos should take approximately 20 minutes to watch

Additional Resources
Reference: [Google Books API Docs](https://developers.google.com/books/docs/v1/using#WorkingVolumes)
Specifically the section about working with Volumes. Review the sample request and response. Practice making requests using Postman and consider the possible properties of the response that you may want to include in your book application.
Reference: [EJS Docs](http://ejs.co/)

Bookmark/Skim
Skim: [EJS Tutorial](https://scotch.io/tutorials/use-ejs-to-template-your-node-application)
Skim: [Source Code for the EJS Tutorial](https://github.com/scotch-io/node-ejs)
Review the code that goes along with the tutorial

![EJS?](https://www.geeksread.com/wp-content/uploads/2018/06/template-and-Ejsrendering-HTML-and-template.png)

# What is EJS?

EJS is a simple templating language that lets you generate HTML markup with plain JavaScript.

          E in EJS is for Embedded, Ejs is simple and effective template engine for JavaScript. EJS is the simple template which allows developers to create the HTML page with plain JavaScript. Ejs provide fast compilation and rendering and include both server and browser support.

    

# Get Started

Install:

          $ npm install ejs

Use:

        let ejs = require('ejs');
        let people = ['geddy', 'neil', 'alex'];
        let html = ejs.render('<%= people.join(", "); %>', {people: people});

CLI:

          ejs ./template_file.ejs -f data_file.json -o ./output.html

Browser support:

          <script src="ejs.js"></script>
          <script>
            let people = ['geddy', 'neil', 'alex'];
            let html = ejs.render('<%= people.join(", "); %>', {people: people});
          </script>
        
