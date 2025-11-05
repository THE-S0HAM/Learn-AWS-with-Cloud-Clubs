# 🧹 EC2 Resource Cleanup Guide - Activity 12

<div align="center">

![EC2](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazon-aws)
![Cleanup](https://img.shields.io/badge/Resource-Cleanup-red?style=for-the-badge&logo=trash)
![Beta](https://img.shields.io/badge/Beta-Activity--12-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3o7abAHdYvZdBNnGZq/giphy.gif" width="300" alt="Cleanup">

### 🌟 *Learn Proper Resource Cleanup to Stop Charges* 🌟

</div>

---

## 🎯 Activity Objective

**Properly terminate EC2 resources** to understand cleanup procedures and prevent ongoing charges.

**⏱️ Estimated Time:** 10-15 minutes  
**💰 Cost:** Free (saves money by stopping charges)  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Terminate Instance 🗑️

1. Go to **EC2** → **Instances**
2. Select your web server instance
3. **Actions** → **Instance State** → **Terminate instance**
4. Confirm termination
5. Instance state changes to "shutting-down" then "terminated"

### Step 2: Observe EBS Volume Behavior 👀

1. Go to **EBS** → **Volumes**
2. Find the volume that was attached to your instance
3. Watch the volume state change to "deleting"
4. Volume disappears (due to "Delete on Termination" = true)

### Step 3: Verify Cleanup ✅

1. **EC2 Instances:** Should show "terminated"
2. **EBS Volumes:** Should be deleted automatically
3. **Security Groups:** Remain (can be reused)
4. **Key Pairs:** Remain (can be reused)

---

## ✅ Verification Steps

```bash
Cleanup Verification:
✅ Instance terminated successfully
✅ EBS volume deleted automatically
✅ No running instances in region
✅ No billable resources remaining
```

---

## 🎯 Next Steps

**Proceed to Activity 13:** [RDS Free Tier Setup](../RDS/Guides/rds-free-tier-setup-guide.md)

<div align="center">

### 🎉 *Resource Cleanup Complete!* 🎉

</div>