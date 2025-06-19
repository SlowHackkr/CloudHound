# CloudHound 🕵️‍♂️

> **Red Team Cloud Recon Framework** | AWS, Azure, and GCP Misconfiguration Scanner

CloudHound is a Python-based offensive security tool designed for red teamers, security researchers, and penetration testers to identify common misconfigurations across cloud platforms like AWS, Azure, and GCP.

## ✨ Features

* 🔍 Detect exposed metadata service endpoints
* 🔑 Identify public AWS S3 buckets
* 🚀 Find open Google Cloud Storage (GCS) buckets
* 📁 Discover publicly accessible Azure Blob Containers
* 📅 Analyze IAM roles for privilege escalation risks (Stub)
* 🧐 Regex match for known credential patterns and tokens

## ⚙️ Usage

```bash
python3 cloudhound.py --target https://your-cloud-domain.com
```

### Options

* `--target`: Required. URL or domain to scan for cloud exposures.

## 🌎 Example Output

```
🔎 Scanning: https://example.com
[+] AWS Metadata exposed at: http://example.com/latest/meta-data/
[!] GCP Storage Bucket exposed: gs://open-public-data
[!] Azure Blob Container is public: https://account.blob.core.windows.net/public-container
[+] IAM Policy Exposure: Detected Overly-Permissive Role "Editor"
[+] AWS Key Pattern Found: AKIAIOSFODNN7EXAMPLE

[✔] CloudHound Scan Complete. Analyze your output for exposures.
```

## 📄 Requirements

* Python 3.8+
* `requests`
* `argparse`
* `re`, `json`, `os`, `time`

Install dependencies:

```bash
pip install -r requirements.txt
```

### `requirements.txt`

```
requests
```

## 🔖 Demo Banner

```bash
   ____ _                 _     _                 _                 _
  / ___| | ___  _   _  __| | __| |_ __ ___  _ __ | | ___   __ _  __| |
 | |   | |/ _ \| | | |/ _` |/ _` | '__/ _ \| '_ \| |/ _ \ / _` |/ _` |
 | |___| | (_) | |_| | (_| | (_| | | | (_) | | | | | (_) | (_| | (_| |
  \____|_|\___/ \__,_|\__,_|\__,_|_|  \___/|_| |_|_|\___/ \__,_|\__,_|

    CloudHound v2.0 — Multi-Cloud Misconfig Hunter [Red Team Edition]
```

## ⚠️ Ethical Notice

CloudHound is intended **only for authorized testing and academic research**. Use it **only on systems you own or are explicitly permitted to test**. Misuse is strictly prohibited.

## 💼 License

Educational Use License. Free for academic, ethical, and non-commercial use.

## 👤 Author

**Arunabha Mishra**
GitHub: [@SlowHackkr](https://github.com/SlowHackkr)
