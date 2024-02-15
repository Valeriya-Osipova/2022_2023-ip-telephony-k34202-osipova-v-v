## Отчет по лабораторной работе №1 "Базовая настройка ip-телефонов в среде Сisco packet tracer"

University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)

Year: 2023/2024

Group: K34202

Author: Osipova Valeriya Vladimirovna

Lab: Lab1

Date of create: 15.02.2024

Date of finished: 

### Цель работы
Изучить рабочую среду Cisco Packet Tracer, ознакомиться с интерфейсами основных устройств, типами кабелей, научиться собирать топологию. Изучить построение сети IP-телефонии с помощью маршрутизатора, коммутатора и IP телефонов Cisco 7960 в среде Packet tracer.

### Ход работы

#### 1 часть

1. Собираем схему соединения, указанную на рисунке

![схема drawio](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/e068d953-1b32-4213-8667-90387c9b1a86)

В Cisco Packet Tracer схема преобретает следующий вид:

![image](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/9f5a7ee0-3358-4650-8349-d0e593a58c61)

2. Присвоим компьютерам статические IP-адреса 192.168.0.1 - 192.168.0.7, как показано на схеме выше, с маской 255.255.255.0.

![image](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/131957d2-a943-44d5-8f26-abaaa91fab05)

![image](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/3006be0b-4aff-4d16-aed5-14897fb3367e)

3. Выполняем команду ping на разных ПК, чтобы проверить связность. Убеждаемся, что любой компьютер посредством пинга успешно передает пакеты любому другому компьютеры на схеме. Пример пинга:

![image](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/4acabaea-5b98-4b5d-9920-e8d766a291fe)

#### 2 часть

1. Собираем схему соединения, указанную на рисунке

![схема2 drawio](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/5cfa828a-ae1d-4eeb-878b-1cdd741e2dd9)

2. Изменяем имя маршрутизатора на CMERouter

```
Router(config)#hostname CMERouter
CMERouter(config)#
```

3. Настраиваем интерфейс fa0/0 на маршрутизаторе CMERouter, направленный на коммутатор. Присвоим ему IP-адрес 192.168.0.1 с маской 255.255.255.0

```
CMERouter(config)#interface FastEthernet0/0
CMERouter(config-if)#ip address 192.168.0.1 255.255.255.0
```

4. 
