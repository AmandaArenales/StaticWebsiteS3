# StaticWebsiteS3
Creating a static website using Amazon S3

## Steps for creating a static website hosted on Amazon S3

1. Create a bucket
For this, you need to go to the amazon S3 console and click on create a bucket to store the data. After it, you need to create a bucket name that must need to be globally unique and choose the AWS region that is close to where in located. All the others settings I leave as default. Then I create a bucket. 

2. Upload the object
After the bucket is created, the file index.html was uploaded to the bucket. Under the Object, if you click on this file you will have more details about it.

3. Bucket Policy
To make the file public is necessary to go to the Permissions tab and first allow public access, so I disabled the "Block all public access". Before doing this make sure you really want to make the files on that bucket public.  After this, go to bucket policy and click on edit. Then, select the policy generator. In the Select Type of policy click "S3 Bucket Policy"; Effect click on "Allow"; Principal you need to write "*" because you want to allow anyone on the Amazon S3 Service to read the object on the bucket. So, in Actions you need to select "GetObject" and Amazon Resource Name (ARN) needs to be your "bucket name + /*" (in my case was: arn:aws:s3:::aarenales-web-static/*). After all, this is done, you click in generate policy. This will generate the policy that you will use on the "Bucket policy" and save the changes.

4. Creating a static website hosting
In the tap property, scroll down until "Static website hosting" click on edit, and select enable static website hosting. After that specify your index document, in my case index.html, and save it. Back to the property tap and scroll down again and you will see under the "Static website hosting" a "Bucket website endpoint" where you can copy the URL and you will be able to see your website (your index HTML file).



