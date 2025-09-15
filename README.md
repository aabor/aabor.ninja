# aabor.ninja
Alexander Borochkin personal web site

Site access points:
http://aabor.ninja
http://www.aabor.ninja

# Update resume in Google Drive
Open Google Drive folder in the Browser window.

To update a file in Google Drive without changing its shareable link, utilize the "Manage Versions" feature. Right-click the file, File Information>"Manage Versions," and upload the updated file. This replaces the old version while preserving the existing link.

# Upload Website to AWS S3 bucket

```sh
# authorization need to perform the following
aws s3 cp ./www/ s3://www.aabor.ninja/ --recursive --exclude "*.DS_Store" --dryrun
aws s3 cp ./www/ s3://www.aabor.ninja/ --recursive --exclude "*.DS_Store"

# update website
aws s3 sync ./www/ s3://www.aabor.ninja/ --exclude "*.DS_Store" --dryrun
aws s3 sync ./www/ s3://www.aabor.ninja/ --exclude "*.DS_Store"
``` 

# Cloudfront invalidation

```sh
aws cloudfront create-invalidation \
    --distribution-id EZ6G3O6BJTNUG \
    --paths "/index.html"

aws cloudfront create-invalidation \
    --distribution-id E2JTJ24WC5UG30 \
    --paths "/index.html"
```
