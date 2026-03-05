University: [ITMO University](https://itmo.ru/ru/)<br />
Faculty: [FICT](https://fict.itmo.ru)<br />
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)<br /> 
Year: 2025/2026<br />
Group: K3323<br />
Author: Krestyanova Elisaveta Fedorovna<br />
Lab: Lab1<br />
Date of create: 05.03.2025<br />
Date of finished: ---<br />

# Задание

Данная работа предусматривает обучение развертыванию виртуальных машин (VM) и системы контроля конфигураций Ansible а также организации собственных VPN серверов.

Цель работы: развертывание виртуальной машины на базе платформы Microsoft Azure с установленной системой контроля конфигураций Ansible и установка CHR в VirtualBox

Ход работы:

Вам необходимо развернуть виртуальную машину с помощью Microsoft Azure в режиме студенческой подписки.

Если не получается в Microsoft Azure, можете выбрать любого бесплатного облачного провайдера

В бесплатном режиме Microsoft Azure предлагает для виртуальных машин только Ubuntu 16.4, нам нужна Ubuntu 18.+ поэтому необходимо обновить операционную систему. Сделать это можно с помощью данных команд:

```
sudo apt update & sudo apt upgrade
sudo do-release-upgrade
```

Теперь необходимо установить python3 и Ansible:

```
sudo apt install python3-pip
ls -la /usr/bin/python3.6
sudo pip3 install ansible
ansible --version
```

Далее вам необходимо на вашем компьютере установить VirtualBox а на него CHR (RouterOS).


После этого вам необходимо создать свой Wireguard/OpenVPN/L2TP сервер для организации VPN туннеля между вашим сервером автоматизации где был установлена система контроля конфигураций Ansible и вашим локальным CHR.


После всех манипуляций вам необходимо будет поднять VPN туннель между вашим VPN сервером на Ubuntu 18 и VPN клиентом на RouterOS (CHR)

# Схема

# Ход работы 

# Результаты

# Заключение

# Дополнительные источники
