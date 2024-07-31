import { Client, Databases } from "@appwrite.io/console";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;'); // Your project ID

const databases = new Databases(client);

const result = await databases.createIntegerAttribute(
    '<DATABASE_ID>', // databaseId
    '<COLLECTION_ID>', // collectionId
    '', // key
    false, // required
    null, // min (optional)
    null, // max (optional)
    null, // default (optional)
    false // array (optional)
);

console.log(response);