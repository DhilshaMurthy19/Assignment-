const axios = require('axios');
async function getUsersWithPosts() {
  try {
    // Fetch users
    const usersResponse = await axios.get('https://jsonplaceholder.typicode.com/users');
    const users = usersResponse.data;

    // Fetch posts for each user
    const usersWithPosts = await Promise.all(
      users.map(async (user) => {
        const postsResponse = await axios.get(`https://jsonplaceholder.typicode.com/posts?userId=${user.id}`);
        const posts = postsResponse.data;
        return {
          ...user,
          posts
        };
      })
    );

    return usersWithPosts;
  } catch (error) {
    console.error('Error fetching data:', error);
    return null;
  }
}
// Example usage
getUsersWithPosts()
  .then((users) => {
    if (users) {
      console.log('Users with posts:', users);
    } else {
      console.log('Failed to fetch data.');
    }
  })
  .catch((error) => {
    console.error('Error:', error);
  });
