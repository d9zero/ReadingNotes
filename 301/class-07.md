# Class 07

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

# Readings: Rest

[What Google Learned From Its Quest to Build the Perfect Team](https://www.google.com/amp/mobile.nytimes.com/2016/02/28/magazine/what-google-learned-from-its-quest-to-build-the-perfect-team.amp.html)

![Google](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.hYWi7hgHKaxvhsK7GlLq_wHaFa%26pid%3DApi&f=1)

If you took Code 201, skim this article again for a refresher. If you did not take Code 201, read this article and think about how it can influence the way you work with your partners during pair programming.

[How I explained REST to my brother](https://gist.github.com/brookr/5977550)

![brothers](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.lPUXZm3-o7lPTRboaA2XIQHaE8%26pid%3DApi&f=1)

# Bookmark/Skim
[Documentation for SuperAgent](https://visionmedia.github.io/superagent/)

Functional programming methods:
Map: 
Filter: will take criteria and filter out results in a list.
Reduce (map filter combo)


Get
Post
Put
Delete

Req:
Method
Headers
Body

Res:
Status
Headers
Body

## REST

          "ME: For anything really. That guy, Roy Fielding, he talks a lot about what those things point to in that research I was talking about. The whole world wide web is built on an architectural style called “REST”. REST provides a definition of a “resource”, which is what those things point to.

          Brother: A web page is a resource?

          ME: Kind of. A web page is a “representation” of a resource. Resources are just concepts. URLs--those things that you type into the browser...

          Brother: I know what a URL is.."

# SuperAgent

![hackerman](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse3.mm.bing.net%2Fth%3Fid%3DOIP.vpIaFpGhw2zA-CGe1R9jyAHaEA%26pid%3DApi&f=1)

SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs. It also works with Node.js!

          request
            .post('/api/pet')
            .send({ name: 'Manny', species: 'cat' })
            .set('X-API-Key', 'foobar')
            .set('Accept', 'application/json')
            .then(res => {
                alert('yay got ' + JSON.stringify(res.body));
            });

# Request basics

A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request. For example a simple GET request:

          request
            .get('/search')
            .then(res => {
                // res.body, res.headers, res.status
            })
            .catch(err => {
                // err.message, err.response
            });

# Setting header fields

Setting header fields is simple, invoke .set() with a field name and value:

          request
            .get('/search')
            .set('API-Key', 'foobar')
            .set('Accept', 'application/json')
            .then(callback);

You may also pass an object to set several fields in a single call:

          request
            .get('/search')
            .set({ 'API-Key': 'foobar', Accept: 'application/json' })
            .then(callback);