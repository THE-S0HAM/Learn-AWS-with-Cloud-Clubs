# 💾 EBS Volume Identification Guide - Activity 11

<div align="center">

![EBS](https://img.shields.io/badge/AWS-EBS-orange?style=for-the-badge&logo=amazon-aws)
![Storage](https://img.shields.io/badge/Block-Storage-blue?style=for-the-badge&logo=database)
![Beta](https://img.shields.io/badge/Beta-Activity--11-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPnAiaMCws8nOsE/giphy.gif" width="300" alt="Storage">

### 🌟 *Understand EC2 Instance Storage with EBS* 🌟

</div>

---

## 🎯 Activity Objective

**Identify and examine your EC2 instance's root volume** to understand how EBS provides persistent block storage.

**⏱️ Estimated Time:** 10-15 minutes  
**💰 Cost:** Free  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Select Instance 🖥️

1. Go to **EC2 Console** → **Instances**
2. Select your running web server instance

### Step 2: Find Storage Information 💾

1. Click the **"Storage"** tab below
2. You'll see a Volume ID (e.g., `vol-0abc123def456789`)
3. Note the volume details

### Step 3: View EBS Volume 🔍

1. Click the **Volume ID** link
2. This opens the **EBS Console**
3. Examine the volume properties:
   - **Size:** 8 GiB (default)
   - **Volume type:** gp3 (General Purpose SSD)
   - **State:** in-use
   - **Attached to:** Your instance ID

### Step 4: Understand Volume Properties 📊

```yaml
EBS Volume Details:
  Size: 8 GiB (default root volume)
  Type: gp3 (General Purpose SSD)
  State: in-use
  Availability Zone: Same as instance
  Encrypted: Yes (default)
  Delete on Termination: Yes (default)
```

---

## ✅ Verification Steps

```bash
EBS Volume Verification:
✅ Volume ID identified in EC2 Storage tab
✅ Volume visible in EBS console
✅ Volume attached to correct instance
✅ Volume properties understood
✅ Volume state shows "in-use"
```

---

## 🎯 Next Steps

**Proceed to Activity 12:** [EC2 Resource Cleanup](./ec2-resource-cleanup-guide.md)

<div align="center">

### 🎉 *EBS Storage Concepts Mastered!* 🎉

</div>