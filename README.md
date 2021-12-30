# AWS_S3_Uploader
Uploads file to an AWS S3 storage bucket.

You need to have an IAM user with a full S3 access (AmazonS3FullAccess) policy. There might be a more restricted one that's better suited to this, but this policy works fine.
Put the access key and secret key in the correct location.

Add the files (with their full paths) to a "List.txt" file in the same folder as the .exe file. Each file should be seperated with a new line. You could also set a full path in the code to the text file. 
From there it reads the text file, saves all the files to a list, and enters the part where they are uploaded.
Here it names the object being uploaded as the filename (logically), and uploads it. I set mine up to upload the the glacier deep archive type, but have commented out that line.
If it fails to upload for some reason, it'll try to upload the same file repeatably until it succeeds or is manually stopped.
If it succeeds it'll continue onto the next file.
There are outputs showing if the upload was successfull or not, with timestamps.

I have no idea how secure this approach to uploading files is, but it works for me. If this program causes issues for you, you have only yourself to blame for following some random script you found on Github.
