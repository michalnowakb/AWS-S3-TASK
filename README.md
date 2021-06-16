p### AWS-S3-TASK

## HOW TO CREATE A BUCKET FOR AWS S3, TRANSFER FILE AND MAKE IT PUBLIC


- first we have to create an EC2 instance
- we have to `SSH` to our instance
- type in your terminal following commands
- `sudo apt-get update`
- `sudo apt-get upgrade`
- `sudo apt-get install python`
- `sudo apt-get install python-pip`
- `sudo apt-get install awscli`
- `sudo apt-get install awscli`

To cofigure our aws access:
- `aws configure`
	- `AWS Access Key ID[None]:` - we have to insert here our Access Key ID
	- `AWS Secret Access Key [None]:` - we have to insert here our Secret Access Key
	- `Default region name [None]: eu-west-1` - we have to insert the region that we want to have our bucket on
	- `Default output format [None]: json` - select in which format we would like to have our file that we will have in our bucket

To create new S3 bucket we have to type following command:
- `aws s3 mb s3://devops-bootcamp-michal-bucket`
Now we can create a file that we will transfer from our EC2 instance to S3 bucket
- `nano devops_bootcamp_michal_s3.text`
To transfer file we have to type following:
- `aws s3 cp devops_bootcamp_michal_s3.text s3://devops-bootcamp-michal-bucket`
To make our file public we have to go to our S3 Buckets
select bucket that we just recently created, to check what do we have in our bucket we have to click on our bucket name, now we have to click on file that we want to change permission for and on the top rigth we have to select `Object actions` and choose from drop-down option at very bottom `Make Public`
