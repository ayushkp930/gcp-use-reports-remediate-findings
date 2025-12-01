# Use reports to remediate findings – Google Cloud SCC Lab

This repository documents my work on the **"Use reports to remediate findings"** lab in Google Cloud.

## Lab Overview

- **Platform:** Google Cloud Platform (GCP)
- **Service:** Security Command Center (SCC)
- **Goal:** Identify and remediate misconfigurations and vulnerabilities reported by SCC.

## Key Findings

1. **Public bucket ACL**
   - Some Cloud Storage buckets were publicly accessible.
   - **Fix:** Removed `allUsers` / `allAuthenticatedUsers` from bucket IAM and restricted access to project members only.

2. **Bucket policy only disabled**
   - Bucket Policy Only / Uniform bucket-level access was disabled.
   - **Fix:** Enabled **Uniform bucket-level access** to simplify and centralize permissions.

3. **Public IP address on VM**
   - A VM instance had a public IP.
   - **Fix:** Removed external IP (or would recreate VM without public IP in a real environment).

4. **Default service account used**
   - VM was using the default Compute Engine service account with broad permissions.
   - **Fix:** Recommended using a dedicated least-privilege service account.

5. **Full API access**
   - VM had full Cloud API access scope.
   - **Fix:** Restricted scopes to only the APIs required.

6. **Bucket logging disabled**
   - Access logs were not enabled on the storage bucket.
   - **Fix:** Enabled bucket logging to monitor access and support audits.

## Screenshots

Folder: `screenshots/`

The screenshots show:
- SCC risk overview
- Compliance dashboards
- Vulnerabilities list before remediation
- Cloud Storage bucket permissions and public access configuration

## What I Learned

- How to use **Security Command Center** to view compliance and security posture.
- How to interpret **IAM & Storage** findings (public access, logging, policy-only).
- Practical steps to harden **Cloud Storage** and **Compute Engine** using SCC recommendations.
