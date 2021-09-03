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

