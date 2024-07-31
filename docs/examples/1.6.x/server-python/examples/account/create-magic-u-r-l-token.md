from appwrite.client import Client

client = Client()
client.set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
client.set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID

account = Account(client)

result = account.create_magic_url_token(
    user_id = '<USER_ID>',
    email = 'email@example.com',
    url = 'https://example.com', # optional
    phrase = False # optional
)