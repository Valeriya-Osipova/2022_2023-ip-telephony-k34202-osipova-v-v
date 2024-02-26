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

### 1 часть

1. В среде cisco packet tracer была реализована схема следующего вида:

<img width="251" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/eefb3663-d6bb-4caf-8a27-02b75d1a89cb">


2. В конфигурационном режиме изменяем название маршрутизатора на CMERouter:

<img width="520" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/e158b4b7-8589-46f6-a226-adc6ee6d1fb4">


3. Отключим синтаксис ввода слов от DNS серверов.

<img width="364" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/cc6e71e2-72be-4fe0-8d2a-95de47fc1d7d">


4. Зададим пароли для защиты маршрутизатора как в удаленном режиме, так и в режиме консоли.

<img width="456" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/73db51c4-6e57-4e7c-a115-7e8ed996829b">


5. Настроим интерфейс fa0/0 на маршрутизаторе Cisco 2811 (CMERouter).

<img width="375" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/6ab2aee4-8784-48e1-9282-557ec9873f89">


6. Настроим DHCP сервера для передачи голоса и данных на маршрутизаторе Cisco 2811.

<img width="336" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/434f0dc1-88b5-4027-bbef-d11d5c45c220">


7. Настроим услуги телефонии Cisco CallManager Express на маршрутизаторе 2811.

<img width="458" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/b5ee5f7f-b244-4824-9ab9-bd0b1706fb75">


8. Создадим VLAN порты на коммутаторе Cisco Catalyst 3560 для взаимодействия коммутатора с маршрутизатором и подключим IP телефоны.

<img width="419" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/d999f37f-57b2-4e38-853f-18a40366a4d9">


9. Настроим IP-телефоны и соединим с коммутатором Cisco Catalyst 3560.

<img width="532" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/2b29cafc-4a49-4a04-b629-163e33749135">


10. Проверим звонки между телефонами и проверим остальные сервисы:

<img width="685" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/463f2e3c-4f3f-46c8-b88f-d5d31c155829">

<img width="695" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/89704da8-17c9-4552-935f-7aca1eff1599">


### 2 часть

В данной части работы была реализована схема следующего вида: 

Создадим два VLAN порта на коммутаторе для взаимодействия коммутатора с маршрутизатором и подключить IP телефоны.

<img width="360" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/3d49a13e-9fd6-41e8-96c5-3c0f8da50c0a">

Интерфейс коммутатора переводим в режим trunk

<img width="344" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/ed69fe2e-67b1-40e6-87e9-5d822f9019ea">


Настроим другие интерфейсы коммутатора:

<img width="349" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/fc8f2c77-2baf-412e-b14b-8132e934c6bb">

На маршрутизаторе настроим DHCP-сервер для компьютеров и для телефонов:

<img width="354" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/8a42e87e-f639-4d41-b308-ff0a1b17209d">

На маршрутизаторе поднимаем саб-интерфейсы, соответсвующие vlan и назначаем им ip адреса:

<img width="565" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/122a123b-df39-4906-bfe3-38ab36a738e8">

<img width="677" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/6ab3cdab-a8db-4824-8d08-f48c83b36cb7">

Настроим телефоны

<img width="549" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/f600c35d-6d3c-4cc5-989e-14226a0e5bde">

<img width="325" alt="Снимок экрана 2024-02-24 113622" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/593de7f3-a64e-40ad-9ae7-1302a598ec15">


На PC включим DHCP:

<img width="519" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/262f5ce0-c0c0-432c-b9e5-33dbda02103b">


Проверим связность:

Выполним пинг между компьютерами:

<img width="428" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/162f2460-aca6-466d-b899-86c9c169025e">
<img width="342" alt="image" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/d0cf4114-c38b-4d3d-8c15-dd38c2cc39cb">


Выполним звонок между телефонами: 

<img width="661" alt="Снимок экрана 2024-02-24 113801" src="https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/fbd5e671-39d9-4bf3-87f3-4af68a5e99ad">


### Вывод
В результате выполнения данной лабораторной работы удалось изучить построение сети IP-телефонии с помощью маршрутизатора Cisco 2811, коммутатора Cisco catalyst 3560 и IP телефонов Cisco 7960.



