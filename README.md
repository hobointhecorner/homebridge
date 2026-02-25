# homebridge systemd service

This is my personal Ansible playbook to configure `homebridge` as a docker compose systemd service on a dedicated host.

## Ansible roles
- [hobo.common](https://github.com/hobointhecorner/Hobo.Ansible.Common)
- [hobo.docker](https://github.com/hobointhecorner/Hobo.Ansible.Docker)
- [hobo.docker-service](https://github.com/hobointhecorner/hobo.ansible.docker-compose-systemd)
- [hobo.service-user](https://github.com/hobointhecorner/hobo.ansible.service_user)
- [hobo.awscliconfig](https://github.com/hobointhecorner/Hobo.Ansible.AwsCliConfigurationFile)
- [hobo.certbot](https://github.com/hobointhecorner/hobo.ansible.certbot)

Check [requirements.yml](./requirements.yml) for links and versions used.

## Initial setup

```shell
ansible-galaxy install -r requirements.yml
ansible-playbook install.yml -e certbot_request_cert=true
```
