# LAB 1
University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)
Year: 2024/2025
Group: K34202
Author: Subbota Anton Dmitrievich
Lab: Lab1
Date of create: 25.09.2024
Date of finished: 25.09.2024
## Цель 

Целью данной работы является развертывание виртуальной машины на базе платформы Microsoft Azure с установленной системой контроля конфигураций Ansible и установка CHR в VirtualBox

## Выполнение

1. Был установлен Python.

![alt text](img/image.png)

![alt text](img/image-1.png)

2. Был установлен ansible.

![alt text](img/image-2.png)

3. Была взята VDS в Selectel, в которой и будет установлен VPN сервер, а именно OpenVPN.

![alt text](img/image-3.png)

4. Был поднят OpenVPN сервер на VDS.

![alt text](img/image-4.png)

![alt text](img/image-5.png)

4.1. Был создан сертификат сервера.

![alt text](img/image-12.png)

4.2. Был создан сертификат клиента.

![alt text](img/image-13.png)

4.3. Создаем конфигурационный файл OpenVPN сервера.

![alt text](img/image-14.png)

4.4. Настраиваем скрипты для сетевого окружения OpenVPN сервера.

![alt text](img/image-15.png)



5. Сделаны сертификат и ключ, полученные при создании OpenVPN сервера.

![alt text](img/image-6.png)

6. Была создана ВРМ c CHR на Virtualbox.

![alt text](img/image-7.png)

7. Были загружены сертификат и клиентский ключ на CHR.

8. Был создан туннель к OpenVPN с CHR.

![alt text](img/image-8.png)

9. Клиент получил адрес от VPN сервера.

![alt text](img/image-9.png)

10. Была проверена работоспособность с сервера и клиента.

![alt text](img/image-10.png)

![alt text](img/image-11.png)

## Вывод

Была развернута виртуальная машина и установлена CHR, на базе Select VDS был установлен Ansible и поднят OpenVPN сервер. Между CHR и VDS настроен VPN туннель.
