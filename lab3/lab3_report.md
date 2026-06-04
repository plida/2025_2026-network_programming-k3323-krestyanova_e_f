University: [ITMO University](https://itmo.ru/ru/)<br />
Faculty: [FICT](https://fict.itmo.ru)<br />
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)<br /> 
Year: 2025/2026<br />
Group: K3323<br />
Author: Krestyanova Elisaveta Fedorovna<br />
Lab: Lab3<br />
Date of create: ---<br />
Date of finished: ---<br />

# Задание

В данной лабораторной работе вы ознакомитесь с интеграцией Ansible и Netbox и изучите методы сбора информации с помощью данной интеграции.

Цель работы: c помощью Ansible и Netbox собрать всю возможную информацию об устройствах и сохранить их в отдельном файле.

Ход работы:

1. Поднять Netbox на дополнительной VM.
2. Заполнить всю возможную информацию о ваших CHR в Netbox.
3. Используя Ansible и роли для Netbox в тестовом режиме сохранить все данные из Netbox в отдельный файл, результат приложить в отчёт.
4. Написать сценарий, при котором на основе данных из Netbox можно настроить 2 CHR, изменить имя устройства, добавить IP адрес на устройство.
5. Написать сценарий, позволяющий собрать серийный номер устройства и вносящий серийный номер в Netbox.


# Схема

# Ход работы 

В VirtualBox создаём новую виртуальную машину: Ubuntu Live server 26.04.

Netbox будем устанавливать через Docker. На виртуальной машине устанавливаем Docker 

docker compose exec netbox /opt/netbox/netbox/manage.py createsuperuser

Пришлось выключить включить контейнер, выключить включить докер и тогда я только смогла зайти 

![alt text](images/image.png)

![site](images/image-1.png)

![alt text](images/image-2.png)

![alt text](images/image-3.png)

Device role: ![alt text](images/image-4.png)

Device type: ![alt text](images/image-5.png)

![alt text](images/image-6.png)

![alt text](images/image-7.png)

![alt text](images/image-8.png)

installed wireguard on ubuntu vm 

connected tunnel

![alt text](images/image-9.png)

![alt text](images/image-10.png)

![alt text](images/image-11.png)

![alt text](images/image-12.png)

![alt text](images/image-13.png)

![alt text](images/image-14.png)

![alt text](images/image-15.png)

for json_query installed jmsepath 

Использование динамического инвентаря

![alt text](images/image-17.png)

![alt text](images/image-16.png)

![alt text](images/image-18.png)

![alt text](images/image-19.png)

Удалила адрес loopback, он успешно добавился

![alt text](images/image-20.png)

![alt text](images/image-21.png)

# Результаты

# Заключение

# Дополнительные источники
