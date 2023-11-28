const fs = require('fs');

// Read the JSON file
const readFile = (filePath) => {
  try {
    const data = fs.readFileSync(filePath, 'utf8');
    return JSON.parse(data);
  } catch (error) {
    console.error('Error reading file:', error);
    return null;
  }
};

// Calculate total posts for each user
const calculateTotalPosts = (users) => {
  return users.map((user) => ({
    ...user,
    totalPosts: user.posts.length
  }));
};

// Write modified data to a new JSON file
const writeFile = (filePath, data) => {
  try {
    fs.writeFileSync(filePath, JSON.stringify(data, null, 2));
    console.log('File has been written successfully!');
  } catch (error) {
    console.error('Error writing file:', error);
  }
};

// File paths
const inputFilePath = 'users.json';
const outputFilePath = 'users_with_total_posts.json';

// Read the data from the input file
const userData = readFile(inputFilePath);

if (userData) {
  // Calculate total posts for each user
  const usersWithTotalPosts = calculateTotalPosts(userData);

  // Write the modified data to a new file
  writeFile(outputFilePath, usersWithTotalPosts);
}
