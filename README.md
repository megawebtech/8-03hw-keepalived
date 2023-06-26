# 8-03hw-keepalived
Задание 1

    Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.
    На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)
    Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).
    Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.
    На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.


Решение.

Меняю приоритеты на портах  Gi0/1 роутеров. 55 и 60.
Настраиваю track.

https://github.com/megawebtech/8-03hw-keepalived/blob/master/screenshot%20setting%20intGi01.JPG

ПРоверяю корректность настройки, разрываю кабель у свитча 0:

https://github.com/megawebtech/8-03hw-keepalived/blob/master/state%20after%20cutting%20wire.JPG

Проверяю, что поменялся приоритет:


https://github.com/megawebtech/8-03hw-keepalived/blob/master/screenshot%20sh%20standby%20br.JPG

ПРиоритет усменьшился на 10 (по умолчанию)


Ссылка на файл на схему CPT:

https://github.com/megawebtech/8-03hw-keepalived/blob/master/hsrp_advanced%20task%201.pkt

