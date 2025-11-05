# 🏗️ CloudFormation S3 Deploy Guide - Activity 17

<div align="center">

![CloudFormation](https://img.shields.io/badge/AWS-CloudFormation-orange?style=for-the-badge&logo=amazon-aws)
![IaC](https://img.shields.io/badge/Infrastructure-as--Code-blue?style=for-the-badge&logo=code)
![Beta](https://img.shields.io/badge/Beta-Activity--17-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPEqDGUULpEU0aQ/giphy.gif" width="300" alt="Infrastructure">

### 🌟 *Deploy Infrastructure as Code* 🌟

</div>

---

## 🎯 Activity Objective

**Deploy S3 bucket using CloudFormation** to understand Infrastructure as Code (IaC) concepts.

**⏱️ Estimated Time:** 15-20 minutes  
**💰 Cost:** Free  
**🔧 Difficulty:** Beginner

---

## 🚀 Step-by-Step Instructions

### Step 1: Navigate to CloudFormation 🏗️

1. Go to **CloudFormation Console**
2. Click **"Create stack"** → **"With new resources (standard)"**

### Step 2: Choose Template 📄

1. **Prepare template:** Select **"Template is ready"**
2. **Template source:** Select **"Sample templates"**
3. Choose **"S3 bucket"** sample template
4. Click **"Next"**

### Step 3: Specify Stack Details 📝

1. **Stack name:** `beta50-s3-stack`
2. Leave parameters as default
3. Click **"Next"**

### Step 4: Configure Stack Options ⚙️

1. Leave all options as default
2. Click **"Next"**

### Step 5: Review and Create ✅

1. Review all settings
2. Click **"Create stack"**
3. Stack creation begins

### Step 6: Monitor Creation 👀

1. Watch stack status change from `CREATE_IN_PROGRESS` to `CREATE_COMPLETE`
2. Process takes 2-3 minutes

### Step 7: Verify S3 Bucket 🪣

1. Go to **S3 Console**
2. Verify new bucket exists (name like `beta50-s3-stack-...`)

---

## ✅ Verification Steps

```bash
CloudFormation Verification:
✅ Stack created successfully
✅ Status shows "CREATE_COMPLETE"
✅ S3 bucket created via template
✅ Resources managed by CloudFormation
```

---

## 🎯 Next Steps

**Proceed to Activity 18:** [CloudFormation Stack Cleanup](./cloudformation-cleanup-guide.md)

<div align="center">

### 🎉 *Infrastructure as Code Deployed!* 🎉

</div>