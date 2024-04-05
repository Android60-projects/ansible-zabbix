# Zabbix server playbook
```
ANSIBLE_HOST_KEY_CHECKING=False ansible-playbook -u ubuntu -K -e "mysql_root_password=password" -i 192.168.100.119, main.yml
```