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

### При запуске ping до loopback 1 R2 из R1.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/qBQ4P97/5.jpg" alt="5" border="0"></a>

### Далее были осуществлены настройки Hello-интервалов, на R1 был выставлен приоритет.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/1dmR81V/15.jpg" alt="15" border="0"></a>

### Далее на R1 был настроен маршрут по умолчанию на Loopback 1 и выполнено перенаправление маршрута по умолчанию с помощью команды: default-information originate.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/QmkRTdW/10.jpg" alt="10" border="0"></a>

### Следующей настройкой было назначение на R2 интерфейса Loopback 1 в passive interface, для запрета отправки объявлений а также назначение режима point-to-point.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/0nK2YBr/21.jpg" alt="21" border="0"></a>

### Также была изменена базовая пропускная спосбоность.
### На роутере R2 среди маршрутов OSPF на момент завершения работы из маршрутов OSPF отображается только маршрут по умаолчанию с R1

<a href="https://imgbb.com/"><img src="https://i.ibb.co/K7vp78q/22.jpg" alt="22" border="0"></a>

### При запуске пинга с R2 на Loopback 1 R1, пинг прошёл успешно.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/C1HTc5y/25.jpg" alt="25" border="0"></a>










