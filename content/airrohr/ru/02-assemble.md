---
title: Сборка 
---

> ⚠️ **Важное замечание**
До того, как приступать к сборке и подсоединять сенсоры нужно прошить и проверить процессор ESP8266!

### Подключение сенсора частиц SDS011

С сенсором SDS011 идет провод, подключенный к USB плате. Его можно использовать для подключения к контроллеру ESP8266 после небольшой доработки.

1. Отсоедините контакт от USB платы (сама USB плата более не понадобится):

![SDS011_step_01](../docs/airrohr/sds_01.png)

2. Надавите острым предметом на выступающую часть разъема и немного потяните за провод. 
**Внимание!** Не вырывайте провод из разъема слишком сильно! Он должен выходить легко.

![SDS011_step_02](../docs/airrohr/sds_02.png)

3. Высвободившийся из центра провод вставьте в крайний разъем так, чтобы он надежно зафиксировался.

![SDS011_step_03](../docs/airrohr/sds_03.png)

4. При помощи острого ножа сделайте разрез посередине.

![SDS011_step_04](../docs/airrohr/sds_04.png)

5. После разреза должно образоваться два разъема. Зачистите оба места среза чтобы получить ровную поверхность (может мешать присоединению других разъемов).

![SDS011_step_05](../docs/airrohr/sds_05.png)

6. Подсоедините разъемы сенсора SDS011 к процессору ESP8266 так, чтобы пластмассовые выступы на разъемах смотрели друг на друга (внутрь платы):

![SDS011_step_06](../docs/airrohr/sds_06.png)

7. Сами разъем надо установить во 2 и 3 контакты пропустив первый (нумерация с противоположной стороны от разъема USB)

![SDS011_step_07](../docs/airrohr/sds_07.png)

8. Для более надежной фиксации контактов на контроллере можно воспользоваться хомутом или термоклеем.

![SDS011_step_08](../docs/airrohr/sds_08.png)

Еще раз проверьте ваше подключение по схеме. Неправильное подключение питания датчика (переполюсовка) может повредить сенсор! Убедитесь, что 5V с датчика приходит на VU контроллера, а GND (ground - земля) соединена с контактом G на плате контроллера:

```bash
SDS011 разъем 1 -> разъем D1 / GPIO5
SDS011 разъем 2 -> разъем D2 / GPIO4
SDS011 разъем 3 -> GND
SDS011 разъем 4 -> не используется
SDS011 разъем 5 -> VU (NodeMCU v3) / VIN (NodeMCU v1,v2)
SDS011 разъем 6 -> не используется
SDS011 разъем 7 -> не используется
```

### Подсоединение сенсора BME280

Датчик BME280 обычно поставляется отдельно от контактных ножек и их необходимо припаять. Если вы не умеете это делать, то можно обратится в ремонт бытовой техники или мобильных телефонов, где вам, возможно, все сделают прямо при вас за несколько минут за небольшую плату.

Отделите четыре провода и подсоедините их параллельно друг к другу контактами (в середине разъема) вовнутрь как показано на фото ниже:

```bash
BME280 | NodeMCU
VIN -> Разъем 3V3 (3.3V)
GND->  GND/G
SDA -> Разъем D3
SCL -> Разъем D4
```

### Tie everything together

 ##### Tie NodeMCU and SDS011 together
<img src="../docs/airrohr/tie-air-quality-sensor-together.jpeg"/>
Use a cable tie to link the NodeMCU (ESP8266) and the SDS011 sensor so that the Wifi antenna points away from the sensor

 ##### Connect flexible tube
 <img src="../docs/airrohr/sds011-with-tube.jpeg" style="width:49%; padding-right: 0.5em"/>
 <img src="../docs/airrohr/bme280-tied-to-tube.jpeg" style="width:49%;">
 
* connect the flexible tube to the SDS011 sensor
* Use another cable tie to attach the BME280 temperature sensor to the tube
* Pass the USB cable through the tube. Mount the SDS011 with the NodeMCU facing to the top and the fan facing to the bottom

 
 ##### Push in sensor into the pipe
* Push the parts into the tube, so it's jammed inside
* USB cable, flexible tube and BME280 should look out of the tube's end
* Push the other pipe onto the first one.

<img src="../docs/airrohr/sds011-jammed-into-tube.jpeg"/>

 ##### Finishing
* Position the temperature sensor on the flexible tube, so that it's on the edge of the pipe.
* Cut off the flexible tube at the end of the pipe
* Optional: you can cover the open ends of the tube with a fine mesh. So air can circulate but insects stay outside
 
<img src="../docs/airrohr/position-bme280.jpeg"/>
