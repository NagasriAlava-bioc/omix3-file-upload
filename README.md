# OMIX3 File Upload and Indexd Script

This repository contains a Python script to upload files to OMIX3 storage and update Indexd records using the Gen3 SDK.

---

## Prerequisites

1. **Python 3** installed on your system.  
2. **Gen3 credentials**: You should have a valid token either in `~/.gen3/credentials.json` or via the `GEN3_AUTH_TOKEN` environment variable.  
3. **Internet access** to reach the OMIX3 Gen3 API and storage endpoints.  

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
