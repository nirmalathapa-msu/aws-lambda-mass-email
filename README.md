# aws-lambda-mass-email

Step 1: Creating IAM Role

In the AWS console search for IAM in the search bar and select the service
In that select roles and click on Create role
Select use cases as Lambda and click on next
In permission, policies choose CloudWatch full access and SES full access and then click on next
Give a suitable name for the role and click on Create role
The role will be created

![image](https://github.com/user-attachments/assets/e76ab47b-9811-4180-b914-7daa9c115492)
![image](https://github.com/user-attachments/assets/f4936081-e162-42d4-98ca-0557a67bed0c)


Step 2: Creating Lambda Function

In the AWS console search for Lambda in the search bar and select the service.
Provide the name of the function.
In the position of runtime, we must choose the language that we want. Here, I am choosing the most recent NodeJS 16.x version.
Choose whether to create a new or existing role as the executing role in the following step. I’m choosing the role that I already created in the previous phase.
Rest everything. We can keep it optional
Select Create a Function


![image](https://github.com/user-attachments/assets/5f093386-6b47-45e6-aa22-3b175a802fb3)
After the creation of the lambda function, we need to write Lambda code to send an email
Next, choose to configure a test event
Give a suitable name for the test event and click on create
![image](https://github.com/user-attachments/assets/29a14040-d973-4c64-b05a-860944aead9e)
![image](https://github.com/user-attachments/assets/7eced84f-bfe9-42a8-9e4f-9c165ed9b293)


Step 3: Creating CloudWatch Events

In the AWS console search for CloudWatch in the search bar and select the service.
In the left navigation pane, select Event in that select rules and then click on create rule.
Next, choose the schedule and click on the Cron expression to set it to a specific time.
Select add target and choose the lambda function I’m choosing the function that I already created in the previous phase.
Click on configure details.
Next, give a name to the rule and rest everything we can keep optional
Click on Create the rule.

![image](https://github.com/user-attachments/assets/eebc03f4-52ff-49c9-8a0d-e4a2dd460b75)

![image](https://github.com/user-attachments/assets/e546b976-33be-426f-a3a8-56e918150e1a)

Result:
Lambda is triggered and sent an email to the users at the scheduled time

using AWS Lambda, IAM role, CloudWatch, and SES can be an efficient and reliable way to send mass emails. Lambda can be used to execute code that triggers email sending, while IAM roles can provide the necessary permissions to access SES. CloudWatch can be used to monitor and log the email-sending process, ensuring its successful completion. SES can be used to send bulk emails while providing features like email validation, suppression lists, and bounce handling. Overall, using these services in conjunction can provide a scalable and cost-effective solution for sending mass emails.






