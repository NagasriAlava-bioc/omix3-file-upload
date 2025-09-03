# OMIX3 File Upload and Indexd Script

This repository contains a Python script to upload files to OMIX3 storage and update Indexd records using the Gen3 SDK.

---

## Prerequisites

1. **Gen3 Credentials**: You must have a cred.json file containing your Gen3 API token with appropriate write permissions to the target project.
2. **Access to S3 Bucket**: Ensure that your Gen3 project is configured with an S3 bucket where files can be uploaded.
3. **Python Environment**: Python 3.10+ is recommended.
---

## Python Environment Setup

### Step 1: Create a virtual environment

```bash
python3 -m venv gen3_env
```
### Step 2: Activate the environment

## Linux/macOS:

```bash
source gen3_env/bin/activate
```

## Windows:

```bash
gen3_env\Scripts\activate
```
### Step 3: Install required packages
```bash
pip install -r requirements.txt
```

#### Packages used in the script:

gen3.auth and gen3.file (from gen3)
requests (for HTTP uploads)
PyJWT (for decoding token information)
boto3, botocore, jmespath, s3transfer (if using S3 uploads)

## Script Usage
### Step 1: Run the script
```bash
python scripts/gen3sdk_upload_file.py <file_to_upload>
```
#### Example:
```bash
python scripts/gen3sdk_upload_file.py ~/path/to/test_s3_in_01.txt
```
