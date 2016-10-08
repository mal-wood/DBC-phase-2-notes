**COOKIES VS SESSIONS**

COOKIES are stored in a user's browser and contain key/value pairs that hold a variety of info //
everytime an HTTP request is made, those cookies are passed from the browser, to the server, and
back to the browser so that they *persist* throughout a user's experience.

SESSIONS are stored on the server and their ID is passed in a cookie. Sessions are more secure than cookies because the
data they contain cannot be viewed or edited by the client. They can store much more than cookies and dave bandwidth - since only
the ID is passed from the client (not all of the bits of info like in a cookie).

Best example that I found on Stack Overflow to describe this relationship: 

>A cookie is simply a short text string that is sent back and forth between the client and the server.
You could store name=bob&password=asdf in a cookie and send that back and forth to identify the client 
on the server side. You could think of this as carrying on an exchange with a bank teller who has no short 
term memory, and needs you to identify yourself for each and every transaction. Of course using a cookie to 
store this kind information is horrible insecure. Cookies are also limited in size.

>Now, when the bank teller knows about his/her memory problem, He/She can write down your information on
a piece of paper and assign you a short id number. Then, instead of giving your account number and driver's
license for each transaction, you can just say "I'm client 12"

>**Translating that to Web Servers: The server will store the pertinent information in the session object, and
create a session ID which it will send back to the client in a cookie. When the client sends back the cookie,
the server can simply look up the session object using the ID. So, if you delete the cookie, the session will
be lost.**
