# 🚀 User Data Web Server Guide - Activity 10

<div align="center">

![EC2](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazon-aws)
![Automation](https://img.shields.io/badge/User-Data-blue?style=for-the-badge&logo=script)
![Beta](https://img.shields.io/badge/Beta-Activity--10-green?style=for-the-badge)

<img src="https://media.giphy.com/media/26tn33aiTi1jkl6H6/giphy.gif" width="300" alt="Automation">

### 🌟 *Automate Instance Configuration with User Data* 🌟

</div>

---

## 🎯 Activity Objective

**Use User Data script** to automatically configure an EC2 instance on launch, installing and configuring a web server.

**⏱️ Estimated Time:** 15-20 minutes  
**💰 Cost:** Free (Free Tier eligible)  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Terminate Old Instance 🗑️

1. Go to EC2 → Instances
2. Select `Beta50-Web-Server`
3. **Actions** → **Instance State** → **Terminate instance**

### Step 2: Launch New Instance 🆕

1. Click **"Launch Instance"**
2. **Name:** `Beta50-Web-Server`
3. **AMI:** Amazon Linux 2023
4. **Instance Type:** t2.micro
5. **Key Pair:** Use existing `beta50-key`

### Step 3: Add User Data Script 📝

1. Expand **"Advanced details"** section
2. Scroll to **"User data"** field
3. Paste this script:

```bash
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "Hello from Beta 50 (Instance ID: $(curl -s http://169.254.169.254/latest/meta-data/instance-id))" > /var/www/html/index.html
```

### Step 4: Configure Security 🔒

1. In **Network settings**, select **"Select existing security group"**
2. Choose the security group from Activity 9
3. Click **"Launch instance"**

### Step 5: Test Website 🌐

1. Wait for instance to be **"Running"**
2. Copy **Public IPv4 address**
3. Open in browser: `http://YOUR-PUBLIC-IP`
4. You should see: "Hello from Beta 50 (Instance ID: i-xxxxx)"

---

## ✅ Verification Steps

```bash
Automation Verification:
✅ Instance launched with User Data
✅ Web server installed automatically
✅ Website accessible via public IP
✅ Page shows "Hello from Beta 50" message
✅ Instance ID displayed correctly
```

---

## 🎯 Next Steps

**Proceed to Activity 11:** [EBS Volume Identification](../EBS/Guides/ebs-volume-identification-guide.md)

<div align="center">

### 🎉 *Automation Success! Your Web Server is Live!* 🎉

</div>