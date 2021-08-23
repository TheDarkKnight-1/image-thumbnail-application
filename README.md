# Image Thumbnail Application

<ul>
  <li>A user uploads an object to the source bucket in Amazon S3 (object-created event).</li>
  <li>Amazon S3 detects the object-created event.</li>
  <li>Amazon S3 publishes the object-created event to AWS Lambda by invoking the Lambda function and passing event data as a function parameter.</li>
  <li>AWS Lambda executes the Lambda function.</li>
  <li>From the event data it receives, the Lambda function knows the source bucket name and object key name. The Lambda function reads the object and creates a thumbnail using graphics libraries, then saves the thumbnail to the target bucket.</li>
</ul>

## Architecture

![alt text](https://github.com/TheDarkKnight-1/image-thumbnail-application/blob/main/arc.png?raw=true)
