# express-jsend

  Adds jsend() and jerror() to the express.response object.

## Installation

    $ npm install express-jsend

## Usage

    // in your app.js or server.js 
    require('express-jsend')
    
    // then in your route 
    function(res, req, next) {
      res.jsend({...data object...});
      // sends -> {"status": "success", data: {... data object...}} 
    
      res.jerror('InvalidParameter', 'The name field is required.');
      // sends -> {"status": "error", code: "InvalidParameter", message: "The name field is required."}
    
      res.jerror(new Error("My custom error"));
      // sends -> {"status": "error", code: "Error", message: "My custom error"}
    }

## License

(The MIT License)

Copyright (c) 2013 Sean Wesenberg &lt;wookets@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
