Perfect 👍 Thanks for sharing the module. I’ll create a **comprehensive MCQ set with answers and explanations** that covers **all Module 1 topics** (AWS SDK, CLI, Management Console, Local Zones, IAM and its subtopics).

Here’s the full set:

---

# ✅ **Module 1 – AWS MCQs with Answers & Explanations**

---

## **AWS SDK**

**1. Which of the following best describes the AWS SDK?**
a) A web-based user interface for AWS
b) A set of software libraries for developers to interact with AWS services
c) A command-line interface tool for AWS
d) A physical appliance to run AWS services locally

**Answer:** b
**Reason:** AWS SDK is a **software development kit** that provides libraries for multiple programming languages (Java, Python, C#, Go, JavaScript, etc.) to easily integrate AWS services into applications.

---

**2. What advantage does AWS SDK provide compared to using raw APIs?**
a) Reduces latency in AWS networking
b) Automates request signing, retries, and error handling
c) Provides GUI access to AWS services
d) Creates IAM users automatically

**Answer:** b
**Reason:** AWS SDK **automatically signs requests**, retries failed calls with exponential backoff, and handles error responses, saving developers time.

---

**3. Which programming language is NOT officially supported by AWS SDK?**
a) Python
b) Java
c) Ruby
d) COBOL

**Answer:** d
**Reason:** COBOL is not supported. AWS SDKs support **modern languages** like Python (boto3), Java, Go, PHP, Ruby, JavaScript, and C#.

---

## **AWS CLI**

**4. Which command is used to configure AWS CLI with credentials?**
a) aws setup
b) aws login
c) aws configure
d) aws init

**Answer:** c
**Reason:** `aws configure` is used to set **Access Key, Secret Key, Region, and Output format**.

---

**5. Which AWS environment has AWS CLI pre-installed by default?**
a) Windows 11
b) Ubuntu Desktop
c) Amazon Linux 2 AMI
d) macOS Ventura

**Answer:** c
**Reason:** Amazon Linux 2 AMIs come with **AWS CLI preinstalled**, making it easier to manage AWS resources via command line.

---

**6. Which of these is a valid AWS CLI command?**
a) aws list services
b) aws ec2 describe-instances
c) aws get-resources
d) aws view services

**Answer:** b
**Reason:** AWS CLI follows a service → command pattern, e.g., `aws ec2 describe-instances`.

---

## **AWS Management Console**

**7. Which of the following is true about AWS Management Console?**
a) It requires installation on your machine
b) It is a browser-based interface for managing AWS services
c) It can only be accessed using the root user
d) It is used only for billing purposes

**Answer:** b
**Reason:** The Management Console is a **web-based GUI** available in a browser.

---

**8. Which tasks can be done via AWS Management Console?**
a) Launch an EC2 instance
b) Create IAM users
c) Configure S3 buckets
d) All of the above

**Answer:** d
**Reason:** The console provides **GUI access** to almost all AWS services.

---

## **AWS Local Zones**

**9. What is the purpose of AWS Local Zones?**
a) To provide physical AWS hardware on customer premises
b) To bring AWS compute, storage, and services closer to end-users for low-latency applications
c) To replace AWS Regions entirely
d) To act as caching servers for CloudFront

**Answer:** b
**Reason:** Local Zones extend AWS infrastructure **closer to population centers** for single-digit millisecond latency.

---

**10. Where are Amazon EBS snapshots stored when created in Local Zones?**
a) In the Local Zone itself
b) In CloudFront edge locations
c) In the parent AWS Region
d) On customer hardware

**Answer:** c
**Reason:** Snapshots in Local Zones are stored in the **parent Region**, not inside the Local Zone.

---

**11. What is the difference between AWS Local Zones and AWS Wavelength?**
a) Local Zones are for 5G, Wavelength is for low-latency compute
b) Local Zones extend AWS to metro areas, Wavelength integrates with telecom 5G networks
c) Wavelength stores snapshots locally, Local Zones store them in Regions
d) Both are the same

**Answer:** b
**Reason:**

* Local Zones → Bring AWS closer to cities.
* Wavelength → Integrates AWS compute/storage **inside telecom 5G networks**.

---

## **IAM Introduction**

**12. Which of the following best describes AWS IAM?**
a) A service that monitors cloud costs
b) A global service to manage access and authentication in AWS
c) A compute service for running applications
d) A local service only available in certain regions

**Answer:** b
**Reason:** IAM (Identity and Access Management) is a **global service** for controlling user and service access.

---

**13. Which IAM entity should be avoided for daily operations?**
a) IAM Role
b) IAM Group
c) Root User
d) IAM User

**Answer:** c
**Reason:** **Root user has unlimited privileges** and should only be used for initial setup.

---

**14. What is AWS best practice for IAM permissions?**
a) Always use the root user for maximum access
b) Grant the least privileges needed
c) Assign admin access to everyone
d) Avoid enabling MFA

**Answer:** b
**Reason:** AWS follows the **Principle of Least Privilege**.

---

## **IAM Access Management**

**15. What is an IAM Policy?**
a) A collection of EC2 instances
b) A JSON document defining permissions
c) A user group in AWS
d) A service to store encryption keys

**Answer:** b
**Reason:** IAM policies are **JSON documents** that specify permissions with *Effect, Action, Resource, Condition*.

---

**16. Which IAM entity allows AWS services like EC2 to assume permissions?**
a) IAM User
b) IAM Group
c) IAM Role
d) IAM Policy

**Answer:** c
**Reason:** **IAM Roles** can be assumed by **services, users, or applications**.

---

**17. Which of these IAM access controls ensures users only get temporary credentials?**
a) Inline policies
b) Service-linked roles
c) Security Token Service (STS)
d) IAM Groups

**Answer:** c
**Reason:** AWS STS provides **temporary credentials** for IAM roles and federated access.

---

## **IAM Role Creation**

**18. When creating a service role in IAM, who assumes the role?**
a) The AWS root user
b) The AWS service (e.g., EC2, Lambda)
c) An IAM group
d) Only external users

**Answer:** b
**Reason:** Service roles are **assumed by AWS services** to perform actions on behalf of the user.

---

## **IAM Policy Evaluation Logic**

**19. Which statement about IAM policy evaluation is true?**
a) Explicit Deny overrides Allow
b) By default, everything is denied
c) Allow must be explicitly granted
d) All of the above

**Answer:** d
**Reason:** IAM evaluation rules:

* Default = **Deny**
* Explicit **Allow** overrides default Deny
* Explicit **Deny** overrides everything

---

**20. If a user has two policies: one allows S3 access and one explicitly denies it, what will happen?**
a) The user gets access
b) The user is denied
c) Both are applied
d) None of the above

**Answer:** b
**Reason:** **Explicit Deny always overrides Allow**, so the user will be denied.

---

# 🎯 **Recap**

* Total: 20 MCQs
* Covered: **AWS SDK, CLI, Console, Local Zones, IAM (intro, access, roles, policy logic)**
* Each answer includes **reasoning** for better understanding.

---

👉 Do you want me to now create a **“harder scenario-based set” (20 questions)** from the same Module 1 (e.g., “Your EC2 needs S3 access, which IAM entity to use?”) — like exam-style practice?
