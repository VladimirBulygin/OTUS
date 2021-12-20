## Лабораторная работа №9. Безопасность сети.

### Для выполнения лабораторной работы была создана следующая топология:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/D7VG1Ct/top.jpg" alt="top" border="0"></a>

### На маршрутизатор R1 был загружен конфигурационный скрипт из инструкции, осуществляющий настройку пула DHCP, адресов-исключений, интерфейсов роутера.

<a href="https://ibb.co/CvNPc6n"><img src="https://i.ibb.co/4M91q2j/conf-1.jpg" alt="conf-1" border="0"></a>

<a href="https://imgbb.com/"><img src="https://i.ibb.co/XV1JM15/conf2.jpg" alt="conf2" border="0"></a>

### Также были произведены стандартные настройки для коммутаторов, настроены VLAN: Management, Native, Parcking_Lot, присвоены адреса SVI.

<a href="https://ibb.co/Zzfbb8p"><img src="https://i.ibb.co/PGrVVhv/sw12.jpg" alt="sw12" border="0"></a>

### В качестве Native VLAN был настроен VLAN333.

<a href="https://ibb.co/Lhjvgjz"><img src="https://i.ibb.co/FqZnYZb/1.jpg" alt="1" border="0"></a>

<a href="https://ibb.co/4PfwKFq"><img src="https://i.ibb.co/YpW4PNC/2.jpg" alt="2" border="0"></a>

### Следующей настройкой безопасности было перемещение неиспользуемых портов свитчей в VLAN999 и последующее их отключение.

<a href="https://ibb.co/3T9Hrgb"><img src="https://i.ibb.co/QJ3GbyV/333.jpg" alt="333" border="0"></a>

### Далее была произведена настройка Port-Security для портов S1 f0/6 и S2 f0/18

<a href="https://ibb.co/NxfCJyS"><img src="https://i.ibb.co/XX6LKC8/6.jpg" alt="6" border="0"></a>

<a href="https://ibb.co/0c4BysF"><img src="https://i.ibb.co/47vsR1Y/8.jpg" alt="8" border="0"></a>

<a href="https://ibb.co/8B3NX6M"><img src="https://i.ibb.co/wLHBYMy/7.jpg" alt="7" border="0"></a>

<a href="https://ibb.co/4f36FPq"><img src="https://i.ibb.co/g7h5rz2/9.jpg" alt="9" border="0"></a>






