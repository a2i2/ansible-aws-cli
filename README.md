# AWS CLI role for Ansible

Installs and configures the AWS CLI for conveniently interacting with AWS services such as S3.

## Requirements

-   Tested on Ubuntu 12.04 Server;
-   Ansible 2.0+

## Role Variables

The default variables are as follows:

    aws_output_format: 'json'
    aws_region: 'ap-southeast-2'
    aws_access_key_id: 'YOUR_ACCESS_KEY_ID'
    aws_secret_access_key: 'YOUR_SECRET_ACCESS_KEY'

## Example Playbook

    - hosts: 'servers'
      roles:
        - role: 'dstil.aws-cli'
          aws_output_format: 'json'
          aws_region: 'ap-southeast-2'
          aws_access_key_id: 'SUPER_SECRET_ACCESS_KEY_ID'   # Don't version this or put it on pastebin
          aws_secret_access_key: 'SUPER_SECRET_ACCESS_KEY'  # Ditto

# License

This playbook is provided 'as-is' under the conditions of the BSD license. No fitness for purpose is guaranteed or implied.
