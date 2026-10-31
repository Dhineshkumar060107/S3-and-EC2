# Experiment No. 2 — Cloud Storage Creation (S3) and Launching an EC2 Instance in AWS
# Reg No:2122224230066
# Name:Dhineshkumar L

## Aim
To create an Amazon S3 bucket for cloud storage and launch a virtual machine using Amazon EC2 in the AWS Management Console.

## Objectives
After completing this experiment, students will be able to:
- Understand AWS Cloud Storage (Amazon S3)
- Create and manage S3 buckets
- Upload and organize files in cloud storage
- Launch an EC2 virtual server
- Connect to an EC2 instance
- Understand cloud computing infrastructure services

## Software Requirements
- Laptop/Desktop
- Internet connection
- AWS Academy Learner Account / AWS Free Tier Account
- Modern web browser (Chrome/Edge)

## Theory

### Amazon S3 (Simple Storage Service)
Amazon S3 is an object storage service provided by AWS that stores unlimited amounts of data with high durability and availability.

**Features:**
- Unlimited storage
- 99.999999999% (11 nines) durability
- High availability
- Secure storage
- Versioning
- Lifecycle management
- Encryption

---

## Part A — Creating an Amazon S3 Bucket

1. Open the AWS console: [https://aws.amazon.com/console/](https://aws.amazon.com/console/)  

<img width="1907" height="1092" alt="image" src="https://github.com/user-attachments/assets/618c9f70-482b-411a-9248-194de8ad7682" />


2. Log in:
   - Click **Sign in using root user email**
   - Enter the registered email address
   - Enter the AWS password
   - Complete the verification process

<img width="1907" height="1135" alt="Screenshot 2026-10-31 103438" src="https://github.com/user-attachments/assets/5ea75982-353a-4358-a24b-96c2be178726" />


3. Type **S3** in the search box.

<img width="1902" height="1086" alt="Screenshot 2026-10-31 103605" src="https://github.com/user-attachments/assets/d2258b6a-7daf-4e75-b670-9b72b97e22e0" />


5. Click **Amazon S3**.
6. Click **Create bucket**.
7. Enter the following details:

   | Parameter    | Value                      |
   |--------------|-----------------------------|
   | Bucket type  | General purpose            |
   | Bucket name  | `student-cloud-storage-001` |
   | AWS Region   | Asia Pacific (Mumbai)      |

<img width="1917" height="1088" alt="Screenshot 2026-10-31 103722" src="https://github.com/user-attachments/assets/36d824ac-65c7-4fb4-83e5-834a49429ca2" />


9. Leave the remaining settings unchanged.
11. Click **Create bucket**.

<img width="1916" height="1088" alt="Screenshot 2026-10-31 103815" src="https://github.com/user-attachments/assets/7703fb8d-8dd2-45d4-a26a-35f31e31b54b" />


12. Click **Upload**.
13. Upload the following files:
    - PDF file
    - Word document
    - Image file

<img width="1917" height="1095" alt="Screenshot 2026-10-31 104422" src="https://github.com/user-attachments/assets/90d184e9-d28b-4bd8-98d6-51de9e926a50" />

    
**Example bucket structure:**
```
dhinesh-cloud-storage-001
│
├── dk_pic.jpg
├── 26-27-ODD-SH4601(FNHT)-SA-...
└── Cloud Security Exp 1.pdf
```
<img width="1917" height="1095" alt="Screenshot 2026-10-31 104422" src="https://github.com/user-attachments/assets/c8e7d5f1-5494-43df-a83f-45561dfc3b01" />


---

## Part B — Launching an Amazon EC2 Instance

1. Type **EC2** in the AWS search bar.

<img width="1912" height="1090" alt="Screenshot 2026-10-31 104445" src="https://github.com/user-attachments/assets/b11ae78b-ef63-4a9f-a69b-b4873b0c02e6" />


2. Open the **EC2 Dashboard**.

<img width="1911" height="1087" alt="Screenshot 2026-10-31 104727" src="https://github.com/user-attachments/assets/c15dd859-7cee-45a0-b6fe-792dcc5c3ff2" />


3. Click **Launch instance**.
4. Enter the instance name: `CloudLabVM`
5. Select the operating system:
   - Amazon Linux 2023
   - Ubuntu Server
6. Select the instance type: `t3.micro`
7. Create a key pair:

   | Parameter      | Value        |
   |----------------|--------------|
   | Key pair name  | `CloudLabKey`|
   | Key pair type  | RSA          |
   | File format    | `.pem`       |

8. Download the `CloudLabKey.pem` file.
9. Configure network settings:
   - ✅ Allow SSH traffic (Port 22)
   - ✅ Allow HTTP traffic (Port 80)
   - ✅ Allow HTTPS traffic (Port 443)
10. Set the storage size: `8 GiB`
11. Click **Launch instance**.

<img width="1912" height="1087" alt="Screenshot 2026-10-31 104801" src="https://github.com/user-attachments/assets/00d8d702-f6f9-4040-83cc-1c7554c0944b" />


12. Wait until the status changes:

<img width="1908" height="1086" alt="Screenshot 2026-10-31 104936" src="https://github.com/user-attachments/assets/a62439f9-0895-4e12-9460-702951ff3aa0" />

<img width="1913" height="1097" alt="Screenshot 2026-10-31 104955" src="https://github.com/user-attachments/assets/33ca413c-2537-41ba-9672-7dbb25bfbd3a" />



    ```
    Pending → Running
    ```

### Connecting to the EC2 Instance
1. Open **EC2**.
2. Select the instance.

<img width="1912" height="1082" alt="Screenshot 2026-10-31 105022" src="https://github.com/user-attachments/assets/6ecc90a8-2541-4cff-bd4c-5c64a3db9cd3" />

3. Click **Connect**.

<img width="1917" height="1086" alt="Screenshot 2026-10-31 105351" src="https://github.com/user-attachments/assets/f6303fe6-f425-4179-bbdd-61f6f9755604" />



4. Select **EC2 Instance Connect**.
5. Click **Connect**.

6. Execute the following command:

   ```bash
   echo "Hello AWS"
   ```

   **Output:**
   ```
   Hello AWS
   ```

<img width="1908" height="1145" alt="Screenshot 2026-10-31 105459" src="https://github.com/user-attachments/assets/f2b53f6b-561d-4cef-a631-d1c2a85e7c16" />
<img width="1915" height="1086" alt="Screenshot 2026-10-31 105604" src="https://github.com/user-attachments/assets/e3331b11-2817-4c5c-9cb4-93472098153a" />


<img width="1917" height="1078" alt="Screenshot 2026-10-31 105641" src="https://github.com/user-attachments/assets/a81f4909-4186-45b5-82fe-f5d4da26f556" />



### Stopping the EC2 Instance
1. Open **EC2**.
2. Select **Instances**.
3. Select the running instance.
4. Click **Instance state**.

<img width="1916" height="1077" alt="Screenshot 2026-10-31 105659" src="https://github.com/user-attachments/assets/fffda5f8-6ff0-4159-b876-45e9f60cad21" />


5. Click **Stop instance**.

   **Status flow:**
   ```
   Running → Stopping → Stopped
   ```
<img width="1903" height="1095" alt="Screenshot 2026-10-31 105706" src="https://github.com/user-attachments/assets/0c43e093-a9c3-44d7-b64a-9ed842a66501" />



### Logging Out of AWS
1. Click the profile icon in the upper-right corner.
2. Select **Sign out**.

---

## Result
The Amazon S3 bucket was created successfully, files were uploaded, an EC2 instance was launched, and the virtual machine was connected successfully.
# CLOUD-STORAGE-CREATION-S3-AND-LAUNCHING-AN-EC2-INSTANCE-IN-AWS-
