# This repository setups an AWS EC2 with Ubuntu 16.04 and Nginx


## Prerequisites

- [X] [Packer](https://www.packer.io/downloads)


## How to Use the Repo

- Clone this repo:
```shell
$ git clone git@github.com:dlavric/AWS-nginx-ubuntu.git
```

- Go to the directory where the repo is stored:
```shell
$ cd AWS-nginx-ubuntu
```

- Export the AWS credentials:
```shell
$ export AWS_ACCESS_KEY_ID="aws_access_key_id"
$ export AWS_SECRET_ACCESS_KEY="aws_secret_access_key"
$ export AWS_SESSION_TOKEN="aws_session_token"
```

- Validate the template:
```shell
$ packer validate example.pkr.hcl
```

- Build the image with Packer:
```shell
$ packer build \
    -var 'ami_name=packer-tutorial' \
    example.pkr.hcl
```