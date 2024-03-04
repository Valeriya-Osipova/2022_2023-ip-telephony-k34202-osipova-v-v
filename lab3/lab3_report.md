## Отчет по лабораторной работе №3 "Использование Asterisk в качестве SIP proxy"

University: [ITMO University](https://itmo.ru/ru/)

Faculty: [FICT](https://fict.itmo.ru)

Course: [IP-telephony](https://github.com/itmo-ict-faculty/ip-telephony)

Year: 2023/2024

Group: K34202

Author: Osipova Valeriya Vladimirovna

Lab: Lab3

Date of create: 26.02.2024

Date of finished: 

### Цель работы
Изучить программный комплекс Asterisk. Настройка Asterisk для локальных звонков.

### Ход работы

1. Установим Asterisk на Ubuntu с помощью команды:

```
sudo apt-get install asterisk
```

2. Настройка SIP каналов. Добавляем в файл /etc/asterisk/sip.conf информацию о телефонах 1000 и 1001:

```
[1000]
type=friend
host=dynamic
secret=1000
context=ext_1000

[1001]
type=friend
host=dynamic
secret=1001
context=ext_1001
```


Добавляем в файл /etc/asterisk/extensions.conf:

```
[ext_1000]
exten => _XXXX,1,Dial(SIP/${EXTEN})

[ext_1001]
exten => _XXXX,1,Dial(SIP/${EXTEN})

3. Перезапускаем Asterisk командой:

```
sudo service asterisk restart
```

4. Проверяем статус:

```
sudo systemctl status asterisk
```

Сервис запущен.

5. В качестве soft-телефона устанавливаем Zoiper5 с официального сайта, при входе вводим данные телефона 1000, указываем localhost:

![image](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/d98440cc-9817-42ef-90e4-b1ea3eae0758)
![image](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/9adf2d19-9319-43a9-bce9-8a92746f2f05)

6. Проверим подключение:

```
sudo asterisk -r
sip show peers
```

![Скриншот 04-03-2024 195525](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/236349b4-9ea6-4031-aca2-61a4605b8ed8)

7. Установим и настроим MicroSIP для телефона 1001:

![Uploading image.png…]()

8. Совершим звонок с телефона 1001 на 1000, чтобы проверить соединение:

![Скриншот 04-03-2024 192306](https://github.com/Valeriya-Osipova/2023_2024-ip-telephony-k34202-osipova-v-v/assets/64967406/906e6a7b-1329-4962-b7ff-ca0cd0123a1e)

### Вывод
В результате выполнения данной лабораторной работы удалось изучить программный комплекс Asterisk. Был настроен Asterisk для локальных звонков.
