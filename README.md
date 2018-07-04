# AWS CLI role for Ansible
==================================

Installs and configures the AWS CLI for conveniently interacting with AWS services such as S3.

Role Variables
--------------

The default variables are as follows:

    aws_output_format: 'json'
    aws_region: 'ap-southeast-2'
    aws_access_key_id: 'YOUR_ACCESS_KEY_ID'
    aws_secret_access_key: 'YOUR_SECRET_ACCESS_KEY'

    aws_cli_user: 'root'
    aws_cli_group: 'root'
    aws_home: '/root'

Requirements
--------------------
    pip

Example Playbook
--------------------
    - hosts: 'localdev'
      roles:
        - role: 'aws-cli'
          aws_output_format: 'json'
          aws_region: 'eu-central-1'
          aws_access_key_id: 'SUPER_SECRET_ACCESS_KEY_ID'   # Don't version this or put it on pastebin
          aws_secret_access_key: 'SUPER_SECRET_ACCESS_KEY'  # Ditto

