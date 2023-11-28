// Logger middleware function
const requestLogger = (req, res, next) => {
  const timestamp = new Date().toISOString();
  const requestedUrl = req.originalUrl;
  console.log(`[${timestamp}] - Requested URL: ${requestedUrl}`);
  next(); // Move to the next middleware in the chain
};
// Implementing the middleware in Express js
const express = require('express');
const app = express();
// Using the middleware for all incoming requests
app.use(requestLogger);
// other routes and middleware will come here
// Start the server
const port = 3000;
app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
