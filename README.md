# AWS-S3
# How To Configure S3 Static Website in AWS​

1. Login to your AWS environment. Click on Services.
2. Click on S3.
3. Click on create bucket.
4. Give it a name > select your region.
5. Click on create bucket.
   
**Note - Bucket Names requirement: Must be unique across all of AWS. Must be 3 to 63 characters in length. Can only contain lowercase letters, numbers, and hyphens.

7. Click on the bucket you just created.
8. Click on upload and select your html file (index.html) as well as any .js or .css.
9. Click on properties, scroll to the bottom of the page to enable Static website hosting.
10. Click on the edit button and then enable.
11. Click on save changes.
12. Click on properties.
13. Click on permissions.
14. Click on edit. Deselect block all public access.
15. Click on save changes.
16. Type “confirm” and click on confirm.
17. Under Permissions, click on edit Bucket policy. Update the Resource with your bucket arn.
    
{
“Version”: “2012–10–17”,
“Statement”: [
{
“Sid”: “AllowPublicAccesstoObjects”,
“Effect”: “Allow”,
“Principal”: “*”,
“Action”: “s3:GetObject”,
“Resource”: “arn:aws:s3:::yourbucketname/*”
}
]
}

**note - Replace "yourbucketname" with the bucket name you created.

19. Click on Save changes.



