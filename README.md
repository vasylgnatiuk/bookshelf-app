<h1 align="center">Project DevOps</h1>

<h2 align="center">Requirements</h2>

- GCP account
- Terraform
- Ansible
- Application setup [tutorial](https://cloud.google.com/python/tutorials/bookshelf-on-compute-engine)

> Note: You should never push your gcp credentials to public and allways destroy resources in cloud after work
---

![](./Phase_III_Project.png)

<h2 align="center">Task Breakdown</h2>

## GCP Console

- Create new project (or use default)
- Create new Service Account for Terraform (or use default)
- Create Cloud Storage bucket for Terraform state file
- Enabe all necessary APIs:
  - [x] Cloud SQL Admin API
  - [x] Cloud Pub/Sub API
  - [x] Service Networking API
  - [x] Cloud Resource Manager API
  - [x] Identity and Access Management (IAM) API

## Terraform

- Use remote state file in separate Cloud Storage bucket
- Create VPC Network
- Create Cloud NAT
- Create SQL instance with private ip
- Create SQL database
- Create Cloud Storage Bucket for Application content
- Create Service Account for Application instance
- Create Instance template (fill up metadata with vars for [ansible](#ansible)
- Create MIG
- Create firewall rules
- Create HTTP LB

> Optional: Create Terraform Modules

## Ansible

- Cloning the sample app (this repo)
- Configuring the app config.py
  - [x] PROJECT_ID
  - [x] CLOUD_STORAGE_BUCKET
  - [x] CLOUDSQL_USER
  - [x] CLOUDSQL_PASSWORD
  - [x] CLOUDSQL_DATABASE
  - [x] CLOUD_STORAGE_BUCKET
- Enable application at startup ([example](https://github.com/GoogleCloudPlatform/getting-started-python/blob/master/7-gce/gce/startup-script.sh))

> Optional: Create Terraform Modules