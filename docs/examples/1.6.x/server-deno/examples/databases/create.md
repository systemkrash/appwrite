import { Client, Databases } from "https://deno.land/x/appwrite/mod.ts";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;') // Your project ID
    .setKey('&lt;YOUR_API_KEY&gt;'); // Your secret API key

const databases = new Databases(client);

const response = await databases.create(
    '<DATABASE_ID>', // databaseId
    '<NAME>', // name
    false // enabled (optional)
);