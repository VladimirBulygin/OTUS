### Лабораторная работа №10. Настройка протокола динамической маршрутизации OSPF.

### Для выполнения лабораторной работы была создана следующая топология.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/VLc2DRT/13.jpg" alt="13" border="0"></a>

### В начале работы были выполнены стандартные настройки маршрутизаторов и свитчей (линии vty, пароли на привилегированный режим, отключен поиск DNS). Тажке были настроены IP в соответствии с интрукцией.

<a href="https://ibb.co/BfkbXXS"><img src="https://i.ibb.co/qD6KttP/14.jpg" alt="14" border="0"></a>

### Далее в режиме конфигурации роутера OSPF были настроены ID роутеров, добавлена сеть между интерфейсами G0/1. 

<a href="https://ibb.co/T089QQR"><img src="https://i.ibb.co/FYwRQQJ/1.jpg" alt="1" border="0"></a>

### В результате R1 и R2 установили отношения смежности.

<a href="https://ibb.co/YLJfkXC"><img src="https://i.ibb.co/1mBRqMg/2.jpg" alt="2" border="0"></a>

### На роутере R2 в area 0 была добавлена сеть Loopback 1 192.168.0.0 255.255.255.0. После чего на R1 поступил маршрут до сети 192.168.0.0 255.255.255.0

<a href="https://imgbb.com/"><img src="https://i.ibb.co/QmkRTdW/10.jpg" alt="10" border="0"></a>

### В результате установления отношений смежности R1 был выбран роутером DR (как имеющий более высокий ID), а R2 был выбран BDR.

<a href="https://ibb.co/xhHXmXy"><img src="https://i.ibb.co/zsJQ8Q1/3.jpg" alt="3" border="0"></a>





