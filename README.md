# aabor.ninja
Alexander Borochkin personal web site

Site access points:
http://aabor.ninja
http://www.aabor.ninja

# Upload Website to AWS S3 bucket

```sh
# authorization need to perform the following
aws s3 cp ./www/ s3://www.aabor.ninja/ --recursive --exclude ".DS_Store" --dryrun
aws s3 cp ./www/ s3://www.aabor.ninja/ --recursive --exclude ".DS_Store"

# update website
aws s3 sync ./www/ s3://www.aabor.ninja/ --exclude ".DS_Store" --dryrun
aws s3 sync ./www/ s3://www.aabor.ninja/ --exclude ".DS_Store"
``` 
