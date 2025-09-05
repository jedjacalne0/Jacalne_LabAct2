# Laboratory Activity 2: CRUD API Implementation

This project is about the usage of Express.js connecting to a MySQL database. This project explores creating databases with aligned project structures and setting up routes, servers, and controllers for a fully functional database. 

# Step By Step Procedure
Ensure that MySQL and Apache are running in the XAMPP Control Panel
First, you create your database via PHP Admin, then set up your tables, including their structures. Verify it through XAMPP through the shell terminal. 

VERIFICATION THROUGH SHELL
- mysql -u root
- SHOW DATABASES;
- USE (database name);
- SHOW TABLES;
- DESCRIBE (table name);

Then we initialize our project structures, create controllers, routes, configs, server, and env file. 

PROJECT INITIALIZATION VIA TERMINAL IN VSCODE
npm init -y
npm install express mysql2 dotenv
npm install -D nodemon

After creating the project structures, first configure our env file.
Then we establish our database connection to MySQL.
Then we establish our express server while creating a health check endpoint to confirm that the app is running with a quick status. 

At this stage, we connect the “front desk” (routes) to the “workshop” (controllers). Routes define which endpoint is hit, and controllers execute what action against the database.
We will install and enable CORS (Cross-Origin Resource Sharing). This is crucial: if later you test from a frontend app (Vue, React, or plain HTML fetch), the browser will block requests unless CORS headers are present.
First, we install CORS

VIA TERMINAL IN VSCODE
npm install cors

Then we create our controller logic.
Then define our routes.
Then, mount the routes and enable CORS in our server.

TESTING
We can test the project via Postman.

Open Postman, then create an environment. Add a variable with its values being the URL of the port project (eg, http//localhost:3306/api). Save the environment and select it also from the dropdown (top-right corner).
Now test the health endpoint by creating a new tab and changing the method to GET. Add the endpoint URL (eg, http//localhost:3306/api). Go to the Headers tab, add a key value as "a Content-Type", then for the value cell add "application/json". click send then expect the response to be {"status": "ok", "db": "connected", "time":"..."}
Then, perform the CRUD Cycle:
POST/POST BY ID
GET/GET BY ID
PUT
DELETE/DELETE BY ID





