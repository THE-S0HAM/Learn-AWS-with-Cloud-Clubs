# 🛡️ Security Group Configuration Guide - Activity 9

<div align="center">

![EC2](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazon-aws)
![Security](https://img.shields.io/badge/Security-Groups-red?style=for-the-badge&logo=shield)
![Beta](https://img.shields.io/badge/Beta-Activity--9-green?style=for-the-badge)

<img src="https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif" width="300" alt="Security">

### 🌟 *Configure Firewall Rules for Your Instance* 🌟

</div>

---

## 🎯 Activity Objective

**Configure Security Group rules** to control inbound traffic to your EC2 instance using AWS's stateful firewall.

**⏱️ Estimated Time:** 10-15 minutes  
**💰 Cost:** Free  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Find Security Group 🔍

1. Go to **EC2 Console** → **Instances**
2. Select your `Beta50-Web-Server`
3. Click **Security** tab below
4. Click the security group link (e.g., `launch-wizard-1`)

### Step 2: Edit Inbound Rules 📝

1. Click **"Edit inbound rules"**
2. Click **"Add rule"**

### Step 3: Add HTTP Rule 🌐

- **Type:** HTTP
- **Port:** 80
- **Source:** Anywhere (0.0.0.0/0)

### Step 4: Add SSH Rule 🔐

- **Type:** SSH
- **Port:** 22
- **Source:** My IP

### Step 5: Save Rules ✅

1. Click **"Save rules"**
2. Rules are applied immediately

---

## ✅ Verification Steps

```bash
Security Group Verification:
✅ HTTP (80) rule added for 0.0.0.0/0
✅ SSH (22) rule added for My IP
✅ Rules saved successfully
✅ Instance accessible on port 80
```

---

## 🎯 Next Steps

**Proceed to Activity 10:** [User Data Web Server](./user-data-web-server-guide.md)

<div align="center">

### 🎉 *Security Configuration Complete!* 🎉

</div>