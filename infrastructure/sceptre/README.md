# Commands for provisioning the infrastructure
```sh
grep your -R config/*
# edit your custom configuration and then
pip install sceptre
export AWS_PROFILE=your-account
sceptre validate-template production s3
sceptre launch-env production
# and if it was the first time, uncomment the template_bucket_name line on config/config.yaml and then reload for saving the templates release on s3
sceptre launch-env production
```
