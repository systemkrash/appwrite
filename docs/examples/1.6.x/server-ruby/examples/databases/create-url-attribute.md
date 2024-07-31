require 'appwrite'

include Appwrite

client = Client.new
    .set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
    .set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID
    .set_key('&lt;YOUR_API_KEY&gt;') # Your secret API key

databases = Databases.new(client)

result = databases.create_url_attribute(
    database_id: '<DATABASE_ID>',
    collection_id: '<COLLECTION_ID>',
    key: '',
    required: false,
    default: 'https://example.com', # optional
    array: false # optional
)