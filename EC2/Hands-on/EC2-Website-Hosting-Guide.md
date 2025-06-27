# EC2 Website Hosting Guide

## Overview
This guide walks you through hosting a static website on Amazon EC2 using Apache web server on Amazon Linux.

## Demo Page
**Live Demo:** http://3.92.199.168/

Enter the above IP address in your browser to see a working example of a static website hosted on EC2.

## Prerequisites
- AWS Account
- Basic knowledge of Linux commands
- SSH client

## Step-by-Step Instructions

### 1. Launch EC2 Instance
- Go to AWS Console → EC2 → Launch Instance
- Choose **Amazon Linux 2023 AMI**
- Select **t2.micro** (free tier eligible)
- Create or select existing key pair
- Configure Security Group with these rules:
  - SSH (22) - Your IP only
  - HTTP (80) - 0.0.0.0/0 (anywhere)
  - HTTPS (443) - 0.0.0.0/0 (anywhere)

### 2. Connect to Instance

**Method 1: Using SSH (Terminal)**
```bash
ssh -i your-key.pem ec2-user@your-public-ip
```

**Method 2: Using AWS Console (Browser-based)**
1. Go to AWS Console → EC2 → Instances
2. Select your instance from the list
3. Click **Connect** button
4. Choose **EC2 Instance Connect** tab
5. Verify the username is `ec2-user`
6. Click **Connect** to open browser terminal

### 3. Install Apache Web Server
```bash
# Update system
sudo yum update -y

# Install Apache
sudo yum install -y httpd

# Start and enable Apache
sudo systemctl start httpd
sudo systemctl enable httpd
```

### 4. Create Your Website
Navigate to web directory and create HTML file:
```bash
cd /var/www/html
sudo nano index.html
```

Add this simple HTML content:
```html
<!DOCTYPE html>
<html>
<head>
    <title>My EC2 Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
        }
        .box {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
            text-align: center;
        }
        h1 {
            color: #333;
            margin: 0;
        }
    </style>
</head>
<body>
    <div class="box">
        <h1>Hello World!</h1>
        <p>Welcome to my EC2 hosted website</p>
    </div>
</body>
</html>
```

### 5. Set Permissions
```bash
# Set ownership and permissions
sudo chown -R apache:apache /var/www/html
sudo chmod -R 755 /var/www/html

# Restart Apache
sudo systemctl restart httpd
```

### 6. Access Your Website
- Get your EC2 public IP: `curl http://checkip.amazonaws.com`
- Open browser and go to: `http://YOUR-PUBLIC-IP`

## Troubleshooting
```bash
# Check Apache status
sudo systemctl status httpd

# View error logs
sudo tail -f /var/log/httpd/error_log

# Check if port 80 is open
sudo netstat -tulpn | grep :80
```

## Quick Commands Summary
```bash
sudo yum update -y && sudo yum install -y httpd
sudo systemctl start httpd && sudo systemctl enable httpd
sudo chown -R apache:apache /var/www/html
sudo chmod -R 755 /var/www/html
```

## Demo Reference
Visit http://3.92.199.168/ to see a live example of this setup in action.

---
**Note:** Replace placeholder values with your actual EC2 instance details.