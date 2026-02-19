Домашнее задание

Создан внешний хост IP 84.252.129.211  пользователь centos  +  сертификат для netology
![alt text](image.png)

Внесен в inventory
![alt text](image-2.png)

Прописал креды, готов запускать.
![alt text](image-3.png)

Пинг - ок

![alt text](image-4.png)

Видим что он скачал версию для x86 и выполнился успешно.
![alt text](image-5.png)

Добавление хоста Vector:
Добавили в инвентори
![alt text](image-6.png)

Проверяем связь - ok.
![alt text](image-7.png)

Проверка конфига:
![alt text](image-8.png)
![ Фиксим  ](image-9.png)
![alt text](image-10.png)

Запуск playbook Tasks должны: скачать дистрибутив нужной версии, выполнить распаковку в /home/centos, установить vector.
![alt text](image-11.png)
![alt text](image-12.png)

Установка ansible lint  
![alt text](image-13.png)
![alt text](image-14.png)

Проверка показала наличие нескольких видов ошибок. Исправляем.
![alt text](image-15.png)

Часть ошибок пофикшено:
![alt text](image-16.png)
и еще:
![alt text](image-17.png)

Готово:
![alt text](image-18.png)

![alt text](image-19.png)

Запуск с флагом --check
ansible-playbook -i inventory/prod.yml site.yml --check

![alt text](image-20.png)
![alt text](image-21.png)

Запуск с флагом  --diff
ansible-playbook -i inventory/prod.yml site.yml --diff

![alt text](image-22.png)
![alt text](image-23.png)

Запускаем и смотрим иденпотентен ли playbook

![alt text](image-24.png)
![alt text](image-25.png)

https://github.com/vegorshkov/ansible-dz02/tree/08-ansible-02-playbook 

