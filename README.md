Lab Brief 
Course: Cloud Computing on AWS 
Storage I Volumes, S3, CLI 
(Add volumes to EC2 instance, migrate data from one volume to the other, write a 
CLI to upload documents to S3 from local machine) 

What is needed? 
1. AWS Account Credentials
2. EC2 Instances (Linux)
3. Shell script environment (any text editor of your choice)
4. Full access to - Volumes, Snapshots, S3, EFS, 1AM
5. Access to create an S3 bucket in 1 other region (Oregon) with cross region replication
access

Command reference  
To elevate your privileges to root 
0. sudo su
All following commands require you to be root 
1. lsblk
2. file -s /dev/xvdf
3. mkfs -t ext4 /dev/xvdf
4. mkdir /appdata
5. mount /dev/xvdf /appdata
6. echo 11This is a sample file11 > /appdata/sample.txt
7. umount /dev/xvdf
Note - umount will not work if the pwd is /appdata.

The CLI set of commands are as 
follows 
1. aws s3 cp [file]
s3://[bucket/folder/fi le]
2. aws s3 Is [bucket]
3. aws s3 rm s3:/ /[bucket/file]
