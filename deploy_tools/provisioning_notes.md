Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3
* Git
* pip
* virtualenv


eg, on Ubuntu:

    sudo apt-get install nginx git python3 python3-pip
    sudo pip3 install virtualenv

## Ngins Virtual Host config

* see nginx.template.conf
* replace SITENAME with, eg, stage-my-domain.com

## Upstart job

* see gunicorn-systemd.template.conf
* replace SITENAME with, eg, stage-my-domain.com
* run
    sudo systemctl enable gunicorn-stage-stage-my-domain.com

## Folder structure

/home/username
|__sites
    |__SITENAME
        |-- database
        |-- source
        |-- static
        |-- virtualenv