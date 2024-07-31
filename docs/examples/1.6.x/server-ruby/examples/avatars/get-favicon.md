require 'appwrite'

include Appwrite

client = Client.new
    .set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
    .set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID
    .set_session('') # The user session to authenticate with

avatars = Avatars.new(client)

result = avatars.get_favicon(
    url: 'https://example.com'
)