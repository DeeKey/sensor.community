---
title: Драйвер и прошивка
---

Мы уже подготовили прошивку. Достаточно установить драйверы и прошить ваш NodeMCU (ESP8266). 

Для связи с NodeMCU (ESP8266) вам понадобятся драйверы для вашей операционной системы. 

Набор микросхем для NocdeMCU v3 обычно составляет CH341, просто проверьте обратную сторону NodeMCU (ESP8266), чтобы найти некоторую техническую информацию. 

Выберите ссылку, соответствующую операционной системе вашего компьютера.

Переведено с помощью www.DeepL.com/Translator (бесплатная версия)

We already prepared the firmware. You only have to install drivers and flash your NodeMCU (ESP8266). 

To communicate with your NodeMCU (ESP8266) you need usb2serial drivers for your operating system. 

The chipset for NocdeMCUs v3 is usually CH341, just check the back of your NodeMCU (ESP8266) to find some technical information. 

Choose the link that corresponds to the operating system of your computer.

### Windows

##### Драйвер для NodeMCU (ESP8266) V2 (чип CP2102) под Windows
* [Windows 10](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) - Windows 10 should be able to automatically download these
* [Windows 7/8/8.1](https://www.silabs.com/documents/public/software/CP210x_Windows_Drivers.zip) - 32-bit version - **not** supporting 64-bit version OS

##### Драйвер для NodeMCU (ESP8266) V3 (чип CH341) под Windows
* [Windows](http://www.wch.cn/downloads/file/5.html) - Windows 10 should be able to automatically download these

---

### MacOS

#####  Драйверы дя MacOS Drivers
* [NodeMCU V2](https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip )
* [NodeMCU V3](http://www.wch.cn/downloads/file/178.html) 

---

### Linux
Дополнительные драйверы не нужны. Все чипы должны поддерживаться системой (можно проверить командой dmesg)

---
### Прошивка устройства 

* Скачайте и запустите программу для прошивки процессора Flashing Tool:
https://github.com/opendata-stuttgart/airrohr-firmware-flasher/releases
    выберите версию для вашей ОС в разделе Assets внизу страницы:

** Linux: после загрузки файла выдайте ему разрешение на исполнение командой: `chmod o+x <download filename>` 

* Выберите из списка нужную прошивку. Обычно это файл latest_BME280_ru.bin который содержит русифицированную прошивку с поддержкой сенсора BME280.

* Подключите NodeMCU к компьютеру с помощью короткого кабеля micro-USB. Используйте кабель короче 1 метра, в противном случае соединение может быть нестабильно.

* После подключения должен определиться порт подключения. Если нет, то выберите порт вручную.

NB! Желательно прошивать процессор без подключенных датчиков или в устройстве, которое ранее уже исправно работало. Если какой-либо сенсор был неверно подключен, то программа может выдать ошибку подключения к процессору и прошить будет невозможно!

* Нажмите кнопку Upload. Должна произойти загрузка прошивки.

После того, как процесс загрузки прошивки завершится отсоедините процессор из порта USB и подсоедините снова. Тем самым вы перезагрузите его.