# LAB 1

## Цель 

Целью данной работы является развертывание виртуальной машины на базе платформы Microsoft Azure с установленной системой контроля конфигураций Ansible и установка CHR в VirtualBox

## Задание 

Вам необходимо развернуть виртуальную машину с помощью Microsoft Azure в режиме студенческой подписки.
Если не получается в Microsoft Azure, можете выбрать любого бесплатного облачного провайдера

В бесплатном режиме Microsoft Azure предлагает для виртуальных машин только Ubuntu 16.4, нам нужна Ubuntu 18.+ поэтому необходимо обновить операционную систему. Сделать это можно с помощью данных команд:
sudo apt update & sudo apt upgrade
sudo do-release-upgrade
Теперь необходимо установить python3 и Ansible:
sudo apt install python3-pip
ls -la /usr/bin/python3.6
sudo pip3 install ansible
ansible --version
Далее вам необходимо на вашем компьютере установить VirtualBox а на него CHR (RouterOS).
В интернете есть инструкции по установке CHR на VirtualBox, одна из этих инструкций вам поможет.

После этого вам необходимо создать свой Wireguard/OpenVPN/L2TP сервер для организации VPN туннеля между вашим сервером автоматизации где был установлена система контроля конфигураций Ansible и вашим локальным CHR.
В интернете есть инструкции по установке Wireguard/OpenVPN/L2TP сервер для Ubuntu 18, одна из этих инструкций вам поможет.

После всех манипуляций вам необходимо будет поднять VPN туннель между вашим VPN сервером на Ubuntu 18 и VPN клиентом на RouterOS (CHR)
Что искать? («Название вашего протокола» клиент RouterOS).

## Выполнение

1. Был установлен Python.

![alt text](image.png)

![alt text](image-1.png)

2. Был установлен ansible.

![alt text](image-2.png)

3. Была взята VDS в Selectel, в которой и будет установлен VPN сервер, а именно OpenVPN.

![alt text](image-3.png)

4. Был поднят OpenVPN сервер на VDS.

![alt text](image-4.png)

![alt text](image-5.png)

5. Сделаны сертификат и ключ, полученные при создании OpenVPN сервера.

![alt text](image-6.png)

6. Была создана ВРМ c CHR на Virtualbox.

![alt text](image-7.png)

7. Были загружены сертификат и клиентский ключ на CHR.

8. Был создан туннель к OpenVPN с CHR.

![alt text](image-8.png)

9. Клиент получил адрес от VPN сервера.

![alt text](image-9.png)

10. Была проверена работоспособность с сервера и клиента.

![alt text](image-10.png)

![alt text](image-11.png)

## Вывод

Была развернута виртуальная машина и установлена CHR, на базе Select VDS был установлен Ansible и поднят OpenVPN сервер. Между CHR и VDS настроен VPN туннель.
