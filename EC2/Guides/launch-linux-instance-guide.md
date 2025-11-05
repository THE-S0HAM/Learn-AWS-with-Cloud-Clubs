# 🖥️ Launch Linux Instance Guide - Activity 8

<div align="center">

![EC2](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazon-aws)
![Linux](https://img.shields.io/badge/Linux-Instance-blue?style=for-the-badge&logo=linux)
![Beta](https://img.shields.io/badge/Beta-Activity--8-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPEqDGUULpEU0aQ/giphy.gif" width="300" alt="Server Launch">

### 🌟 *Launch Your First Virtual Server in the Cloud* 🌟

</div>

---

## 🎯 Activity Objective

**Launch a t2.micro EC2 instance** and create a key pair for secure access, understanding the fundamentals of cloud computing.

**⏱️ Estimated Time:** 15-20 minutes  
**💰 Cost:** Free (Free Tier eligible)  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Launch Instance 🚀

1. Go to **EC2 Console**
2. Click **"Launch Instance"** button

### Step 2: Configure Instance 🔧

#### 2.1 Name and AMI
- **Name:** `Beta50-Web-Server`
- **AMI:** Select **Amazon Linux 2023** (Free tier eligible)

#### 2.2 Instance Type
- Select **t2.micro** (Free tier eligible)

#### 2.3 Key Pair
1. Click **"Create new key pair"**
2. **Name:** `beta50-key`
3. **Type:** RSA
4. **Format:** .pem
5. Click **"Create key pair"**
6. **Save the downloaded file securely**

#### 2.4 Launch
- Leave other settings as default
- Click **"Launch instance"**

---

## ✅ Verification Steps

```bash
Instance Verification:
✅ Instance appears in EC2 Dashboard
✅ Status shows "Running"
✅ Instance type is t2.micro
✅ Key pair file downloaded and saved
```

---

## 🎯 Next Steps

**Proceed to Activity 9:** [Security Group Configuration](./security-group-config-guide.md)

<div align="center">

### 🎉 *Great! Your First EC2 Instance is Running!* 🎉

</div>