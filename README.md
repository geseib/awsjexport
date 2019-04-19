# awsjexport

* Create or Determine an S3 Bucket to use for uploading the zipped python code to lambda
* Copy index.zip to this bucket
* run **juntoDownloadDataSet-v0.3.yaml** cloudformation template with the following info:
    * Junto DataSet ARN that is in a PRoduct that you have a subscription to
    * The name of the S3 Bucket 
    
### Completed
Now whenever a new Revision is published, an Cloudwatch Event triggers Lambda to copy the file to the S3 folders


### Ideas to enhance:
* Create a lifecycle on the S3 bucket to move to Infrequent access S3 or to Delete the object after x number of days

