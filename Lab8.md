## Лабораторная работа №8. DHCP, SLAAC.

### Для выполнения данной лабораторной работы была использована топология, в соотвествии с инструкцией:

<a href="https://ibb.co/HrsLz6P"><img src="https://i.ibb.co/WcwNyZz/1.jpg" alt="1" border="0"></a>

### Были выполнены стандартные настройки безопасности для марушрутизаторов и свитчей, произведены настройки IPV6 адресов и линк-локал адресов, в соотвествии 
### c инструкцией к лабораторной работе.

<a href="https://ibb.co/N15PS7W"><img src="https://i.ibb.co/gvNpV6t/2.jpg" alt="2" width="1000" border="0"></a>

### Далее были настроены маршруты по умолчанию между ipv6 адресами интерфейсов g0/0 маршрутизаторов:
<a href="https://ibb.co/SQpt4Lq"><img src="https://i.ibb.co/DGn9Hq3/3.jpg" alt="3" width="1000" border="0"></a>

<a href="https://ibb.co/ckyHdRW"><img src="https://i.ibb.co/VJLZ8bF/4.jpg" alt="4" width="1000" border="0"></a>
### При выполнении icmp запроса на порты g0/1 соседнего маршрутизатора, пинг был выполнен успешно:
<a href="https://ibb.co/1LBsz0V"><img src="https://i.ibb.co/9NBwZpX/5.jpg" alt="5" width="1000" border="0"></a>
### При проверке назначения IPV6 адресов на компьютерах PCa и PCb, каждый из хостов получил IPV6 адрес из соответствующей сети:
<a href="https://ibb.co/WGpXGQ6"><img src="https://i.ibb.co/fqGWqb2/7.jpg" alt="7" width="1000" border="0"></a>
### Следующим шагом была настройка роутера 1 для предоставления DHCPv6 без состояния для PC-A. Также для локальной сети R1 был предоставлен флаг OTHER.
<a href="https://imgbb.com/"><img src="https://i.ibb.co/xX8sbJK/9.jpg" alt="9" border="0"></a>
<a href="https://imgbb.com/"><img src="https://i.ibb.co/RBSr5Hs/10.jpg" alt="10" border="0"></a>
### После выполнения настроек, компьютер PC-A получил от роутера настройку DNS сервера.
<a href="https://ibb.co/9w2QLqD"><img src="https://i.ibb.co/cbt4HNB/8.jpg" alt="8" border="0"></a>
### Далее для роутера R1 была произведена настройка DHCP c сохранением состояния.
<a href="https://imgbb.com/"><img src="https://i.ibb.co/pwfnrpr/13.jpg" alt="13" border="0"></a>
### Проблемой последнего шага лабораторной работы стало отсутствие в Cisco Packet Tracer 8.0 команды ipv6 dhcp relay, в связи с этим выполнение шага было невозможным.
### В случае присутствия данной команды в эмуляторе и успешной настройке ретрансляции компьютер PC-B успешно получил бы настройку DHCP сервера.


