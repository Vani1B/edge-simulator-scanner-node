# edge-simulator-scanner-node

# 📡 Edge Scanner Telemetry Monitoring with AWS & Datadog

This project simulates a real-time edge computing scenario where barcode scanners (as edge devices) send telemetry data to a central system hosted on AWS. The telemetry is monitored using Datadog, with dashboards and alerts configured to ensure availability, performance, and proactive remediation.

---

## 🎯 Project Goals

- Simulate edge scanner telemetry (e.g., scan count, failure rate, latency)
- Ingest metrics into Datadog for real-time observability
- Visualize scanner performance through dashboards
- Set up alerting for scanner anomalies
- Automate service restart if telemetry agent fails

---


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

Now in CloudWatch create subscription filter to connect Lambda. 

![image](https://github.com/user-attachments/assets/dce4e35b-eefa-4ad7-89d8-8f05770d75db)

Now go to Lambda, copy ARN and add the ARN to Datadag Integration

![image](https://github.com/user-attachments/assets/6a4cf170-d09e-44fa-ba21-290b5620c6a1)

![image](https://github.com/user-attachments/assets/26eb90d0-48e5-443e-bd87-1a1ad4518bc6)

Metrics are showing

![image](https://github.com/user-attachments/assets/7a0b9d3e-0c5a-47b0-824b-3f4893f3e9e2)

Log explorer started working

![image](https://github.com/user-attachments/assets/3727b099-67bd-450e-bf75-def61a71e2f3)

Infrasturcture is up

![image](https://github.com/user-attachments/assets/498e26dd-c742-440f-83d9-e88740923b9c)


create the custom Dashboard named it as scannerTelemetry Dashboard

![image](https://github.com/user-attachments/assets/a00ca0a2-dc78-4fc9-ad77-9e30fc2af343)

![image](https://github.com/user-attachments/assets/2704dc85-4893-4dca-9db1-cce24a5fd35f)














































