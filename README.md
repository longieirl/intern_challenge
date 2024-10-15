### Coding Challenge: "Simple CSV Reader and CRUD API with Node.js"

**Overview**:

Welcome to your coding challenge!

The goal is to read data from a CSV file, load it into an in-memory data structure, and expose a RESTful API to perform basic CRUD operations on the data. This challenge will help you get familiar with working with `Node.js`, Express, and handling file operations.

**Challenge Requirements**:

1. **Read Data from a CSV File**:
    - You'll generate a CSV file named `data.csv` containing information about "employees". The CSV file will have the following columns:
        - `id` (number, unique)
        - `name` (string)
        - `email` (string)
        - `position` (string)
        - `salary` (number)
    - Your application should read the contents of this file when the server starts and load the data into an in-memory data structure (e.g. an array). You may use a library like `csv-parser` to parse the CSV file.


2. **Develop a RESTful API**:
    - Create a RESTful API using Express to perform CRUD operations on the employee data, the API should support the following endpoint:
    - **GET /employees**: Retrieve a list of all employees e.g. http://localhost:5000/employees
    - Refer to https://www.freecodecamp.org/ to understand more about how CRUD works and how to expose endpoints.


3. **Data Persistence**:
    - Since this is a simple application, the data can remain in memory (e.g. stored in an array) and does not need to be persisted across server restarts.


4. **Additional RESTful API endpoints (Optional)**:
   - Create a RESTful API using `Node.js` and `Express` to perform CRUD operations on the employee data. The API should support the following endpoints:
   - **GET /employees/:id**: Retrieve details of a specific employee by their ID.


5. **Data Validation (Optional)**:
    - Ensure the data is validated before performing any operations:
        - `name` should not be empty.
        - `email` should be a valid email format.
        - `position` should not be empty.
        - `salary` should be a positive number.
    - If validation fails, return a `400 Bad Request` with an appropriate error message.


6. **Unit Tests (Optional)**:
    - `Jest` is a JavaScript testing framework designed to ensure correctness of any JavaScript codebase.
    - Refer to https://jestjs.io/docs/getting-started

### Deliverables:
1. A working `Node.js` application that meets the requirements.
2. A `README.md` file explaining how to set up and run the project.
3. The `data.csv` file used for testing.

### Getting Started:
1. **Initialize a new `Node.js` project**:
    - Create a new project folder e.g. `internchallenge_myname`
    - Change into the new project folder and run `npm init` to create a new `Node.js` project, accept all other defaults during the prompting.
    - Install the necessary dependencies (`express` for the web framework and a CSV parsing library like `csv-parser`).
    - You do not need to install `fs` since this component is part of the `Node.js` framework.

2. **Create an `index.js` File**:
    - This will be the main entry point for your application.
    - Implement code using `csv-paraser` to read the `data.csv` file into an array, you can use `console.log` to ensure you have read the data correctly!
    - Implement code to set up the `Express` server to render the data to the frontend e.g. when `http://localhost:5000` is called, it returns the data in JSON format.

3. **Test Your Endpoints**:
    - Use a tool like Postman or curl to test the REST API endpoints.

### Sample `data.csv` Content:
```csv
id,name,email,position,salary
1,John Doe,john.doe@example.com,Software Engineer,75000
2,Jane Smith,jane.smith@example.com,Project Manager,90000
3,Bob Johnson,bob.johnson@example.com,QA Tester,60000
```

### Additional notes/links:
Notes;
Look at using `nodemon` to handle refreshing your app when you make changes.

Links;
https://nodejs.org/en/download/package-manager
https://www.npmjs.com/package/csv-parser
https://www.npmjs.com/package/express

### Common Errors;

`SyntaxError: Cannot use import statement outside a module`</br> 
Solution: Update the package.json with `"type": "module"

`Error: listen EADDRINUSE: address already in use :::5000` </br>
Solution: Edit your entry file e.g. index.js and change the port to a unique value

`Error: ReferenceError: require is not defined in ES module scope, you can use import instead` </br>
Solution: Ensure the project `package.json` is updated with `"type": "module"`, for example;
```JSON
{
  "name": "internchallenge_myname",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "type": "module",
  ...
```
The `module` type forces your project to use `import fs from 'fs';` instead of `const fs = require('fs')` when consuming third party libraries.

### Submission:
- Create a GitHub repository for your code.
- Commit your code and share the repository link for review.

Good luck!
