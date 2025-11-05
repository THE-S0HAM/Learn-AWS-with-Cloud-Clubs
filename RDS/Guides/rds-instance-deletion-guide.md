# 🗑️ RDS Instance Deletion Guide - Activity 14

<div align="center">

![RDS](https://img.shields.io/badge/AWS-RDS-orange?style=for-the-badge&logo=amazon-aws)
![Cleanup](https://img.shields.io/badge/Database-Cleanup-red?style=for-the-badge&logo=trash)
![Beta](https://img.shields.io/badge/Beta-Activity--14-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3o7abAHdYvZdBNnGZq/giphy.gif" width="300" alt="Database Cleanup">

### 🌟 *Clean Up Database Resources* 🌟

</div>

---

## 🎯 Activity Objective

**Delete RDS database instance** to understand proper database cleanup and prevent ongoing charges.

**⏱️ Estimated Time:** 10-15 minutes  
**💰 Cost:** Free (saves money by stopping charges)  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Select Database 🎯

1. Go to **RDS Console** → **Databases**
2. Select your `beta50-db` database

### Step 2: Delete Database 🗑️

1. Click **"Actions"** menu
2. Select **"Delete"**

### Step 3: Configure Deletion Options ⚙️

1. **Deselect** "Create final snapshot?" (this is a test database)
2. **Deselect** "Retain automated backups"
3. **Check** "I acknowledge that upon instance deletion..."
4. Type `delete me` in the confirmation field
5. Click **"Delete"**

### Step 4: Monitor Deletion 👀

1. Database status changes to "Deleting"
2. Process takes 5-10 minutes
3. Database disappears from list when complete

---

## ✅ Verification Steps

```bash
RDS Cleanup Verification:
✅ Database deletion initiated
✅ Status shows "Deleting"
✅ Database removed from list
✅ No billable RDS resources remaining
```

---

## 🎯 Next Steps

**Proceed to Activity 15:** [Lambda Hello World](../Lambda/Guides/lambda-hello-world-guide.md)

<div align="center">

### 🎉 *Database Cleanup Complete!* 🎉

</div>