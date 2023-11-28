import React, { useState, useEffect } from 'react';
const Blog = () => {
  const [posts, setPosts] = useState([]);
  const [loading, setLoading] = useState(true);
 useEffect(() => {
    // Simulating fetching blog posts with setTimeout
    const fetchPosts = () => {
      setLoading(true); // Set loading state to true while fetching
      setTimeout(() => {
        // Simulated API call
        const mockPosts = [
          { id: 1, title: 'First post', content: 'Content of first post' },
          { id: 2, title: 'Second post', content: 'Content of second post' },
          // Add more posts here...
        ];
        setPosts(mockPosts);
        setLoading(false); // Set loading state to false after fetching
      }, 2000); // Simulating a delay of 2 seconds
    };

    fetchPosts();
  }, []); // Empty dependency array to run the effect only once
  return (
    <div>
      {loading ? (
        <p>Loading...</p>
      ) : (
        <div>
          <h1>Blog Posts</h1>
          {posts.map((post) => (
            <div key={post.id}>
              <h2>{post.title}</h2>
              <p>{post.content}</p>
            </div>
          ))}
        </div>
      )}
    </div>
  );
};
export default Blog;
