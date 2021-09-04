### Лабораторная работа. Просмотр таблицы MAC-адресов коммутатора.

#### Для выполнения  лабораторной работы была создана топология в соответствии с инструкцией:

! <a href="https://imgbb.com/"><img src="https://i.ibb.co/Hr2mmbV/Lab2-1.jpg" alt="Lab2-1" border="0"></a>

#### Т.к. у вновь созданных свитчей не было изначальной конфигурации, команд на удаление конфига и перезагрузку свитча не выполнялось:

! <a href="https://imgbb.com/"><img src="https://i.ibb.co/FmgPS5G/Lab2-2.jpg" alt="Lab2-2" border="0"></a>

#### С помощью команд ip address в режиме глобальной конфигурации, внутри настройки интерфейса VLAN1, были назначены следующие адреса:
1) Свитчу №1 - 192.168.1.11 255.255.255.0
<a href="https://imgbb.com/"><img src="https://i.ibb.co/XsVZBCX/Lab2-4.jpg" alt="Lab2-4" border="0"></a>
2) Свитчу №2 - 192.168.1.12 255.255.255.0
<a href="https://imgbb.com/"><img src="https://i.ibb.co/2jGzhhB/Lab2-5.jpg" alt="Lab2-5" border="0"></a>

Также PC A и PC B были назначены следующие IP адреса:

<a href="https://ibb.co/pd3sCqS"><img src="https://i.ibb.co/TtHnzys/Lab2-3.jpg" alt="Lab2-3" border="0"></a>

Для удаленного управления свитчами были установелны пароли на консоль, vty и привилигированный режим: 
<a href="https://ibb.co/YfwBg0z"><img src="https://i.ibb.co/0Yvy5sg/Lab2-6.jpg" alt="Lab2-6" border="0"></a>
<a href="https://ibb.co/QbhYcBp"><img src="https://i.ibb.co/yfKgRTd/Lab2-7.jpg" alt="Lab2-7" border="0"></a>

После анализа МАС адресов на компьютерах PC A и PC B было установлено:

1) МАС адресс PC A -0004.9A39.248B
2) МАС адресс PC B - 0004.9A39.248B

<a href="https://ibb.co/6nDgBzc"><img src="https://i.ibb.co/1vR861Y/Lab2-8.jpg" alt="Lab2-8" border="0"></a>

Далее были проанализированы МАС адреса свитчей командой Show interface FastEthernet 0/1 
<a href="https://ibb.co/PhdhJW9"><img src="https://i.ibb.co/hWSWrdZ/Lab2-9.jpg" alt="Lab2-9" border="0"></a>

После выполнения команд show mac-address table, был получен следующий результат:

<a href="https://ibb.co/rpMBhvf"><img src="https://i.ibb.co/B6jhJwK/Lab2-10.jpg" alt="Lab2-10" border="0"></a>

Данные mac-адреса относятся к свитчам, подключенным к друг другу по интерефейсу FastEthernet 0/1. Делаю вывод о том, что свитчи "узнали"
адрес друг друга благодаря протоколу STP, DTP и CDP. Поэтому в таблице MAC-адресов нет ещё mac-адресов компьютеров.

В окне результатов команды можно было бы узнать MAC-адрес компьютера в случае обмена пакетами со свитчом (не ping).

При очистке таблицы Mac-адресов и повторном её отображении вначале mac адреса отсутствуют, через несколько секунд появляется MAC-адрес соседнего коммутатора.

<a href="https://ibb.co/Phk0YNc"><img src="https://i.ibb.co/MVdQhsc/Lab2-11.jpg" alt="Lab2-11" border="0"></a>

На PC А была выполнена команда arp -a, результат - отсутствие каких-либо mac-адресов.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/HHT7Pq5/Lab2-12.jpg" alt="Lab2-12" border="0"></a>

Далее с PC B был выполнен ping на все устройства сети. Во всех случаях он был положительным.

<a href="https://ibb.co/2N65c8s"><img src="https://i.ibb.co/ZmJNcHY/Lab2-14.jpg" alt="Lab2-14" border="0"></a>

Также результатом выполнения пинга было отображение mac-адресов в таблице свитча S2 и на машине PC B.

<a href="https://ibb.co/Bywqv1H"><img src="https://i.ibb.co/v3DZftC/Lab2-16.jpg" alt="Lab2-16" border="0"></a>

