# Ansible for Redmine (local setup)

## setup ansible (for Ubuntu 14.04)

```
$ sudo apt-get update
$ sudo apt-get install python-dev libxml2-dev libxslt-dev python-pip
$ sudo pip install ansible markupsafe
$ ansible --version
=> 2.0.1.0
```

## setup ansible (for CentOS 7)

```
sudo yum install epel-release
sudo yum install ansible
sudo yum install git
```

## clone repository

```
$ cd /tmp
$ git clone git@github.com:agileware-jp/ansible_redmine_local.git
```

## run ansible

```
$ cd /tmp/ansible_redmine_local
$ ansible-playbook -i hosts setup_redmine.yml --extra-vars '{ "app_fqdn":"[EXAMPLE.COM]" }'
```
