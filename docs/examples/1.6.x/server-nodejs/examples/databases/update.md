const sdk = require('node-appwrite');

const client = new sdk.Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const databases = new sdk.Databases(client);

const result = await databases.update(
    '<DATABASE_ID>', // databaseId
    '<NAME>', // name
    false // enabled (optional)
);