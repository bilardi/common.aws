# common.aws
The repository contains all that you need to manage your AWS account
* cloudformation templates of each object
* guideline to create all

## Prerequisite
* an AWS account, in this repository called **your-account**

## Usage
```sh
pip install awscli --upgrade --user
aws configuration --profile your-account
git clone https://github.com/bilardi/common.aws.git
cd common.aws/infrastructure/
more README.md
# and if you don't save your custom configurations on a repository versioned, then copy all on s3
aws s3 cp . s3://your-custom-configurations-bucket/common.aws/ --recursive --exclude "*" --include "*.json" --include "*.yaml" --include "*yml" --profile your-account
# and if you have to modify it, then copy all on your local
aws s3 cp s3://your-custom-configurations-bucket/common.aws/ . --recursive --exclude "*" --include "*.json" --include "*.yaml" --include "*yml" --profile your-account
```
