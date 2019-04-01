<h1 align="center">Project DevOps</h1>

<h2 align="center">Requirements</h2>

- GCP account
- Terraform
- Ansible

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

## Terraform

- Use remote state file in separate Cloud Storage bucket
  - Create Cloud Storage Bucket for Terraform remote state
- Create VPC Network
- Create firewall rules
- Create Cloud NAT
- Create SQL instance with private ip
- Create Cloud Storage Bucket for Application content
- Create Service Account for Application instance
- Create Instance template (fill up metadata: SQL instance connection string, bucket name)
- Create MIG
- Create HTTP LB

> Optional: Create Terraform Modules