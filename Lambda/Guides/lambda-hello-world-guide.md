# ⚡ Lambda Hello World Guide - Activity 15

<div align="center">

![Lambda](https://img.shields.io/badge/AWS-Lambda-orange?style=for-the-badge&logo=amazon-aws)
![Serverless](https://img.shields.io/badge/Serverless-Computing-blue?style=for-the-badge&logo=server)
![Beta](https://img.shields.io/badge/Beta-Activity--15-green?style=for-the-badge)

<img src="https://media.giphy.com/media/3oKIPnAiaMCws8nOsE/giphy.gif" width="300" alt="Serverless Animation">

### 🌟 *Run Code Without Managing Servers* 🌟

</div>

---

## 🎯 Activity Objective

**Create and test a simple Lambda function** to understand serverless computing concepts and experience running code without provisioning or managing servers.

**⏱️ Estimated Time:** 10-15 minutes  
**💰 Cost:** Free (within Free Tier limits)  
**🔧 Difficulty:** Beginner

---

## 📋 Prerequisites

- ✅ AWS Account with IAM user access (Activities 1-2 completed)
- ✅ Basic understanding of programming concepts
- ✅ Access to AWS Management Console

---

## 🚀 Step-by-Step Instructions

### Step 1: Navigate to Lambda Console ⚡

#### 1.1 Open Lambda Service
1. Sign in to **AWS Management Console** (as IAM user)
2. In the services search bar, type **"Lambda"**
3. Click on **"Lambda"** service
4. You'll see the Lambda dashboard

---

### Step 2: Create Lambda Function 📝

#### 2.1 Start Function Creation
1. Click **"Create function"** button
2. Select **"Author from scratch"** (default option)

#### 2.2 Configure Basic Settings
```yaml
Function Configuration:
  Function name: beta50-hello-world
  Runtime: Python 3.11 (or latest available)
  Architecture: x86_64 (default)
  Permissions: Create new role with basic Lambda permissions
```

**Step-by-step:**
1. **Function name:** `beta50-hello-world`
2. **Runtime:** Select **"Python 3.11"** (or latest Python version)
3. **Architecture:** Leave as **"x86_64"** (default)
4. **Permissions:** Leave as **"Create a new role with basic Lambda permissions"**
5. Click **"Create function"**

---

### Step 3: Test the Function 🧪

#### 3.1 Configure Test Event
1. In the **Code** tab, click the **"Test"** button
2. You'll see "Configure test event" dialog
3. **Event name:** `TestEvent`
4. **Template:** Leave as **"hello-world"** (default)
5. **Event JSON:** Leave the default JSON as is:
```json
{
  "key1": "value1",
  "key2": "value2",
  "key3": "value3"
}
```
6. Click **"Save"**

#### 3.2 Execute the Function
1. Click **"Test"** button again
2. The function will execute
3. Wait for execution to complete

---

### Step 4: Review Results 📊

#### 4.1 Check Execution Results
**You should see:**
```yaml
Execution Results:
  Status: Succeeded
  Duration: ~1-5 ms
  Billed Duration: ~1 ms
  Memory Used: ~50 MB
  Max Memory: 128 MB
```

#### 4.2 View Function Response
**Expected Response:**
```json
{
  "statusCode": 200,
  "body": "\"Hello from Lambda!\""
}
```

#### 4.3 Check Logs
**In the logs section, you'll see:**
```
START RequestId: [unique-id] Version: $LATEST
END RequestId: [unique-id]
REPORT RequestId: [unique-id] Duration: X.XX ms Billed Duration: X ms Memory Size: 128 MB Max Memory Used: XX MB
```

---

## ✅ Verification Steps

### 🔍 Verify Function Creation

```bash
Function Verification:
✅ Function appears in Lambda console
✅ Function name is "beta50-hello-world"
✅ Runtime shows Python 3.11
✅ Function status is "Active"
```

### 🧪 Verify Function Execution

```bash
Execution Verification:
✅ Test event configured successfully
✅ Function executed without errors
✅ Response shows "Hello from Lambda!"
✅ Execution logs are visible
✅ Duration is under 100ms
```

---

## 🔧 Understanding Lambda Concepts

### ⚡ What is Serverless?

```yaml
Serverless Computing:
  No Server Management:
    - AWS manages all infrastructure
    - Automatic scaling
    - Built-in high availability
  
  Pay-per-Use:
    - Only pay for execution time
    - No charges when not running
    - Granular billing (100ms increments)
  
  Event-Driven:
    - Functions triggered by events
    - Automatic invocation
    - Scales to zero when idle
```

### 📊 Lambda Execution Model

```yaml
Function Lifecycle:
  1. Event Trigger: Function receives event
  2. Cold Start: Initialize runtime (first time)
  3. Handler Execution: Run your code
  4. Response: Return result
  5. Container Reuse: Keep warm for subsequent calls
```

---

## 💰 Cost Analysis

### 🆓 Free Tier Benefits

```yaml
Lambda Free Tier (Monthly):
  Requests: 1,000,000 free requests
  Compute: 400,000 GB-seconds
  Duration: Generous allowance for learning
  
Cost Example (After Free Tier):
  Requests: $0.20 per 1M requests
  Duration: $0.0000166667 per GB-second
  Your Test: Essentially free for learning
```

---

## 🔧 Troubleshooting

### ❌ Common Issues

#### Issue: Function Creation Fails
```bash
Possible Causes:
- Invalid function name
- Insufficient permissions
- Service limits reached

Solutions:
✅ Use alphanumeric characters and hyphens only
✅ Ensure IAM user has Lambda permissions
✅ Try different function name
```

#### Issue: Test Execution Fails
```bash
Common Problems:
- Syntax errors in code
- Timeout issues
- Memory limits

Solutions:
✅ Check function code for errors
✅ Increase timeout if needed
✅ Review CloudWatch logs for details
```

---

## 🎯 Next Steps

After completing this activity:

1. ✅ **Proceed to Activity 16:** [SNS Topic Creation](../../SNS/Guides/sns-topic-creation-guide.md)
2. 🔍 **Explore Code:** Look at the default Python code
3. 💡 **Try Modifications:** Change the response message
4. 📚 **Learn More:** Explore Lambda triggers and integrations

---

## 🆘 Need Help?

### 📞 Support Channels
- **Discord:** Beta 50 Batch Channel
- **Email:** awscloudclubscoe@yahoo.com
- **Office Hours:** Tuesday/Thursday 4-5 PM IST

### 🤔 Common Questions

**Q: What programming languages does Lambda support?**  
A: Python, Node.js, Java, C#, Go, Ruby, and custom runtimes.

**Q: How long can a Lambda function run?**  
A: Maximum execution time is 15 minutes.

**Q: Can Lambda functions access the internet?**  
A: Yes, by default they have internet access unless placed in a VPC.

**Q: How do I trigger Lambda functions?**  
A: Via API Gateway, S3 events, CloudWatch events, SNS, SQS, and many other AWS services.

---

<div align="center">

### 🎉 *Awesome! You've Created Your First Serverless Function!* 🎉

**You've successfully completed Activity 15 of the Beta 50 Program!**

<img src="https://media.giphy.com/media/3o7abKhOpu0NwenH3O/giphy.gif" width="150" alt="Success">

**Next: Activity 16 - SNS Topic Creation**

</div>