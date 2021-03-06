---
title: Конфигурация устройства
---
Внимание: если вы ранее настраивали устройство для работы в своей сети, то повторная настройка вам не требуется!

1. Подсоедините измерительную станцию с помощью USB кабеля к питанию.
2. Станция попытается соединиться к вашей WiFi сети. Если устройство только было прошито или вы изменили пароль WiFi сети то станция не сможет подключиться  и поднимет собственную сеть WiFi с именем `airRohr-ID`. Где **ID** это серийный номер процессора ESP8266. **Пожалуйста запишите этот номер, так как он потребуется вам дляьше для регистрации станции на сервере приема данных.**
3. На своем компьютере (или смартфона) войдите в меню поиска сетей WiFi и дождитесь появления указанной выше сети (это может занять до 5 минут, если сеть не появилась, выключите и включите станцию). Подключитесь к сети станции.
   <br>*Android*: Если соединение было сразу после подключение разорвано, то вам, возможно, нужно деактивировать опцию 'интеллектуальный сетевой коммутатор (Smart network switch)' в разделе 'Соединения -> WiFi -> Дополнительно'. Актуально для теефонов марки Samsung.
4. Как только вы подключились в браузере наберите адрес 192.168.4.1 либо
   http://airRohr-ХХХХХХХ.local (где Х  серийный номер процессора ESP8266).
5. Должно открыться меню первичной настройки устройства. В меню выберите из списка сетей вашу домашнюю сеть и введите пароль от сети. После чего нажмите кнопку  'Сохранить и перезапустить'
6. Подключите ваш компьютер обратно к вашей домашней сети.
   Если вы ввели пароль правильно и устройство подключилось в вашу локальную сеть, то теперь оно должно быть доступно по IP адресу, который был выдан в вашей сети (не путайе его с адресом 192.168.4.1, который использовался в шагах выше!).
   Если же станция в вашей сети не появилась, а вновь подняла собственную сеть, то это значит, что вы где-то ошиблись и вам надо повторить все шаги снова.

### Как узнать IP станции

Для того, чтобы узнать IP адрес устройства можно воспользоваться одним из способов:
* открыть меню настройки вашего домашнего роутера и посмотреть там в списке подключенных к сети устройств.
* воспользоваться программой Flashing Tool, которую ранее использовали для прошивки станции. В программе надо открыть вкладку Discovery и нажмите кнопку Refresh. Должна появиться строка с адресом устройства в вашей локальной сети.

<br>

<img src="../docs/airrohr_config_initial.jpg" loading="lazy"/>
<br>

### Как убедится, что станция отсылает данные

Если вы не делали никаких иных изменений настроек, нежели чем описано выше, то станция начнет отсылать данные. После 10 минут работы вы можете посмотреть накопленные данные на [этом сайте](https://www.madavi.de/sensor/graph.php) введя **ID** станции (серийный номер процессора ESP8266).
