# Task 1 – Cloud Storage Setup on AWS S3

## ✅ Objective
Create and configure cloud storage using AWS S3. Upload example files and configure access permissions using bucket policies.

---

## ☁️ Cloud Provider Used
- Amazon Web Services (AWS)
- Service: S3 (Simple Storage Service)

---

## 🔧 Steps Performed

### 1. Created S3 Bucket
- Bucket Name: `codtech-cloud-storage-manasi`
- Region: Asia Pacific (Mumbai)
- Object Ownership: Bucket owner enforced
- Block Public Access: Disabled

### 2. Uploaded Files
- Files: `sample.txt`, `photo.jpg`, etc.

### 3. Configured Public Access Using Bucket Policy

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowPublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::codtech-cloud-storage-manasi/*"
    }
  ]
}
