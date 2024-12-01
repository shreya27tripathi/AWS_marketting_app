# AWS_marketting_app
### Step 1: Setting Up S3 Bucket
1.	Navigate to S3: Go to the AWS Management Console and select the S3 service.
2.	Create Bucket: Click on the "Create bucket" button.
3.	Bucket Configuration: Enter a unique bucket name, select the region, and click "Next".
4.	Set Permissions: Keep the default settings or customize as needed, then click "Next".
5.	Review: Review the configuration and click "Create bucket".
### Step 2: Uploading Files to S3
1.	Navigate to Bucket: Click on the bucket you created.
2.	Upload HTML Template: Click on the "Upload" button and select the HTML email template file (email_template.html).
3.	Upload Contact List: Click on the "Upload" button again and select the CSV contact list file (contacts.csv).
### Step 3: Configuring SES
1.	Navigate to SES: Go to the AWS Management Console and select the SES service.
2.	Verify Email Address: Under "Email Addresses" in the left sidebar, click "Verify a New Email Address" and follow the instructions to verify your sender email address.
3.	Verify Domain: If you haven't already verified your domain, navigate to "Domains" in the left sidebar, click "Verify a New Domain", and follow the instructions.
4.	Request Sandbox Removal (Optional): If you're still in the SES sandbox, follow the instructions to request sandbox removal.
### Step 4: Creating Lambda Function
1.	Navigate to Lambda: Go to the AWS Management Console and select the Lambda service.
2.	Create Function: Click on the "Create function" button.
3.	Configure Function: Choose "Author from scratch", enter a name for your function, select Python as the runtime, and choose an existing role with basic Lambda permissions or create a new one.
4.	Write Code: In the function code editor, paste the Python code provided in the Lambda Function Python Code section.
5.	Set Environment Variables: Add environment variables for the S3 bucket name and sender email address.
6.	Save Function: Click on the "Save" button.
### Step 5: Setting IAM Permissions
1.	Navigate to IAM: Go to the AWS Management Console and select the IAM service.
2.	Create Policy: Click on "Policies" in the left sidebar, then "Create policy", and choose the JSON tab. Paste the IAM policy JSON code provided in the Policies section.
3.	Attach Policy: Attach the created policy to the IAM role associated with your Lambda function.
### Step 6: Configuring EventBridge
1.	Navigate to EventBridge: Go to the AWS Management Console and select the EventBridge service.
2.	Create Rule: Click on "Create rule" and configure a rule to trigger the Lambda function on a schedule.

