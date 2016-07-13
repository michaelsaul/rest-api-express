> Node.js REST API Example with MongoDB, Mongoskin, Express 4 for Azure

This project updates the upstream to add support for running an API Example with Azure App Service API App, DocumentDB (using Mongo DB Protocol Support).

Brief instructions:

1. Create DocumentDB with Mongo Protocol Support.
2. Create Azure API App.
3. Set Environment Variable for MONGO_DB_URL using URL from DocumentDB.
4. Download and test code.
```
$ git clone https://github.com/michaelsaul/rest-api-express.git
$ cd rest-api-express
$ npm install
$ node express.js
```

5. Push changes to Azure App Service.
6. Edit environment.sh.template and save as environment.sh
7. Test configuration using environment.sh script.
```
$ sh environment.sh


  express rest api server
    ✓ posts an object (101ms)
    ✓ retrieves an object (67ms)
    ✓ retrieves a collection (57ms)
    ✓ updates an object (67ms)
    ✓ checks an updated object (49ms)
    ✓ removes an object (66ms)
    ✓ checks an removed object (56ms)


  7 passing (472ms)
```

# Original Project Information 

## Express.js 4.x

`master` branch

Original tutorial: <http://webapplog.com/express-js-4-node-js-and-mongodb-rest-api-tutorial/>

Brief instructions:

```
$ git clone https://github.com/azat-co/rest-api-express.git
$ cd rest-api-express
$ npm install
$ node express.js
```

In a new terminal window:

```
$ mocha express.test.js
```

Or, if you don't have mocha installed globally:

```
$ ./node_modules/mocha/bin/mocha express.test.js
```

You can use `package.json` commands:

```
$ npm start
$ npm test
```