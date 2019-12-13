# Squid-Packer

[Packer](https://www.packer.io/) templates to build a [Squid](http://www.squid-cache.org/) proxy AWS AMI

## Usage

Clone the repository:

    $ git clone https://github.com/mohtork/packer.git  && cd packer/squid

Validate the packer template:

    $ packer validate squid.json  

Build a machine image from the template in the repository:

    $ packer build squid.json

## Configuration

You can configure each template to match your requirements by setting the following [user variables](https://packer.io/docs/templates/user-variables.html).

 User Variable                 | Description
------------------------------ |----------------------------------------------------------------------------------------
 `AWS_REGION`                  | as environment variable
 `AWS_ACCESS_KEY`              | as environment variable
 `AWS_SECRET_KEY`              | as environment variable
 `source_ami`                  | The base AWS AMI you will use to build squid on top of , should be centOS , AWS Linux or Redhat
 `ssh_username`                | 'ec2-user' for Amazon Linux , 'centos' for CenOS
 `ssh_key_pair`                | The name of ssh key you have created on AWS
 `ssh_private_key_file`        | The path to private key you have downloaded from AWS


### Requirments

Ansible should be installed on the host that will build AMI with packer

