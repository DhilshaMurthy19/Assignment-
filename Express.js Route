// Assuming you have a database connection and a Post model
const express = require('express');
const app = express();
// Endpoint to retrieve posts as JSON
app.get('/posts', async (req, res) => {
  try {
    // Assuming Post is the model representing your posts
    const posts = await Post.find(); 
  // Fetch all posts from the database
    res.json({ posts }); // Return the posts as JSON
   } catch (error) {
    console.error(error);
    res.status(500).json({ error: 'Failed to retrieve posts' });
  }
});
// Start the server
const port = 3000;
app.listen(port, () => {
  console.log(`Server is running on port ${port}`);
});
