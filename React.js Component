import React, { useState, useEffect } from 'react';
import axios from 'axios';

const BlogPosts = () => {
  const [posts, setPosts] = useState([]);

  useEffect(() => {
    // Fetch blog posts from an API (replace URL with your API endpoint)
    axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(response => {
        setPosts(response.data);
      })
      .catch(error => {
        console.error('Error fetching posts:', error);
      });
  }, []);

  const handleViewPost = (postId) => {
    // Handle the action to view the full post (e.g., navigate to the post page)
    console.log(`View full post with ID: ${postId}`);
  };

  return (
    <div>
      <h1>Blog Posts</h1>
      {posts.map(post => (
        <div key={post.id} style={{ border: '1px solid #ccc', padding: '10px', marginBottom: '10px' }}>
          <h2>{post.title}</h2>
          <p>Author: User {post.userId}</p>
          <button onClick={() => handleViewPost(post.id)}>View Full Post</button>
        </div>
      ))}
    </div>
  );
};
export default BlogPosts;
