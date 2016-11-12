gcloud-ubuntu
===============

[![Build Status](https://travis-ci.org/suzuki-shunsuke/ansible-gcloud-ubuntu.svg?branch=master)](https://travis-ci.org/suzuki-shunsuke/ansible-gcloud-ubuntu)

Ansible Role to [Install gcloud on Ubuntu](https://cloud.google.com/sdk/docs/quickstart-debian-ubuntu).

```
# Create an environment variable for the correct distribution
export CLOUD_SDK_REPO="cloud-sdk-$(lsb_release -c -s)"

# Add the Cloud SDK distribution URI as a package source
echo "deb https://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee /etc/apt/sources.list.d/google-cloud-sdk.list

# Import the Google Cloud Platform public key
curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

# Update the package list and install the Cloud SDK
sudo apt-get update && sudo apt-get install google-cloud-sdk
```

https://galaxy.ansible.com/suzuki-shunsuke/gcloud-ubuntu/

Requirements
------------

Nothing.

Role Variables
--------------

Nothing.

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: servers
  roles:
  - role: suzuki-shunsuke.gcloud-ubuntu
```

License
-------

MIT
