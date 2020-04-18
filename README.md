# password-protected-docs

## GCP App Engine API

Must have google app engine api enabled:
https://console.developers.google.com/apis/api/appengine.googleapis.com/

## Service Account Permissions

- App Engine Deployer
- Cloud Build Service Account
- Storage Object Creator
- Storage Object Viewer

## Service Account Key on CircleCI

Save service account key (json) as env var, but then write it to a file before using it or gcloud command will interpret as .p12
