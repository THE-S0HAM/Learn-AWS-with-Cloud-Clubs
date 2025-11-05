# 🗄️ RDS Free Tier Setup Guide - Activity 13

<div align="center">

![RDS](https://img.shields.io/badge/AWS-RDS-orange?style=for-the-badge&logo=amazon-aws)
![Database](https://img.shields.io/badge/MySQL-Database-blue?style=for-the-badge&logo=mysql)
![Beta](https://img.shields.io/badge/Beta-Activity--13-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPEqDGUULpEU0aQ/giphy.gif" width="300" alt="Database">

### 🌟 *Launch Managed Database Service* 🌟

</div>

---

## 🎯 Activity Objective

**Launch a Free Tier RDS MySQL database** to understand managed database services vs. self-managed databases.

**⏱️ Estimated Time:** 15-20 minutes  
**💰 Cost:** Free (Free Tier eligible)  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Navigate to RDS 🗄️

1. Go to **RDS Console**
2. Click **"Create database"**

### Step 2: Configure Database 🔧

#### 2.1 Creation Method
- Select **"Standard Create"**

#### 2.2 Engine Options
- Select **"MySQL"**

#### 2.3 Templates
- Select **"Free tier"** (automatically limits options)

#### 2.4 Settings
- **DB instance identifier:** `beta50-db`
- **Master username:** `admin`
- **Master password:** Create secure password (save it!)

#### 2.5 Connectivity
- Expand **"Connectivity"** section
- Set **"Public access"** to **"Yes"** (for testing only)

### Step 3: Create Database 🚀

1. Click **"Create database"**
2. Creation takes 5-10 minutes
3. Status changes from "Creating" to "Available"

### Step 4: Note Connection Details 📝

Once available, note:
- **Endpoint:** Database connection URL
- **Port:** 3306 (MySQL default)
- **Username:** admin
- **Password:** Your chosen password

---

## ✅ Verification Steps

```bash
RDS Verification:
✅ Database status shows "Available"
✅ Endpoint URL is provided
✅ Free tier template was used
✅ MySQL engine selected
✅ Public access enabled for testing
```

---

## 🎯 Next Steps

**Proceed to Activity 14:** [RDS Instance Deletion](./rds-instance-deletion-guide.md)

<div align="center">

### 🎉 *Managed Database Successfully Created!* 🎉

</div>