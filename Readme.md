Лабораторная работа. Базовая настройка коммутатора. Часть 1.
--------------------------------------------------

Топология.

<img src="https://i.ibb.co/FX0VBpK/Lab1.jpg" alt="Lab1" border="0"></a>

Для выполнения лабораторной работы был выбран свитч Cisco 2960 cо следующей конфигурацией:

<a href="https://ibb.co/cx4y8Cq"><img src="https://i.ibb.co/GFzdMtm/Lab1-2.jpg" alt="Lab1-2" border="0"></a>

При анализе конфигурации свитча созданных сетей VLAN обнаружено не было:

<a href="https://ibb.co/Wc3hhq7"><img src="https://i.ibb.co/y8R99GK/Lab1-3.jpg" alt="Lab1-3" border="0"></a>)

Также было выполнено удаление загрузочной информации из NVRAM с последующей перезагрузкой устройства:
<a href="https://ibb.co/5krDV6R"><img src="https://i.ibb.co/8br3V07/Lab1-33.jpg" alt="Lab1-33" border="0"></a>
<a href="https://ibb.co/9Y88Gg4"><img src="https://i.ibb.co/dKWW7Mp/Lab1-4.jpg" alt="Lab1-4" border="0"></a>

<a href="https://ibb.co/ZK7TnQv"><img src="https://i.ibb.co/MpQNYzK/Lab1-5.jpg" alt="Lab1-5" border="0"></a>

Для эмуляции соединения ПК и свитча использовался Cisco Packet Tracer 6.2. ПК был подключён к устройству через консольный порт, затем был использован стандартный эмулятор терминального подключения Cisco Packet Tracer.
<a href="https://ibb.co/Cb6Qkvc"><img src="https://i.ibb.co/sKCq0Qf/Lab1-7.jpg" alt="Lab1-7" border="0"></a>

### Контрольный вопрос: Почему нужно использовать консольное подключение для первоначальной настройки коммутатора? Почему нельзя подключиться к коммутатору через Telnet или SSH? 

### Ответ: Подключение по консоли доступно без пароля, в отличие от telnet или ssh, для которых нужны дополнительные настройки линий.


При изучении файла Running Config была получена следующая информация: 

<a href="https://ibb.co/yNw0ZyX"><img src="https://i.ibb.co/Rgx2s09/Lab1-81.jpg" alt="Lab1-81" border="0"></a>

<a href="https://ibb.co/wRPJpS8"><img src="https://i.ibb.co/mG2vh9d/Lab1-82.jpg" alt="Lab1-82" border="0"></a>

На свитче Cisco 2960 имеется 24 порта FastEthernet и 2 порта GigabitEthernet Также имеются два диапазона линий vty: c 0 по 4 и с 5 по 15.

Далее при попытке просмотреть информацию о загрузочной конфигурации, появилось сообщение: 

<a href="https://imgbb.com/"><img src="https://i.ibb.co/n01bJf1/Lab1-9.jpg" alt="Lab1-9" border="0"></a>

Причина появления данного сообщения состоит в том, что не была создана запись загрузочной конфигурации путём выполнения команды: copy running config startup config.

Также в конфигурации видно, что на свитче отсутствует ip-адресс SVI. VLAN 1 находится в состоянии "shutown".

<a href="https://imgbb.com/"><img src="https://i.ibb.co/d6m8gmh/Lab1-10.jpg" alt="Lab1-10" border="0"></a>

После выполнения команды Show interfaces vlan 1, видно, что интерфейс отключён, как и IP-протокол, получена информация об MAC-адресе интерфейса, размере MTU, пропускной способности сети (BW), статистике полученных и отправленных пакетов (по нулям, т.к. интерфейс выключен).

<a href="https://ibb.co/9VzyXXN"><img src="https://i.ibb.co/ZYtcssV/Lab1-11.jpg" alt="Lab1-11" border="0"></a>

После того как были соединены кабелем Ehernet компьютер и свитч, сразу же появилось сообщение о поднятом интерфейсе VLAN1, также после просмотра информации об VLAN1 было видно как поменялся MAC.

<a href="https://ibb.co/M2tgmSB"><img src="https://i.ibb.co/5MS1P4K/Lab1-13.jpg" alt="Lab1-13" border="0"></a>

После выполнения команды Show Version выяснено что свитч работает под управлением Cisco Ios 12.2, файл образа системы носит название: C2960-LANBASE-M, а базовый MAC-адрес имеет следующий вид: 0001.4203.0D12.

<a href="https://ibb.co/nBYDJ99"><img src="https://i.ibb.co/hc4Kzbb/Lab1-14.jpg" alt="Lab1-14" border="0"></a>

Далее, при исследовании свойств интерфейса Fastehernet0/6 было выяснено, что данный интерфейс включён, протокол работает. Режим дуплекса установлен в Full-duplex, скорость: 100МБит/с, MAC - 000b.beed.7506. Для включения интерфейса на свитче используется команда "no shutdown".

<a href="https://ibb.co/DrFycRP"><img src="https://i.ibb.co/3Rbq6C5/Lab1-15.jpg" alt="Lab1-15" border="0"></a>

Для анализа сетей VLAN на свитче была выполнена команда "Show VLAN", по умолчанию имя сети VLAN - VLAN 1, в него входят все интерфейсы устройства, как FastEthernet так и GigabitEthernet. Сеть VLAN 1 принадлежит к сети  типа "ethernet".

<a href="https://ibb.co/YZ1t8dR"><img src="https://i.ibb.co/JQGz2pB/Lab1-16.jpg" alt="Lab1-16" border="0"></a>

В соответствии со следующим заданием была изучена флэш - память. После выполнения команды "Show flash" был получен следующий результат: 

<a href="https://ibb.co/R0KKPCq"><img src="https://i.ibb.co/r6hhMZV/Lab1-17.jpg" alt="Lab1-17" border="0"></a>

Имя образа устройства: c2960-lanbase-mz.122-25.FX.bin.

## Часть 2.

Во второй части приступаю к настройке коммутатора.

В соответствии с текстом лаборатороной работы копирую команды в свитч..

<a href="https://ibb.co/Kzb8JvW"><img src="https://i.ibb.co/R4YJqwc/Lab1-18.jpg" alt="Lab1-18" border="0"></a>

Команда no ip domain-lookup отключает поиск по DNS при ошибочном вводе команды, hostname - изменение имени свитча, service password-encryption - шифрование паролей в текущей конфигурации, enable secret class - включение защиты паролем привилегированного режима, banner motd # - создание баннера, информационного сообщения.

Далее произвожу назначение Ip адреса VLAN1 для удаленного управления коммутатором.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/HGZ1T3B/Lab1-19.jpg" alt="Lab1-19" border="0"></a>

В следующем задании ограничиваю доступ к консоли свитча: 

<a href="https://imgbb.com/"><img src="https://i.ibb.co/44kNQdH/Lab1-20.jpg" alt="Lab1-20" border="0"></a>

Команда Login ипользуется для активации пароля.

И далее ограничение паролем доступа к виртуальным линиям (telnet, shh).

<a href="https://imgbb.com/"><img src="https://i.ibb.co/2vFJdhV/Lab1-22.jpg" alt="Lab1-22" border="0"></a> 

Для удаленного подключения к устройству был назначен IP-адрес на PC.

<a href="https://ibb.co/8gCQGkW"><img src="https://i.ibb.co/zVMtCdy/Lab1-23.jpg" alt="Lab1-23" border="0"></a>

И произведен успешный тест удаленного подключения по телнет: 

<a href="https://ibb.co/xG8XqYy"><img src="https://i.ibb.co/nf86MBT/Lab1-24.jpg" alt="Lab1-24" border="0"></a>

Общая конфигурация свитча после лабораторной работы выглядит так: 

<a href="https://ibb.co/PGp8ZVj"><img src="https://i.ibb.co/232B7ph/Lab1-27-1.jpg" alt="Lab1-27-1" border="0"></a>

<a href="https://ibb.co/vwWnchY"><img src="https://i.ibb.co/h7Nzgcf/Lab1-27-2.jpg" alt="Lab1-27-2" border="0"></a>


Были проверены настройки VLAN1. Полоса пропускания - 10.000 Kbit, интерфейс поднят, протокол работает.

<a href="https://ibb.co/WtKGG7m"><img src="https://i.ibb.co/RyHYYtR/Lab1-25.jpg" alt="Lab1-25" border="0"></a>

В заключение выполняется пинг утройства. Пинг был выполнен как в адрес компьютера, так и в адрес свитча.
