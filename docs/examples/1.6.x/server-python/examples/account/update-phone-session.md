from appwrite.client import Client

client = Client()
client.set_endpoint('https://cloud.appwrite.io/v1') # Your API Endpoint
client.set_project('&lt;YOUR_PROJECT_ID&gt;') # Your project ID

account = Account(client)

result = account.update_phone_session(
    user_id = '<USER_ID>',
    secret = '<SECRET>'
)