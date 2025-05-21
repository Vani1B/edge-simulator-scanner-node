# edge-simulator-scanner-node


Launch Ec2 instance with type t2.micro

![image](https://github.com/user-attachments/assets/28f4656e-99f1-40ea-9866-4233366a521c)

ssh to the instance and install boto3 inside a python virtual environment

![image](https://github.com/user-attachments/assets/e2335c17-577f-4f93-acfa-c6df378bf8ba)

Create file name scanner_telemetry.py and add the python script 

![image](https://github.com/user-attachments/assets/a8c988b1-54c1-4efd-9f4b-0bd13f5905f4)

Run python scanner_telemetry.py to see the logs locally

![image](https://github.com/user-attachments/assets/a72c8592-d328-4ab9-ad79-6653690ee064)

Now to push these logs to Aws cloud watch, attach IAM role to the instance

![image](https://github.com/user-attachments/assets/72a0466a-dd24-41af-a4a5-263758b65d9e)

Change the python script to cloudwatch logs

![image](https://github.com/user-attachments/assets/cf0bb618-3e8f-4841-995e-ec0dccc6191a)

Now loginto Cloud watch log and go to log groups find scanner telemetry

![image](https://github.com/user-attachments/assets/ea1ad26e-7e0f-4dfb-93a0-9c6a3ae6c7cf)

![image](https://github.com/user-attachments/assets/acec960f-1771-4108-b760-96f27d66c12f)

scanner log stream events

![image](https://github.com/user-attachments/assets/706b476a-a4e8-46d6-a73d-dfede6519d4b)

Lets connect AWS to Datadog (CloudWatch Integration). Go to Datadog dashboard and select linux

![image](https://github.com/user-attachments/assets/b6f8f34c-017a-4c4b-ae4f-4365c3b6974e)

Install Datadog agent in Ec2 instance

![image](https://github.com/user-attachments/assets/72172614-30a7-4c11-b6c1-e075dd7efe82)

Agent got connected Datadog UI

![image](https://github.com/user-attachments/assets/9ece263f-1bbc-42bf-81e8-77baa1665ced)

Instance connected to Datadaog

![image](https://github.com/user-attachments/assets/234d33b6-ad72-4d8d-9e25-a83e4e4480fa)

![image](https://github.com/user-attachments/assets/b7822a64-0655-4e59-b741-41a8bfa359b7)

To push the logs from cloudwatch to datadog we need datadog forwarder. Used cloud formation to create datadog forwarder

![image](https://github.com/user-attachments/assets/db5f3af4-72f9-46ef-8b8f-fc92e8ff303f)





























