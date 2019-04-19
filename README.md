<h1 align="center">Application for DevOps lab</h1>

- Install dependencies `git, virtualenv`
- Download, install, and initialize the Cloud SDK
- Setup SQL Proxy

> Note: You must authenticate gcloud to use the proxy

```
  wget https://dl.google.com/cloudsql/cloud_sql_proxy.linux.amd64 -O cloud_sql_proxy
  chmod +x cloud_sql_proxy
  ./cloud_sql_proxy -instances='{YOUR_SQL_CONNECTION_NAME}'=tcp:3306
```

- Clone the sample repository: `git clone https://github.com/kovalandoleg/bookshelf-app.git`
- Configuring the app config.py

```
  PROJECT_ID={YOUR_PROJECT_ID}
  CLOUDSQL_USER={YOUR_SQL_USER}
  CLOUDSQL_PASSWORD={YOUR_SQL_USER_PASSWORD}
  CLOUDSQL_DATABASE={YOUR_SQL_DATABASE_NAME}
  CLOUDSQL_CONNECTION_NAME={YOUR_SQL_CONNECTION_NAME}
  CLOUD_STORAGE_BUCKET={YOUR_BUCKET_NAME}
```

- Install app dependencies

```
  virtualenv -p python3 env
  source env/bin/activate
  pip install -r requirements.txt
```

- Create tables with command: `python bookshelf/model_cloudsql.py`
- Run application: `honcho start -f ./procfile worker bookshelf`

> Google [tutorial](https://cloud.google.com/python/tutorials/bookshelf-on-compute-engine) for this python application
