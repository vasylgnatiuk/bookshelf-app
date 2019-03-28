<h1 align="center"> BOOKSHELF APP</h2>

<h2 align="center">Requirements</h2>

This app for GCP lab work

- Cloud Storage bucket with public-read rights
- Cloud SQL instance

> Note: You must authenticate gcloud to use app from your local machine.

<h2 align="center">Config & Run</h2>

This app for GCP lab work

    DATA_BACKEND = 'cloudsql'
    PROJECT_ID = 'YOUR_PROJECT_ID'
    CLOUDSQL_USER = 'CLOUD_SQL_USER'
    CLOUDSQL_PASSWORD = 'SQL_USER_PASSWORD'
    CLOUDSQL_DATABASE = 'DATABASE_NAME'
    CLOUDSQL_CONNECTION_NAME = 'YOUR_PROJECT_ID:REGION:CLOUD_SQL_INSTANCE_NAME'

> Note: You must authenticate gcloud to use app from your local machine.