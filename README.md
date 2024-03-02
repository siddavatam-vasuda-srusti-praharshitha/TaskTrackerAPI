# TaskTrackerAPI
****Backed API for updating Database****
 <br />
Backend: Node.js with Express.js <br />
Databae: Sqlite3 <br />
IDE: Visual Studio <br />
Libraries : Stored in package.json <br />
  * nodemon - Automatic server restarting.  <br />
  * body-parser - Middleware in Express.js for parsing incoming request bodies(JSON). <br />
  * express-validator - Input validation in an Express.js application. <br />

 Start App.js:
  * Create a TaskTracker table if it doesn't exist.
  * Route GET, POST, PUT, DELETE requests to router.
  * App runs on localhost(9000).

 Routes:
  * getTask.js - Route GET request to Controller and returns tasks in response.
  * insertTask.js - Route the POST request to controller and insert the task into TaskTracker table.
  * updateTask.js - Route the PUT request to controller and update the task for given taskId in TaskTracker table.
  * deleteTask.js - Route the DELETE request to controller and delete the task of taskID from taskTracker table.
  * Handled input validation while receiving request using express-validator.

Controller:
 * Route the request to model and fetches response in callback from model(result from database).

Model:
 * Implemented methods for all the routes and returns response in callback to controller, by fetching data from TaskTracker table(taskModel.js).
 * Fetches queries from utils/config.json and stores data in database (sqlite.db).
 * Single db connection object is being used in database/dbconn.js for sqlite.db.

