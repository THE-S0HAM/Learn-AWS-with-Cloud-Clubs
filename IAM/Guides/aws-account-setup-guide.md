# 🏗️ AWS Account Setup Guide - Activity 1

<div align="center">

![AWS](https://img.shields.io/badge/AWS-Account--Setup-orange?style=for-the-badge&logo=amazon-aws)
![Security](https://img.shields.io/badge/Security-MFA-red?style=for-the-badge&logo=shield)
![Beta](https://img.shields.io/badge/Beta-Activity--1-blue?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPEqDGUULpEU0aQ/giphy.gif" width="300" alt="Setup Animation">

### 🌟 *Establish Your Learning Environment & Secure Root User* 🌟

</div>

---

## 🎯 Activity Objective

**Establish your learning environment and secure the root user** by creating a new AWS account and implementing security best practices from day one.

**⏱️ Estimated Time:** 15-20 minutes  
**💰 Cost:** Free (requires credit card for verification)  
**🔧 Difficulty:** Beginner

---

## 📋 Prerequisites

- Valid email address
- Credit card (for account verification - you'll stay within Free Tier)
- Mobile phone (for MFA setup)
- Smartphone with authenticator app capability

---

## 🚀 Step-by-Step Instructions

### Step 1: Create AWS Account 🆕

<div align="center">
<img src="https://media.giphy.com/media/26tn33aiTi1jkl6H6/giphy.gif" width="200" alt="Account Creation">
</div>

#### 1.1 Navigate to AWS
```bash
# Visit the AWS website
URL: https://aws.amazon.com/
```

#### 1.2 Start Account Creation
1. Click **"Create an AWS Account"** button
2. Enter your **email address**
3. Choose an **AWS account name** (e.g., "YourName-Learning-Account")
4. Click **"Continue"**

#### 1.3 Complete Registration
```yaml
Required Information:
  Contact Type: Personal
  Full Name: [Your Full Name]
  Phone Number: [Your Phone Number]
  Country/Region: [Your Country]
  Address: [Your Complete Address]
  City: [Your City]
  State/Province: [Your State]
  Postal Code: [Your Postal Code]
```

#### 1.4 Payment Information
- Enter credit card details (required for verification)
- **Note:** You won't be charged if you stay within Free Tier limits
- AWS may place a $1 temporary authorization (refunded automatically)

#### 1.5 Identity Verification
- Choose **Text message (SMS)** or **Voice call**
- Enter the verification code received
- Click **"Continue"**

#### 1.6 Select Support Plan
- Choose **"Basic support - Free"**
- Click **"Complete sign up"**

---

### Step 2: Secure Root User with MFA 🔒

<div align="center">
<img src="https://media.giphy.com/media/ZVik7pBtu9dNS/giphy.gif" width="200" alt="Security">
</div>

#### 2.1 Sign In as Root User
1. Go to [AWS Management Console](https://console.aws.amazon.com/)
2. Click **"Sign in to the Console"**
3. Select **"Root user"**
4. Enter your email address and password

#### 2.2 Navigate to Security Credentials
```bash
# Once logged in:
1. Click your account name (top-right corner)
2. Select "Security credentials" from dropdown
3. You'll be redirected to IAM dashboard
```

#### 2.3 Enable MFA for Root User
1. In the **"Multi-factor authentication (MFA)"** section
2. Click **"Assign MFA device"**
3. Choose **"Virtual MFA device"**
4. Click **"Continue"**

#### 2.4 Set Up Virtual MFA Device
```markdown
Recommended Authenticator Apps:
- Google Authenticator (iOS/Android)
- Microsoft Authenticator (iOS/Android)
- Authy (iOS/Android/Desktop)
```

**Setup Process:**
1. Install authenticator app on your smartphone
2. In AWS console, click **"Show QR code"**
3. Scan QR code with your authenticator app
4. Enter two consecutive MFA codes from your app
5. Click **"Assign MFA"**

---

### Step 3: Create Account Alias 🏷️

<div align="center">
<img src="https://media.giphy.com/media/3o7abAHdYvZdBNnGZq/giphy.gif" width="150" alt="Customization">
</div>

#### 3.1 Navigate to IAM Dashboard
1. In AWS Console, search for **"IAM"**
2. Click on **"IAM"** service
3. You'll see the IAM Dashboard

#### 3.2 Create Custom Account Alias
1. In the IAM Dashboard, find **"AWS Account"** section
2. Next to **"Account Alias"**, click **"Create"**
3. Enter a unique alias (e.g., `yourname-beta50`)
4. Click **"Create alias"**

**Alias Requirements:**
- 3-63 characters long
- Only lowercase letters, numbers, and hyphens
- Must be globally unique across all AWS accounts

---

## ✅ Verification Steps

### 🔍 Verify Account Setup

```bash
# Check these items:
✅ AWS account created successfully
✅ Email verification completed
✅ Payment method added and verified
✅ Account is active and accessible
```

### 🔒 Verify MFA Setup

```bash
# Test MFA:
1. Sign out of AWS Console
2. Sign back in as root user
3. Confirm you're prompted for MFA code
4. Enter code from authenticator app
5. Successfully access console
```

### 🏷️ Verify Account Alias

```bash
# Check alias:
1. Go to IAM Dashboard
2. Confirm custom alias is displayed
3. Note the sign-in URL format:
   https://[your-alias].signin.aws.amazon.com/console
```

---

## 🛡️ Security Best Practices

### ✅ Immediate Actions
- **Never share root credentials**
- **Use MFA on all accounts**
- **Create IAM users for daily tasks**
- **Enable CloudTrail logging**
- **Set up billing alerts**

### 🚨 Security Warnings
```yaml
Critical Security Rules:
  - Root user is for emergencies only
  - Always use MFA
  - Never hardcode credentials
  - Regularly rotate access keys
  - Monitor account activity
```

---

## 💰 Cost Management

### 🆓 Free Tier Benefits
```yaml
AWS Free Tier Includes:
  EC2: 750 hours/month (t2.micro)
  S3: 5 GB storage
  RDS: 750 hours/month (db.t2.micro)
  Lambda: 1M requests/month
  CloudWatch: 10 custom metrics
```

### 📊 Monitoring Costs
- Set up billing alerts (covered in Activity 6)
- Check AWS Free Tier usage regularly
- Use AWS Cost Explorer for detailed analysis

---

## 🔧 Troubleshooting

### ❌ Common Issues

#### Issue: Credit Card Declined
```bash
Solutions:
- Contact your bank to authorize international transactions
- Try a different credit card
- Ensure billing address matches card details
- Wait 24 hours and try again
```

#### Issue: MFA Setup Fails
```bash
Solutions:
- Ensure phone time is synchronized
- Try different authenticator app
- Check internet connection
- Clear browser cache and cookies
```

#### Issue: Account Alias Already Taken
```bash
Solutions:
- Try variations: yourname-beta50-2024
- Add numbers or location: yourname-mumbai-beta50
- Use underscores: your_name_beta50
```

---

## 📚 Additional Resources

### 🔗 Helpful Links
- [AWS Account Setup Documentation](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html)
- [MFA Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_mfa.html)
- [AWS Free Tier Details](https://aws.amazon.com/free/)

### 📱 Recommended Apps
- [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)
- [Microsoft Authenticator](https://www.microsoft.com/en-us/security/mobile-authenticator-app)
- [Authy](https://authy.com/)

---

## 🎯 Next Steps

After completing this activity:

1. ✅ **Proceed to Activity 2:** [IAM User & MFA Setup](./iam-user-mfa-setup-guide.md)
2. 📚 **Bookmark AWS Console:** Add to browser favorites
3. 📱 **Test MFA:** Practice signing in with MFA
4. 💾 **Save Credentials:** Store in secure password manager

---

## 🆘 Need Help?

### 📞 Support Channels
- **Discord:** Beta 50 Batch Channel
- **Email:** awscloudclubscoe@yahoo.com
- **Office Hours:** Tuesday/Thursday 4-5 PM IST

### 🤔 Common Questions
**Q: Will I be charged for creating an account?**  
A: No, account creation is free. You only pay for resources you use beyond Free Tier limits.

**Q: Can I use a debit card instead of credit card?**  
A: Yes, most debit cards with international transaction capability work.

**Q: What if I lose access to my MFA device?**  
A: Contact AWS Support with account verification details to reset MFA.

---

<div align="center">

### 🎉 *Congratulations! Your AWS Account is Ready!* 🎉

**You've successfully completed Activity 1 of the Beta 50 Program!**

<img src="https://media.giphy.com/media/3o7abKhOpu0NwenH3O/giphy.gif" width="150" alt="Success">

**Next: Activity 2 - IAM User & MFA Setup**

</div>