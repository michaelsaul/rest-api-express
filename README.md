# Node.js REST API Example with MongoDB, Mongoskin, Express 4 for Azure

This project updates the upstream to add support for running an API Example with Azure App Service API App, DocumentDB (using Mongo DB Protocol Support).

## Environment Setup Instructions:

1. Create DocumentDB with Protocol Support for MongoDB.
2. Create Azure API App.
3. In the Azure API App and on your local box, set an Environment Variable for MONGO_DB_URL using URL from DocumentDB.
4. Download and test code.
> Note that the express.js applicaiton will look for the NODE_ENV environment variable. If it is "development" it will default to mongodb on localhost. Anything else will default to the URL stored in the MONGO_DB_URL environment variable.
```
$ git clone https://github.com/michaelsaul/rest-api-express.git
$ cd rest-api-express
$ npm install
$ node express.js
```

## Testing Instructions

1. Edit environment.sh.template and save as environment.sh
2. Source environment.sh
3. Use mocha to run test suite.
```
$ source environment.sh
$mocha express.test-azure.js 

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

## Original Project Information 

Original tutorial: <http://webapplog.com/express-js-4-node-js-and-mongodb-rest-api-tutorial/>