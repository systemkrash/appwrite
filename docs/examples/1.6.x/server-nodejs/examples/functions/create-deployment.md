const sdk = require('node-appwrite');
const fs = require('fs');

const client = new sdk.Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const functions = new sdk.Functions(client);

const result = await functions.createDeployment(
    '<FUNCTION_ID>', // functionId
    InputFile.fromPath('/path/to/file', 'filename'), // code
    false, // activate
    '<ENTRYPOINT>', // entrypoint (optional)
    '<COMMANDS>' // commands (optional)
);