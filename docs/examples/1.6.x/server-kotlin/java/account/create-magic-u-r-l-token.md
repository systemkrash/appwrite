import io.appwrite.Client;
import io.appwrite.coroutines.CoroutineCallback;
import io.appwrite.services.Account;

Client client = new Client()
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;"); // Your project ID

Account account = new Account(client);

account.createMagicURLToken(
    "<USER_ID>", // userId
    "email@example.com", // email
    "https://example.com", // url (optional)
    false, // phrase (optional)
    new CoroutineCallback<>((result, error) -> {
        if (error != null) {
            error.printStackTrace();
            return;
        }

        System.out.println(result);
    })
);
