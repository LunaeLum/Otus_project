# Otus_project
Итоговый проект для Otus на тему "Быстрое восстановление инфраструктуры FrontEnd, BackEnd, БД, Мониторинг"

Описание:
Стенд состоит из трех виртуальных машин на базе ОС Сentos 7. На первой машине (master): nginx, appache, СУБД mysql в роли master, node_exporter, mysql_exporter. На второй машине (slave): appache, СУБД mysql в роли replica, node_exporter, mysql_exporter, скрипт бекапа базы данных. На третьей машине (monitoring_backup): prometheus, grafana и бэкапы. Не предусмотрена централизованная установка. Скрипты необходимо выполнять на каждой машине.

Все скрипты, указанные далее, должны выполняться с правами администратора (sudo bash имя_скрипта или под учетной записью root).

Настройка master:
1. Выполните selinux_firewalld_disable для отключения selinux и firewalld
2. Выполните static_ip_script для настройки статического ip адреса на интерфейсе enp0s3
3. Выполните nginx_install для установки сервера nginx в качестве FrontEnd
4. Выполните apache_install для установки сервера Apache в качестве BackEnd
5. Выполните mysql_install_master для установки СУБД MySQL в роли master.
6. Выполните node_exporter_install для возможности подключения данного сервера к мониторингу prometeus
7. Выполните mysql_exporter_install для возможности подключения СУБД MySQL к мониторингу prometeus

Настройка slave:
1. Выполните selinux_firewalld_disable для отключения selinux и firewalld
2. Выполните static_ip_script для настройки статического ip адреса на интерфейсе enp0s3
3. Выполните mysql_install_slave для установки СУБД MySQL в роли slave.
4. Выполните node_exporter_install для возможности подключения данного сервера к мониторингу prometeus
5. Выполните mysql_exporter_install для возможности подключения СУБД MySQL к мониторингу prometeus
6. Настройте скрипт mysql_backup и настройте его повторение в cron

Настройка monitoring_backup:
1. Выполните selinux_firewalld_disable для отключения selinux и firewalld
2. Выполните static_ip_script для настройки статического ip адреса на интерфейсе enp0s3
3. Выполните prometheus_install для установуи системы мониторинга Prometeus
4. Выполните grafana_install для установки grafana

Вы восхитительны!
