# Class 11 - Readings: SENDING FORM DATA

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
 - [class 15](class-15.md)
 - [class 16](class-16.md)
 - [class 17](class-17.md)
 - [class 18](class-18.md)


![javascript forms](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fspeckyboy.com%2Fwp-content%2Fuploads%2F2013%2F08%2Fjquery_form_validation_01.jpg&f=1&nofb=1)


## Reading
[Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)
## Additional Resources
[HTML5 Forms Reference](https://htmlreference.io/forms/)
Pay special attention to the “action” and “method” attributes.
## Videos
[Video Series on Styling HTML5 Forms](https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK)
Note that this video series is approximately 40 minutes long. You do not need to watch every video from the series, but should keep it handy for reference as you style your book app during lab time.


### Sending form data

Objective: 	To understand what happens when form data is submitted, including getting a basic idea of how data is processed on the server

![Architecture](https://media.prod.mdn.mozit.cloud/attachments/2012/11/20/4291/c1a4a06f1fd9ed42ec5b06e814dd3111/client-server.png)

        At it's most basic, the web uses a client/server architecture that can be summarized as follows. a client (usually a web browser) sends a request to a server (most of the time a web server like Apache, Nginx, IIS, Tomcat, etc.), using the HTTP protocol. The server answers the request using the same protocol.

### On the client side: defining how to send the data

The <form> element defines how the data will be sent. All of its attributes are designed to let you configure the request to be sent when a user hits a submit button. The two most important attributes are action and method.

The action attribute defines where the data gets sent. Its value must be a valid relative or absolute URL. If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.

    <form action="https://example.com">

    <form action="/somewhere_else">

The names and values of the non-file form controls are sent to the server as name=value pairs joined with ampersands. The action value should be a file on the server that can handle the incoming data, including ensuring server-side validation. The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page).

### The method attribute

The method attribute defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the GET method and the POST method

### The GET method

The GET method is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to get this resource." In this case, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL.


    <form action="http://www.foo.com" method="GET">
      <div>
        <label for="say">What greeting do you want to say?</label>
        <input name="say" id="say" value="Hi">
      </div>
      <div>
        <label for="to">Who do you want to say it to?</label>
        <input name="to" id="to" value="Mom">
      </div>
      <div>
        <button>Send my greetings</button>
      </div>
    </form>
