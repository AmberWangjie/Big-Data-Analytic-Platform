# Terraform

## AWS configuration
To use Terraform, you have to gain a pair of AWS key/secret
See [here](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html) (Using_CreateAccessKey) for ways to get it


After getting the AWS access key and access key secret, modify `~/.aws/credentials` as following:
```ini
[default]
aws_access_key_id = [your access key id]
aws_secret_access_key = [your access key secret]
```

To be able to remotely ssh into your ec2 instance, you also need to create an ec2 keypair
See [here](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) for ways to get it.

After getting your AWS EC2 private key, please save it locally。Then run the command to modify the permission of private key, otherwise it is possible to not be able to do ssh connection
```sh
chmod 400 [private key location]
```

## Ansible configuration
See README.md under project/Ansible