# 🌍 Region & AZ Exploration Guide - Activity 7

<div align="center">

![EC2](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazon-aws)
![Global](https://img.shields.io/badge/Global-Infrastructure-blue?style=for-the-badge&logo=globe)
![Beta](https://img.shields.io/badge/Beta-Activity--7-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPnAiaMCws8nOsE/giphy.gif" width="300" alt="Global Network">

### 🌟 *Understand AWS Global Infrastructure: Regions & Availability Zones* 🌟

</div>

---

## 🎯 Activity Objective

**Visually understand the relationship between AWS Regions and Availability Zones** and learn how AWS's global infrastructure provides high availability and fault tolerance.

**⏱️ Estimated Time:** 10-15 minutes  
**💰 Cost:** Free  
**🔧 Difficulty:** Beginner

---

## 📋 Prerequisites

- ✅ AWS Account with IAM user access (Activities 1-2 completed)
- ✅ Basic understanding of geographic concepts
- ✅ Access to AWS Management Console

---

## 🚀 Step-by-Step Instructions

### Step 1: Check Regions 🌐

#### 1.1 Access Region Selector
1. Sign in to **AWS Management Console** (as IAM user)
2. Look at the **top-right corner** of the console
3. Find the **region selector** (shows current region)
4. Click on the region selector dropdown

#### 1.2 Examine Region List
**Document these major regions:**
```yaml
Popular AWS Regions:
  North America:
    - us-east-1: N. Virginia (Default region)
    - us-west-2: Oregon
  
  Europe:
    - eu-west-1: Ireland
    - eu-central-1: Frankfurt
  
  Asia Pacific:
    - ap-south-1: Mumbai
    - ap-southeast-1: Singapore
```

---

### Step 2: Navigate to EC2 Console 🖥️

#### 2.1 Open EC2 Service
1. In the services search bar, type **"EC2"**
2. Click on **"EC2"** service
3. You'll see the EC2 Dashboard

#### 2.2 Check Service Health
1. On the EC2 Dashboard, look for **"Service Health"** section
2. Note the AZs listed for your current region (e.g., `ap-south-1a`, `ap-south-1b`)

---

### Step 3: View AZs via Launch Instance 🚀

#### 3.1 Start Instance Launch Process
1. Click **"Launch Instance"** button
2. Scroll down to **"Network settings"** section
3. Look for the **"Subnet"** dropdown
4. Click on the **Subnet dropdown** to expand it

#### 3.2 Analyze Subnet-AZ Mapping
**You'll see entries like:**
```yaml
Subnet Format:
  subnet-xxxxxxxx (us-east-1a) | Default in us-east-1a
  subnet-yyyyyyyy (us-east-1b) | Default in us-east-1b
```

#### 3.3 Cancel Instance Launch
1. **Don't proceed with launching** - this is just exploration
2. Click **"Cancel"** or navigate away from the page

---

## ✅ Verification Steps

### 📝 Answer This Question

**How many Availability Zones are in your default region?**

Write your answer: ________________

**Common Answers:**
- us-east-1: 6 AZs
- us-west-2: 4 AZs
- ap-south-1: 3 AZs
- eu-west-1: 3 AZs

---

## 🎯 Next Steps

After completing this activity:

1. ✅ **Proceed to Activity 8:** [Launch Linux Instance](./launch-linux-instance-guide.md)
2. 🌍 **Explore More Regions:** Switch between different regions
3. 📊 **Compare Services:** Note service availability differences

---

<div align="center">

### 🎉 *Great! You Understand AWS Global Infrastructure!* 🎉

**You've successfully completed Activity 7 of the Beta 50 Program!**

<img src="https://media.giphy.com/media/3o7abKhOpu0NwenH3O/giphy.gif" width="150" alt="Success">

**Next: Activity 8 - Launch Linux Instance**

</div>