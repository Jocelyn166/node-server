# node-server
Build a web server with Node JS, no framework used, to build foundational knowledge of Node.js.

1. Use a switch statement to define contentType according to the request URL's extensions.
2. Use conditional (ternary) statements to determine the value of the filePath variable according to contentType.
3. Define an async serveFile function that accepts filePath, contentType, and response as the parameter, inside a try-catch block. Inside try, await fsPromises to readFile and response.writeHead with filePath and contentType, also handles image and JSON file type. Inside the catch, set the response status code to 500, and also emit the logEmitter to create a new file to log out the error.
4. Create a server using http.createServer(), inside the createServer, emit the logEmitter to create a new file to log out the request detail, serve the file using the async serveFile function once the file exists, and serve a 404 page once the file doesn't exist.
