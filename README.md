# packer-ansible-sentry

Packer recipe for creating a DigitalOcean snapshot image with Sentry using Ansible to provision.

## configure

Copy `secrets.json.example` to `secrets.json` and edit to your taste.

Copy `.env.example` to `.env` and edit to your taste.

## install dependencies

Ansible Galaxy requirements:

    ansible-galaxy install -r requirements.yml

## build

Build a DigitalOcean snapshot image:

    packer build packer.json

## services

### local services
- postgresql
- redis-server
- sentry-web
- sentry-worker
- sentry-cron

### public services
- nginx (virtual host proxied to sentry-web)
