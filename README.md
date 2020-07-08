Разворачивет Zabbix в Vagrant по адресу 192.168.100.102, стенд поднимается из директории `./homework` по команде `vagrant up`, после поднятия на ВМ необходимо выполнить следующие команды:

```
sudo -u postgres createuser --pwprompt zabbix # запросит ввод пароля, для стенда устанавливался '12345678'
sudo -u postgres createdb -O zabbix zabbix
zcat /usr/share/doc/zabbix-server-pgsql*/create.sql.gz | sudo -u zabbix psql zabbix
```

Еще не нашёл проблему с юнитом, zabbix_server запускается с толкача

```
/usr/sbin/zabbix_server -c /etc/zabbix/zabbix_server.conf
```

Данные для подключения ВЕБ консоли

```
#zabbix_login: Admin/zabbix
#zabbix DBPassword: 12345678
#zabbix DBPort: 5432
```
