## Bit Zesty Ansible Playbooks

**For recent changes please refer to [the changelog](https://github.com/bitzesty/ansible_playbooks/blob/master/CHANGELOG.md)**.

### Own Recipes

#### Packages (roles/packages)

Installs general packages

#### SSH configuration (roles/ssh_config)

Sets up base SSH configuration (/etc/ssh/ssh_config and /etc/ssh/sshd_config)

#### Deployer (roles/deployer)

Sets up deployer user account

#### Github users (roles/github_users)

Fetches allowed users ssh keys from https://github.com/{{ item }}.keys and uploads them to /home/{{ deployer }}/.ssh/authorized_keys

#### Postgresql (roles/postgresql)

Sets up postgresql 9.3

#### NGINX Setup (roles/nginx)

Sets up NGING / Passenger for app

#### Rbenv Ruby Setup (roles/rbenv_ruby)

Sets up Rbenv and required Ruby

#### Rails env variables (roles/rails_env_vars)

Adds env variables to deployer user's .bashrc file

#### Passenger restart (roles/passenger_restart)

Restarts Passenger

#### Restart shoryuken (roles/restart_shoryuken | NEED TO SWITCH TO RUNIT)

Restarts Shoryuken

#### Restart NGINX (roles/nginx_restart)

Restarts NGINX

#### Upstart scripts (roles/upstart)

Add services to upstart (for now only shoryuken available)

### Third Party Recipies

#### Locale (f500.locale) (roles/locales)

https://github.com/f500/ansible-locale

* Generate localisation files from templates (locale-gen).
* Configure locale environment variables.

#### Clamav (igor_mukhin.clamav) (roles/locales)

https://github.com/ansible-roles/ansible-role-clamav

Ansible role to install clamav antivirus and optionally ClamTK

#### App Deployment Playbooks (nicolai86.*)

1) nicolai86.prepare-release

https://github.com/nicolai86/ansible-prepare-release

Prepares a new release via GIT

2) nicolai86.rails-deployment

https://github.com/nicolai86/ansible-rails-deployment

Deploy project

3) nicolai86.finalize-release

https://github.com/nicolai86/ansible-finalize-release

Finalize the release

