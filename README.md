# Zabbix server playbook
This repo contains playbook that will setup Zabbix server using roles by [robertdebock](https://github.com/robertdebock).

## Install required roles
```
ansible-galaxy install -r requirements.yaml
```

## Run playbook
```
ansible-playbook -u ubuntu -K -e "mysql_root_password=password" -i 192.168.100.119, main.yml
```