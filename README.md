# gcp-buckets-compute-labs
Microsoft Windows [Version 10.0.26220.7344]
(c) Microsoft Corporation. All rights reserved.

C:\Windows\System32>cd "C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin"

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil mb -l us-central1 gs://ak-demo-1-20251213/
Creating gs://ak-demo-1-20251213/...

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil cp "C:\Users\Asus\Desktop\GCP_prac\customer_details.csv" gs://ak-demo-1-20251213/
Copying file://C:\Users\Asus\Desktop\GCP_prac\customer_details.csv [Content-Type=application/vnd.ms-excel]...
\ [1 files][ 23.1 KiB/ 23.1 KiB]
Operation completed over 1 objects/23.1 KiB.

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil versioning set on gs://ak-demo-1-20251213//
CommandException: "versioning" command must specify a bucket

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil versioning set on gs://ak-demo-1-20251213/
Enabling versioning for gs://ak-demo-1-20251213/...

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil cp "C:\Users\Asus\Desktop\GCP_prac\customer_details.csv" gs://ak-demo-1-20251213/
Copying file://C:\Users\Asus\Desktop\GCP_prac\customer_details.csv [Content-Type=application/vnd.ms-excel]...
- [1 files][ 23.1 KiB/ 23.1 KiB]
Operation completed over 1 objects/23.1 KiB.

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil ls -a gs://ak-demo-1-20251213/
gs://ak-demo-1-20251213/customer_details.csv#1765569024910788
gs://ak-demo-1-20251213/customer_details.csv#1765569121184505

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil lifecycle set lifecycle.json gs://ak-demo-1-20251213/
OSError: No such file or directory.

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil lifecycle set "C:\Users\Asus\Desktop\GCP_prac\lifecycle.json" gs://ak-demo-1-20251213/
Setting lifecycle configuration on gs://ak-demo-1-20251213/...

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gsutil lifecycle get gs://ak-demo-1-20251213/
{"rule": [{"action": {"type": "Delete"}, "condition": {"age": 30}}]}

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances create ak-demo1-vm\ --machine-type=e2-micro \ --zone=us-central1-a
ERROR: (gcloud.compute.instances.create) unrecognized arguments: \

To search the help text of gcloud commands, run:
  gcloud help -- SEARCH_TERMS

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances create ak-demo1-vm \ --machine-type=e2-micro \ --zone=us-central1-a
ERROR: (gcloud.compute.instances.create) unrecognized arguments: \

To search the help text of gcloud commands, run:
  gcloud help -- SEARCH_TERMS

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances create ak-demo1-vm --machine-type=e2-micro --zone=uscentral1 -a
ERROR: (gcloud.compute.instances.create) unrecognized arguments: -a

To search the help text of gcloud commands, run:
  gcloud help -- SEARCH_TERMS

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances create ak-demo1-vm --machine-type=e2-micro --zone=uscentral1-a
ERROR: (gcloud.compute.instances.create) Could not fetch resource:
 - Permission denied on 'locations/uscentral1-a' (or it may not exist).


C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances create ak-demo1-vm --machine-type=e2-micro --zone=uscentral1
ERROR: (gcloud.compute.instances.create) Could not fetch resource:
 - Permission denied on 'locations/uscentral1' (or it may not exist).


C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances create ak-demo1-vm --machine-type=e2-micro --zone=us-central1-a
Created [https://www.googleapis.com/compute/v1/projects/groovy-catalyst-481010-n9/zones/us-central1-a/instances/ak-demo1-vm].
NAME         ZONE           MACHINE_TYPE  PREEMPTIBLE  INTERNAL_IP  EXTERNAL_IP    STATUS
ak-demo1-vm  us-central1-a  e2-micro                   10.128.0.3   34.57.121.217  RUNNING

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute ssh ak-demo1-vm --zone=us-central1-a
WARNING: The private SSH key file for gcloud does not exist.
WARNING: The public SSH key file for gcloud does not exist.
WARNING: The PuTTY PPK SSH key file for gcloud does not exist.
WARNING: You do not have an SSH key for gcloud.
WARNING: SSH keygen will be executed to generate a key.
This tool needs to create the directory [C:\Users\Asus\.ssh] before being able to generate SSH keys.

Do you want to continue (Y/n)?  Y

WARNING: Invalid characters in local username [Kommula Akhila]. Using username corresponding to active account: [g712akv3]
Updating project ssh metadata...|Updated [https://www.googleapis.com/compute/v1/projects/groovy-catalyst-481010-n9].
Updating project ssh metadata...done.
Waiting for SSH key to propagate.
The host key is not cached for this server:
  34.57.121.217 (port 22)
You have no guarantee that the server is the computer you
think it is.
The server's ssh-ed25519 key fingerprint is:
  ssh-ed25519 255 SHA256:PA76H2FFVSjMSUMlqqNhSuVRgtCDzJV7HPrUjnFs8jE
If you trust this host, enter "y" to add the key to Plink's
cache and carry on connecting.
If you want to carry on connecting just once, without adding
the key to the cache, enter "n".
If you do not trust this host, press Return to abandon the
connection.
Store key in cache? (y/n, Return cancels connection, i for more info)
C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>dfdfvgdfgdy
'dfdfvgdfgdy' is not recognized as an internal or external command,
operable program or batch file.

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>y
'y' is not recognized as an internal or external command,
operable program or batch file.
C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcould compute instances delete ak-demo1-vm --zone=us-central1-a
'gcould' is not recognized as an internal or external command,
operable program or batch file.

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>gcloud compute instances delete ak-demo1-vm --zone=us-central1-a
The following instances will be deleted. Any attached disks configured to be auto-deleted will be
deleted unless they are attached to any other instances or the `--keep-disks` flag is given and
specifies them for keeping. Deleting a disk is irreversible and any data on the disk will be lost.
 - [ak-demo1-vm] in [us-central1-a]

Do you want to continue (Y/n)?  Y

Deleted [https://www.googleapis.com/compute/v1/projects/groovy-catalyst-481010-n9/zones/us-central1-a/instances/ak-demo1-vm].

C:\Program Files (x86)\Google\Cloud SDK\google-cloud-sdk\bin>









## Overview
Hands-on GCP lab demonstrating Google Cloud Storage (GCS) bucket configuration and data transfer to Compute Engine VM.  
Project ID: groovy-catalyst-481010-n9 | Date: December 13, 2025  
Goal: Practice production patterns like versioning (data protection), lifecycle (cost control), and bucket-to-VM data flow (batch processing).

### Why Versioning?
Object versioning protects individual files (objects) in the bucket.  
If a file is accidentally overwritten or deleted (by bug, employee, or ransomware), older versions remain recoverable.  
Real-world: Companies enable this on customer/transaction data to survive attacks and meet audit requirements.

### Why Lifecycle Rule?
Standard storage class has high monthly cost but no retrieval fee — great for active data.  
Data older than ~30 days is rarely accessed, so keeping it in Standard wastes money.  
Lifecycle auto-deletes (or downgrades to cheaper classes) to cap costs.  
Example: 10 GB new data/day → without rule, cost grows forever. With rule, max ~300 GB billed.

### Why e2-micro + Specific Zone?
- Compute (VM hours) costs more than storage → use smallest free-tier machine (e2-micro) for learning/small jobs.
- Single zone (us-central1-a): Lower latency (data close to bucket), meets data location rules.

### How VM Accessed Bucket Without Password?
The VM runs under the project's service account (robot identity) with IAM permissions — no keys needed.  
`gsutil` inside VM automatically uses the VM's identity (secure, no hardcoded credentials).

## Key Learnings
- GCS is for unstructured data lakes; versioning protects files from loss/overwrites.
- Lifecycle rules are automatic cost control — essential for scaling data.
- Compute Engine = full virtual servers; use small/free for tests, delete when idle to avoid billing.
- Data flows securely from bucket → VM using project identity (no passwords).
- These patterns are used daily in real data engineering pipelines.
