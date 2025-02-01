
# **Serverless Email Marketing Project**  

This project provides a **serverless email marketing solution** using **AWS Lambda, S3, SES, EventBridge, and IAM**. It automates sending personalized emails to target users based on CSV data stored in **Amazon S3**.  

## **Project Overview**  
This project automates the email marketing process using a **serverless architecture**. By leveraging:  
- **AWS Lambda** for computation  
- **S3** for storage  
- **SES** for email sending  
- **EventBridge** for scheduling  

This ensures a **scalable and cost-effective** email marketing solution.  

## **Prerequisites**  
- ✅ **A validated email address** (must be from a domain)  
- ✅ **Basic AWS knowledge**  
- ✅ **A text editor** to edit HTML email templates (or use `email.html` provided in the repo)  

## **🛠 Architecture Diagram**  
*(Insert architecture diagram here if available.)*  

## **📌 High-Level Requirements**  
1. A storage solution for **email templates and contact lists** (**S3**).  
2. A mechanism for **sending emails** (**SES**).  
3. A process to **merge emails with contacts** and send them (**Lambda**).  
4. A scheduler to **trigger emails at set intervals** (**EventBridge**).  
5. **Access management** using IAM roles and policies.  

---

## **🚀 Setup Guide**  

### **Step 1: AWS S3 Bucket Setup**  
1. Open the **Amazon S3** console.  
2. Click **Create Bucket**.  
3. Name the bucket (e.g., `email-marketing-project`) and keep the default settings.  

### **Step 2: Upload Contacts and Email Template**  
1. Upload **`contacts.csv`** and **`email.html`** to the created S3 bucket.  

### **Step 3: AWS SES Setup**  
1. Open **Amazon SES** in AWS.  
2. Verify your **email** and **domain**.  
3. Create an **Identity** (Minimum **2**).  

### **Step 4: Lambda Function Configuration**  
1. Open **AWS Lambda**.  
2. Create a new function.  
3. Upload **`LambdaFuction.py`**.  
4. Test and deploy the function.  

### **Step 5: IAM Policy Configuration**  
1. Open **IAM** in AWS.  
2. Create a new **Policy** and paste the contents of **`AMIpolicyForSES.txt`** in **JSON format**.  
3. Attach this policy to the **Lambda execution role**.  

### **Step 6: EventBridge Rule Configuration**  
1. Open **EventBridge** in AWS.  
2. Create a **rule** to schedule email sending.  

---

## **📩 Email Output Format**  

Once the setup is complete, AWS SES sends emails based on the **EventBridge schedule**. Below is a sample **email output format**:  

```plaintext
From: noreply@yourdomain.com  
To: recipient@example.com  
Subject: Welcome to Our Newsletter!  

Hello [Recipient Name],  

Thank you for subscribing to our newsletter! We are excited to have you onboard.  
Stay tuned for the latest updates and exclusive offers.  

Best regards,  
[Your Company Name]  
```

---

## **🔥 Project Benefits**  
✔ **Fully Serverless** – No infrastructure management.  
✔ **Scalable & Cost-Effective** – Pay only for what you use.  
✔ **Automated & Secure** – IAM-managed permissions for security.  

---

## **📎 Resources & Links**  
- **AWS Lambda Documentation:** [AWS Lambda](https://docs.aws.amazon.com/lambda/)  
- **Amazon S3 Guide:** [AWS S3](https://docs.aws.amazon.com/s3/)  
- **AWS SES Overview:** [AWS SES](https://docs.aws.amazon.com/ses/)  
- **AWS IAM Policies:** [AWS IAM](https://docs.aws.amazon.com/iam/)  
- **AWS EventBridge Setup:** [AWS EventBridge](https://docs.aws.amazon.com/eventbridge/)  

---

🚀 **Built with AWS for seamless and automated email marketing!**  

---

