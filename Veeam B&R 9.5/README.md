# Шаблон для получения данных из Veeam
## Что умеет
Простенький скрипт, умеет получать: 
1. Имя задачи
2. Статус последнего выполнения задачи
3. Дата полседнего успешного выполнения задачи
## Установка
1. Скопировать скрипт veeam.ps1 в папку C:\Zabbix\script
2. Добавить в zabbix_agentd.conf строку:
```
UserParameter=Veeam[*],powershell -File C:\Zabbix\script\veeam.ps1 "$1" "$2"
```
3. Импортировать шаблон в Zabbix

