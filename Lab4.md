## Лабораторная работа №4. Настройка IPV6.

### Топология.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/55L8Tst/image.jpg" alt="image" border="0"></a>

### Для выполнения лабораторной работы использовалось оборудование: 1) Коммутатор Cisco 2960-24TT 2) Маршрутизатор Cisco 2911 3) Два ПК.

### Перед началом работы с оборудованием была произведена настройка линий, паролей на привилегированный режим, линии и консоль. Выполнялась проверка первоначальной конфигурации с помощью команды Show Startup config - изначальных конфигураций на утройствах не было.

### Далее для включения IPV6 на коммутаторе была выполнена команда: sdm prefer dual-ipv4-and-ipv6 default, после чего было получено сообщение о необходимости перезагрузки. Следующим действием была выполнена перезагрузка командой Reload.
<a href="https://ibb.co/zWgtsGR"><img src="https://i.ibb.co/1YN4Z8q/1.jpg" alt="1" border="0"></a>

### В соответствии с частью второй лабораторной работы, были назначены IPV6 адреса на интерфейсах роутера.
<a href="https://ibb.co/HGtKJPT"><img src="https://i.ibb.co/RQ3g56T/2.jpg" alt="2" border="0"></a>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/r4VdDzF/3.jpg" alt="3" border="0"></a>
### Далее была выполнена настройка одного и того же локального адреса для обоих интерфейсов роутера:
<a href="https://imgbb.com/"><img src="https://i.ibb.co/6mnvMyJ/4.jpg" alt="4" border="0"></a>
### Были просмотрены группы многоадресной рассылки для интерфейса роутера gigabitethernet 0/0 с помощью команды R1#show ipv6 interface gigabitEthernet 0/0:
<a href="https://ibb.co/9WFbbVr"><img src="https://i.ibb.co/BBXyyrC/5.jpg" alt="5" border="0"></a>
### При просмотре сетевых настроек PCB адрес ipv6 отсутствовал, кроме Link local:
<a href="https://ibb.co/VC0sLgB"><img src="https://i.ibb.co/fNVsXk0/6.jpg" alt="6" border="0"></a>
### Следующей операцией было выполнение на роутере команды для включения IPV6 адресации IPv6 unicast-routing. Результатом её выполнения был полученный компьютером в автоматическом режиме IPV6 адрес. 
<a href="https://ibb.co/KsjCSqf"><img src="https://i.ibb.co/s1vLzwN/7.jpg" alt="7" border="0"></a>
### Был также настроен IPV6 адрес для интерфейса свитча VLAN1. 

<a href="https://ibb.co/Qm9B8q4"><img src="https://i.ibb.co/vz15srS/8.jpg" alt="8" border="0"></a>

### Завершающим этапом лабораторной работы было назначение компьютерам статических адресов IPV6 и проверка подключения через пинг и tracert.
<a href="https://ibb.co/4J826m0"><img src="https://i.ibb.co/x31YpCr/9.jpg" alt="9" border="0"></a>

### Ответы на контрольные вопросы:
1) В разных канальных средах неважно какой будет локальный адрес, т.к. канальные среды не пересекаются.
2) Идентификатор сети для IP 2001:db8:acad::aaaa:1234/64- 2001:db8:acad.




