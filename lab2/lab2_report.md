## Отчет по лабораторной работе №2 "Конфигурация voip в среде Сisco packet tracer"

University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)

Year: 2023/2024

Group: K34202

Author: Osipova Valeriya Vladimirovna

Lab: Lab2

Date of create: 21.02.2024

Date of finished: 

### Цель работы
Изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.

### Ход работы

#### 1 часть

В среде cisco packet tracer была реализована схема следующего вида:

<img width="165" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/749e1c9a-c07b-4262-9554-9cb87497ed8c">

В конфигурационном режиме изменяем название маршрутизатора на CMERouter:

<img width="500" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/e158b4b7-8589-46f6-a226-adc6ee6d1fb4">

Отключим синтаксис ввода слов от DNS серверов.

<img width="344" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/cc6e71e2-72be-4fe0-8d2a-95de47fc1d7d">

Зададим пароли для защиты маршрутизатора как в удаленном режиме, так и в режиме консоли.

<img width="436" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/73db51c4-6e57-4e7c-a115-7e8ed996829b">

Настроим интерфейс fa0/0 на маршрутизаторе Cisco 2811 (CMERouter).

<img width="355" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/6ab2aee4-8784-48e1-9282-557ec9873f89">

Настроим DHCP сервера для передачи голоса и данных на маршрутизаторе Cisco 2811.

<img width="316" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/434f0dc1-88b5-4027-bbef-d11d5c45c220">

Настроим услуги телефонии Cisco CallManager Express на маршрутизаторе 2811.

<img width="428" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/b5ee5f7f-b244-4824-9ab9-bd0b1706fb75">

Создать VLAN порты на коммутаторе Cisco Catalyst 3560 для взаимодействия коммутатора с маршрутизатором и подключить IP телефоны.



