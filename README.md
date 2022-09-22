# Otus_project
Итоговый проект для Otus на тему "Быстрое восстановление инфраструктуры FrontEnd, BackEnd, БД, Мониторинг"

Описание:
Стенд состоит из трех виртуальных машин на базе ОС Сentos 7. На первой машине (master): nginx, appache, СУБД mysql в роли master, node_exporter, mysql_exporter. На второй машине (slave): appache, СУБД mysql в роли replica, node_exporter, mysql_exporter, скрипт бекапа базы данных. На третьей машине (monitoring_backup): prometheus, grafana и бэкапы. Не предусмотрена централизованная установка. Скрипты необходимо выполнять на каждой машине.
