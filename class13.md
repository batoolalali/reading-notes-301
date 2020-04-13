# Sending form data

The form data has been validated on the client-side, so it is okay to submit the form.

### what happens to the data when a form is submitted??

- Client/server architecture
1. a client sends a request to a server using the HTTP protocol.
2. The server answers the request using the same protocol.

HTML form on a web page is nothing more than a convenient user-friendly way to configure an HTTP request to send data to a server. This enables the user to provide information to be delivered in the HTTP request.


##### On the client side: defining how to send the data
The `<form>` element defines how the data will be sent.
its attributes are designed to let you configure the request to be sent when a user hits a submit button.

- The action attribute:
1. **The action attribute** defines where the data gets sent. Its value must be a valid relative or absolute URL.
2. **The method attribute** defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods.

    - The GET method: used by the browser to ask the server to send back a given resource, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL.
    - The POST method: the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request. If a form is sent using this method, the data is appended to the body of the HTTP request.

##### Viewing HTTP requests
The only thing displayed to the user is the URL called. As we mentioned above, with a GET request the user will see the data in their URL bar, but with a POST request they won't. This can be very important for two reasons:

1. If you need to send a password (or any other sensitive piece of data), never use the GET method or you risk displaying it in the URL bar, which would be very insecure.

2. If you need to send a large amount of data, the POST method is preferred because some browsers limit the sizes of URLs. In addition, many servers limit the length of URLs they accept.


##### On the server side: retrieving the data
The server receives a string that will be parsed in order to get the data as a list of key/value pairs. The way you access this list depends on the development platform you use and on any specific frameworks you may be using with it.


 sending form data is easy, but securing an application can be tricky. Just remember that a front-end developer is not the one who should define the security model of the data.It's possible to perform client-side form validation, but the server can't trust this validation because it has no way to truly know what has really happened on the client-side.

If you've worked your way through these tutorials in order, you now know how to markup and style a form, do client-side validation, and have some idea about submitting a form.