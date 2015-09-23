
`earl-express`
==============

Provides the `application` macro, which is used as follows:

```earlgrey
require-macros:
   earl-express -> application
require:
   cookie-parser

application my-app:
   use: cookie-parser
   get "/hello":
      @res.send{"Hello!"}
   post "/something":
      ...

port = 3000
print 'Listening on port {port}!'
my-app.listen{port, .localhost}
```
