# restapi-express-mongodb-mongoose
* Integrating the REST API server together with the Mongoose schema and models to create a full-fledged REST API server. 
- Develop a full-fledged REST API server with Express, MongoDB and Mongoose
- Serve up various REST API end points together with interaction with the MongoDB server.
- Scaffold out an Express Application
- Scaffold out an Express application named rest-server using the Express generator at a convenient location on your computer by typing the following at the prompt:

````
     express rest-server
````

- First do an npm install in the rest-server folder to install all the modules. 
- Install mongoose and mongoose-currency Node modules by typing the following at the prompt:

````
     npm install     
     npm install mongoose mongoose-currency --save
````
Open app.js file and add in the code to connect to the MongoDB server as follow:

`````
var mongoose = require('mongoose');
var url = 'mongodb://localhost:27017/conFusion';
mongoose.connect(url);
var db = mongoose.connection;
db.on('error', console.error.bind(console, 'connection error:'));
db.once('open', function () {
    // we're connected!
    console.log("Connected correctly to server");
});
`````
