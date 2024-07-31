import io.appwrite.Client
import io.appwrite.coroutines.CoroutineCallback
import io.appwrite.services.Storage

val client = Client(context)
    .setEndpoint("https://cloud.appwrite.io/v1") // Your API Endpoint
    .setProject("&lt;YOUR_PROJECT_ID&gt;") // Your project ID

val storage = Storage(client)

val result = storage.getFileView(
    bucketId = "<BUCKET_ID>", 
    fileId = "<FILE_ID>", 
)