# Лаб. работа №3. Ansible advanced

Создаем файл с ip адресами управляемых хостов `inventory.ini`  

Создаем файл с именами сканируемых хостов `targets.txt`  

Создаем файл сценариев ansible `playbook.yml`  

Плейбук будет состоять из одного сценария `Scan ports with Nmap`  
Используем список хостов `webservers`  
Подключемся к управляемым хостам под пользователем `runner`  
Повышаем привелегии пользователя при помощи `sudo`  

Расписываем задачи:  
1. убеждаемся что Nmap установлен, если нет - устанавливаем, используем модуль `apt`  
2. копируем файл с целями для сканирования `tartets.txt` на оба хоста, используем модуль `copy`  
3. запускаем Nmap с параметрами в командной строке, результат выполнения команды регистрируем в переменной `nmap_results`, используем модуль `command`  
4. выводим содержимое переменной `nmap_results` при помощи модуля `debug`  

Проверяем playbook на ошибки:  
`ansible-playbook playbook.yml -i inventory.ini --check`

Запускаем playbook из текущей директории:  
`ansible-playbook playbook.yml -i inventory.ini`  
или при помощи скрипта `run.sh`

Результат выполнения сценария:  
<img width="841" height="383" alt="image" src="https://github.com/user-attachments/assets/c78fca1e-ae8f-4846-a7b7-de1b269dbfa6" />


