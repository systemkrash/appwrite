import 'package:appwrite/appwrite.dart';

Client client = Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('&lt;YOUR_PROJECT_ID&gt;'); // Your project ID

Databases databases = Databases(client);

Document result = await databases.updateDocument(
    databaseId: '<DATABASE_ID>',
    collectionId: '<COLLECTION_ID>',
    documentId: '<DOCUMENT_ID>',
    data: {}, // optional
    permissions: ["read("any")"], // optional
);