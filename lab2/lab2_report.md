University: [ITMO University](https://itmo.ru/ru/)<br />
Faculty: [FICT](https://fict.itmo.ru)<br />
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)<br /> 
Year: 2025/2026<br />
Group: K3323<br />
Author: Krestyanova Elisaveta Fedorovna<br />
Lab: Lab2<br />
Date of create: 13.03.2026<br />
Date of finished: ---<br />

# Задание

В данной лабораторной работе вы на практике ознакомитесь с системой управления конфигурацией Ansible, использующаяся для автоматизации настройки и развертывания программного обеспечения.

Цель работы: С помощью Ansible настроить несколько сетевых устройств и собрать информацию о них. Правильно собрать файл Inventory.

Ход работы:

- Установить второй CHR на своем ПК.
- Организовать второй OVPN Client на втором CHR.
- Используя Ansible, настроить сразу на 2-х CHR:
    логин/пароль;

    NTP Client;

    OSPF с указанием Router ID; 4. Собрать данные по OSPF топологии и полный конфиг устройства.


# Схема

# Ход работы 

## Конфигурация 2-й роутера

При клонировании контейнера на нём dhcp-клиент перестал видеть нужный интерфейс валидным. В winbox я заново в настройках dhcp-клиента выбрала интерфейс ether2, и он очнулся, получив новый айпи-адрес.

![dhcp-клиент 2-го роутера](images/1-1.png)

Меняем адрес на новый 10.220.220.3:

![Смена адреса](images/1-2.png)

Создаём снова интерфейс, чтобы пересоздать ключи:

![Пересоздание ключей](images/1-3.png)

Публичный ключ CHR2:
nep4zIqCurxKpQLPhwhycdFvMTnf/mOqAJWw3MgJEVw=

Привязываем снова айпи адрес к интерфейсу туннеля:

![Привязка айпи-адреса](images/1-4.png)

И шлюз:

![Привязка шлюза](images/1-5.png)

А в конфиг VPS добавляем соотвествующий пир:

```
[Peer]
# CHR 2
PublicKey = nep4zIqCurxKpQLPhwhycdFvMTnf/mOqAJWw3MgJEVw=
AllowedIPs = 10.220.220.3/32
PersistentKeepalive = 25
```

Проверяем:

![Пинг с VPS](images/1-6.png)

![Связность роутеров](images/1-7.png)

# Результаты

# Заключение

# Дополнительные источники
