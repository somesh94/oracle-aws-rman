# oracle-aws-rman
Migrated an on-premise Oracle database to an EC2-hosted Oracle server in AWS. Implemented automated RMAN backup using Bash and Python scripts to store daily backups in Amazon S3. The Oracle EC2 instance is hosted in a private subnet with access configured via a bastion (jump) server.

# Oracle RMAN Backup Automation to AWS S3

This project automates Oracle RMAN backups and uploads them to Amazon S3, running on an EC2-hosted Oracle server in a private subnet.

---

## 🚀 Project Overview

- **Migration**: Migrated an on-premise Oracle database to an EC2 instance in AWS.
- **Architecture**: Oracle EC2 hosted in a **private subnet**, accessed securely via a **bastion (jump) server**.
- **Backup Automation**:
  - Used **RMAN** to take Oracle database backups.
  - Wrote **Bash** and **Python scripts** to handle the backup and upload.
  - Backups are stored automatically in an **S3 bucket**.
- **Automation**: Set up a **cron job** to run the backup and upload script daily.
- **Validation**: Verified backup upload in the S3 bucket and maintained logging.

---

## 🛠️ Technologies Used

- **Oracle Database**
- **AWS EC2 (Private Subnet)**
- **AWS S3**
- **AWS IAM (for role-based access)**
- **Bastion Host**
- **Python (Boto3 for S3 upload)**
- **Bash**
- **Crontab (for job scheduling)**

---

## 📂 Scripts Included

### `backup.sh`
- Shell script to:
  - Trigger Oracle RMAN backup
  - Call Python script to upload `.bkp` files to S3

### `upload_rman_to_s3.py`
- Python script that:
  - Scans the backup directory
  - Uploads `.bkp` files to a specified S3 bucket using Boto3
  - Logs all activity (success/failure)

---

## 📸 Included Screenshots

- VPC & Subnet setup
- On-premise database snapshot
- Bastion server configuration
- Oracle EC2 server setup
- Database creation in EC2
- Export/import of database
- IAM role for S3 access
- S3 bucket creation and config
- Crontab job for automation
- RMAN backup run logs
- Backup visible in the S3 bucket

---

## 📎 GitHub Repository

**🔗 [Click here to view the project on GitHub](https://github.com/somesh94/oracle-aws-rman)**

