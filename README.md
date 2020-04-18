# password-protected-docs

## GCP App Engine API

Must have google app engine api enabled:
https://console.developers.google.com/apis/api/appengine.googleapis.com/

## Service Account Permissions

- App Engine Deployer
- App Engine Service Admin
- Cloud Build Service Account
- Storage Object Creator
- Storage Object Viewer

## Service Account Key on CircleCI

Save service account key (json) as environment variable in circleCI, but then write it to a file before using it or gcloud command will interpret as .p12

## IAP settings

Add anyone you want to have access as `IAP-secured Web App User` from: https://console.cloud.google.com/security/iap

Can use a google group and then just add/remove people from it!

---

Next steps...
- Adding custom domain