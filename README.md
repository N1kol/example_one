# Ansible + Docker: Автоматизация развертывания PostgreSQL 
Ansible-плейбук для автоматической установки Docker на Ubuntu и запуска PostgreSQL в контейнере.  

##  Стек технологий  
- Ansible (автоматизация)  
- Docker (контейнеризация)  
- PostgreSQL (СУБД)

##  Как запустить  
### Требования  
- Ubuntu 20.04/22.04  
- Ansible 2.7+  

## Инструкция 
0. В данном примере в качесте файла инвентори используется стандартный файл - /etc/ansible/hosts
x.x.x.x ansible_user=root ansible_python_interpreter=/usr/bin/python3 (В моем случае было необходимо указать интерпретатор явно)

1. Клонируйте репозиторий:  
git clone https://github.com/N1kol/example_one.git

2. Перейдите в директорию с плейбуком

3. Запустите плейбук:
ansible-playbook playbook.yml  

## Проверка работы
1. Проверьте статус контейнера:
docker ps

2. Подключитесь к PostgreSQL:
psql -h localhost -U postgres
