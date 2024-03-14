# core-collection
The InTouch Core Services Postman Collection


Organisation ID

The Organisation ID retrieved from the “Get ID” call is used in the initiation process for workflows. We’ve created this as an environment variable so it can be managed across the calls from your environment. 


Initiation of Calls

The initiation calls, given your Organisation ID, will start the process for the given workflow and return a Tracking ID so you can keep track of the workflow process. You can do this from the status call, inputing the Tracking ID as a path variable. The call will return the current status of the workflow process, returning results for each call within the workflow as they run. For calls that return encoded data, the workflow process will include decoding the document or image and uploading it to a private S3 bucket. You will then see a document and/or image URL in your results, with a secure, pre-signed link to your file. For security reasons, these links expire after 24-hours.


