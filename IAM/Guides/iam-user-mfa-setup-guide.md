# 🔐 IAM User & MFA Setup Guide - Activity 2

<div align="center">

![IAM](https://img.shields.io/badge/AWS-IAM-red?style=for-the-badge&logo=amazon-aws)
![Security](https://img.shields.io/badge/Security-MFA-green?style=for-the-badge&logo=shield)
![Beta](https://img.shields.io/badge/Beta-Activity--2-blue?style=for-the-badge)

<img src="https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif" width="300" alt="Security Animation">

### 🌟 *Implement Least Privilege with Administrative IAM User* 🌟

</div>

---

## 🎯 Activity Objective

**Create a non-root administrative user for daily use** following AWS security best practice of "least privilege" and never using root account for routine tasks.

**⏱️ Estimated Time:** 15-20 minutes  
**💰 Cost:** Free  
**🔧 Difficulty:** Beginner

---

## 📋 Prerequisites

- ✅ AWS Account with root user MFA enabled (Activity 1 completed)
- ✅ Access to AWS Management Console as root user
- ✅ Smartphone with authenticator app

---

## 🚀 Step-by-Step Instructions

### Step 1: Create IAM Group 👥

#### 1.1 Navigate to IAM Console
1. Sign in as **root user**
2. Search for **"IAM"** in services
3. Click on **"IAM"** service
4. You'll see the IAM Dashboard

#### 1.2 Create Administrative Group
1. In left navigation, click **"User groups"**
2. Click **"Create group"** button
3. **Group name:** `Beta50_Admins`
4. **Description:** `Administrative group for Beta 50 batch learners`

#### 1.3 Attach Administrative Policy
1. In **"Attach permissions policies"** section
2. Search for **"AdministratorAccess"**
3. Check the box next to **"AdministratorAccess"** policy
4. Click **"Create group"**

```yaml
AdministratorAccess Policy:
  Description: Provides full access to AWS services and resources
  Use Case: Administrative users who need complete access
  Security Note: Use carefully - provides extensive permissions
```

---

### Step 2: Create IAM User 👤

<div align="center">
<img src="https://media.giphy.com/media/26tn33aiTi1jkl6H6/giphy.gif" width="200" alt="User Creation">
</div>

#### 2.1 Start User Creation
1. In left navigation, click **"Users"**
2. Click **"Create user"** button

#### 2.2 Configure User Details
```yaml
User Configuration:
  User name: [yourname]-Daily-Admin
  Example: john-Daily-Admin
  
Access Type:
  ✅ Provide user access to AWS Management Console
  Console password: Custom password (create strong password)
  ✅ User must create a new password at next sign-in
```

**Step-by-step:**
1. **User name:** Enter `[yourname]-Daily-Admin`
2. Check **"Provide user access to the AWS Management Console"**
3. Select **"Custom password"**
4. Enter a strong password (save it securely)
5. **Uncheck** "User must create new password" (for convenience)
6. Click **"Next"**

#### 2.3 Add User to Group
1. Select **"Add user to group"**
2. Check the box next to **"Beta50_Admins"**
3. Click **"Next"**
4. Review settings and click **"Create user"**

---

### Step 3: Test IAM User Login 🧪

#### 3.1 Get Sign-in Information
1. After user creation, note the **Console sign-in URL**
2. Format: `https://[account-alias].signin.aws.amazon.com/console`
3. **Save this URL** - you'll use it for daily access

#### 3.2 Sign Out and Test Login
1. **Sign out** of root user account
2. Open new browser tab/window
3. Go to the console sign-in URL
4. **Account ID:** Your account alias or ID
5. **IAM user name:** `[yourname]-Daily-Admin`
6. **Password:** The password you created
7. Click **"Sign in"**

---

### Step 4: Enable MFA for IAM User 🔒

<div align="center">
<img src="https://media.giphy.com/media/3o7abAHdYvZdBNnGZq/giphy.gif" width="150" alt="MFA Setup">
</div>

#### 4.1 Access Security Credentials
1. **While signed in as IAM user**, click your username (top-right)
2. Select **"Security credentials"**
3. Scroll to **"Multi-factor authentication (MFA)"** section

#### 4.2 Assign MFA Device
1. Click **"Assign MFA device"**
2. **Device name:** `[yourname]-phone-mfa`
3. **MFA device:** Select **"Authenticator app"**
4. Click **"Next"**

#### 4.3 Configure Authenticator App
1. Open authenticator app on your phone
2. Click **"Show QR code"** in AWS console
3. Scan QR code with your app
4. Enter **two consecutive MFA codes** from app
5. Click **"Add MFA"**

---

## ✅ Verification Steps

### 🔍 Verify Group Creation

```bash
Group Verification:
✅ Beta50_Admins group exists
✅ AdministratorAccess policy attached
✅ Group shows in IAM dashboard
✅ Policy permissions are correct
```

### 👤 Verify User Creation

```bash
User Verification:
✅ IAM user created successfully
✅ User is member of Beta50_Admins group
✅ Console access enabled
✅ User can sign in with password
```

### 🔒 Verify MFA Setup

```bash
MFA Verification:
1. Sign out of IAM user account
2. Sign back in with same credentials
3. ✅ System prompts for MFA code
4. Enter code from authenticator app
5. ✅ Successfully access console
```

---

## 🛡️ Security Best Practices

### ✅ IAM Security Fundamentals

```yaml
Security Principles:
  ✅ Least Privilege: Grant minimum required permissions
  ✅ MFA Everywhere: Enable on all accounts
  ✅ Strong Passwords: Use complex, unique passwords
  ✅ Regular Reviews: Audit permissions periodically
  ✅ No Root Usage: Use root only for emergencies
```

### 🚨 Critical Security Rules

```markdown
Never Do This:
❌ Don't use root account for daily tasks
❌ Don't share IAM user credentials
❌ Don't disable MFA once enabled
❌ Don't use overly broad permissions
❌ Don't ignore security recommendations
```

---

## 🔧 Troubleshooting

### ❌ Common Issues

#### Issue: Can't Create Group
```bash
Possible Causes:
- Not signed in as root user
- Insufficient permissions
- Group name already exists

Solutions:
✅ Ensure you're using root account
✅ Try different group name
✅ Check IAM service availability
```

#### Issue: User Login Fails
```bash
Common Problems:
- Wrong sign-in URL
- Incorrect username format
- Password issues
- Account ID confusion

Solutions:
✅ Use correct console URL format
✅ Verify username exactly as created
✅ Reset password if needed
✅ Check account alias/ID
```

#### Issue: MFA Setup Fails
```bash
Troubleshooting Steps:
✅ Ensure phone time is synchronized
✅ Try different authenticator app
✅ Check internet connectivity
✅ Clear browser cache
✅ Use incognito/private browsing
```

---

## 📚 Understanding IAM Concepts

### 👥 Groups vs Users vs Roles

```yaml
IAM Components:
  Users:
    - Individual identities
    - Long-term credentials
    - For human access
    
  Groups:
    - Collections of users
    - Simplify permission management
    - Apply policies to multiple users
    
  Roles:
    - Temporary credentials
    - For services or cross-account access
    - No permanent credentials
```

### 📋 Policies and Permissions

```yaml
Policy Types:
  AWS Managed:
    - Created and maintained by AWS
    - Example: AdministratorAccess
    - Regularly updated by AWS
    
  Customer Managed:
    - Created by you
    - Customizable for specific needs
    - You maintain and update
    
  Inline Policies:
    - Attached directly to user/group/role
    - One-to-one relationship
    - Not reusable
```

---

## 💡 Advanced Tips

### 🎯 Permission Management

```yaml
Best Practices:
  Start Small: Begin with minimal permissions
  Add Gradually: Increase permissions as needed
  Use Groups: Manage permissions via groups
  Regular Audits: Review permissions quarterly
  Document Changes: Keep track of permission changes
```

### 🔄 Account Management

```yaml
Daily Operations:
  ✅ Always use IAM user (never root)
  ✅ Enable MFA on all accounts
  ✅ Use strong, unique passwords
  ✅ Monitor account activity
  ✅ Keep credentials secure
```

---

## 🎯 Next Steps

After completing this activity:

1. ✅ **Proceed to Activity 3:** [S3 Bucket Creation](../S3/Guides/s3-bucket-creation-guide.md)
2. 🔖 **Bookmark IAM User Sign-in URL:** Save for daily use
3. 🔒 **Store Credentials Securely:** Use password manager
4. 📱 **Test MFA:** Practice signing in with MFA

---

## 🆘 Need Help?

### 📞 Support Channels
- **Discord:** Beta 50 Batch Channel
- **Email:** awscloudclubscoe@yahoo.com
- **Office Hours:** Tuesday/Thursday 4-5 PM IST

### 🤔 Common Questions

**Q: Should I ever use the root account again?**  
A: Only for specific tasks that require root access (billing, account closure, etc.).

**Q: Can I create multiple IAM users?**  
A: Yes, create separate users for different people or purposes.

**Q: What if I lose access to my MFA device?**  
A: Contact AWS Support with account verification to reset MFA.

**Q: Can I change the group permissions later?**  
A: Yes, you can modify group policies anytime.

---

## 📖 Additional Learning

### 🔗 Helpful Resources
- [IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS Security Blog](https://aws.amazon.com/blogs/security/)

### 🎓 Advanced Topics (Future Learning)
- IAM Roles and Assume Role
- Cross-Account Access
- IAM Access Analyzer
- AWS Organizations
- Service Control Policies (SCPs)

---

<div align="center">

### 🎉 *Excellent! Your IAM Security is Now Configured!* 🎉

**You've successfully completed Activity 2 of the Beta 50 Program!**

<img src="https://media.giphy.com/media/3o7abKhOpu0NwenH3O/giphy.gif" width="150" alt="Success">

**Next: Activity 3 - S3 Bucket Creation**

</div>