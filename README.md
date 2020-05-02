# password-protected-docs

A full explanation/walkthrough of this project can be found at: https://devopsdirective.com/posts/2020/04/password-protected-website/

## GCP App Engine API

This project uses Google's App Engine API which must be enabled for your GCP project here: https://console.developers.google.com/apis/api/appengine.googleapis.com/

## Service Account Permissions

The service account credentials used by CircleCI must have the following roles:

- App Engine Deployer
- App Engine Service Admin
- Cloud Build Service Account
- Storage Object Creator
- Storage Object Viewer

## Service Account Key on CircleCI

Save service account key (json) as environment variable in circleCI, but then write it to a file before using it or gcloud command will interpret as .p12

```bash
echo ${GCLOUD_SERVICE_KEY} > /tmp/sa_key.json
gcloud auth activate-service-account --key-file=/tmp/sa_key.json
rm /tmp/sa_key.json
```

## IAP settings

Access to the site is controlled by granting individuals or groups the `IAP-secured Web App User` role from: https://console.cloud.google.com/security/iap

---

Next steps...
- Adding custom domain
- Customize the OAuth consent screen