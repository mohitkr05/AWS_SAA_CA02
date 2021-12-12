
#Installing AWS CLI on Ubuntu 20.04 on WSL 2

1. Update the WSL system 
```
sudo apt update 
sudo apt upgrade

```

2. Download the AWS cli package, check for the updated package on the following [link](https://docs.aws.amazon.com/cli/v1/userguide/install-linux.html)

```

curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"
unzip awscli-bundle.zip

```

3. Install Python3.8-venv and Python-is-Python3

```
sudo apt install python3.8-venv
sudo apt-get install python-is-python3
```