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

Lets connect AWS to Datadog (CloudWatch Integration)


















