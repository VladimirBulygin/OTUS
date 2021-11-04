#### Лабораторная работа №6. VLAN.
## Для выполнения лабораторной работы была построена топология, состоящая из одного маршрутизатора R1, свитчей S1 и S2 и двух хостов.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/7WGFLDy/image.jpg" alt="image" border="0"></a>

## В начале были выполнены стандартные настройки безопасности для маршрутизатора R1. Отключен поиск по DNS, включена функция шифрования паролей, установлено имя роутера и время.
<a href="https://ibb.co/8j4GhY5"><img src="https://i.ibb.co/THqJCW8/1.jpg" alt="1" border="0"></a>
<a href="https://ibb.co/6JcZt09"><img src="https://i.ibb.co/n8q01Md/2.jpg" alt="2" border="0"></a>

## Следующим шагом была настройка идентичная по командам настройка коммктаторов S1 и S2. После настройки у обоих свитчей конфигурация отличалась только именем устройства.

<a href="https://ibb.co/6JFDYRb"><img src="https://i.ibb.co/k6XqKg0/3.jpg" alt="3" border="0"></a>
<a href="https://ibb.co/dMgqsrj"><img src="https://i.ibb.co/pwy86xb/4.jpg" alt="4" border="0"></a>

## После настройки коммутаторов были назначены ip - адреса хостам.

## В начале второй части лабораторной работы была выполнена настройка VLAN аналогичным образом на обоих коммутаторах.

<a href="https://ibb.co/8s0KRj7"><img src="https://i.ibb.co/JtKBbzs/5.jpg" alt="5" width="1000" heigth="1000" border="0"></a>

## После создания VLAN была выполнена настройка SVI - интерфейса управления аналогично на обоих свитчах.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/bJMLbrt/6.jpg" alt="6" border="0"></a>

## И далее порты коммутатора S1 были включены во VLAN, в соответствии с таблицей внутри лаб. работы.

<a href="https://ibb.co/vk1pgDg"><img src="https://i.ibb.co/4pWz9J9/8-1.jpg" alt="8-1" border="0"></a>

## Подобным образом был натроен свитч S2.

<a href="https://ibb.co/rpY9qWf"><img src="https://i.ibb.co/JpVZ8hF/8-2.jpg" alt="8-2" border="0"></a>

## При настройке Native на другом коммутаторе появилась ошибка:


## В заключение был активирован транк-порт на роутере, настроены саб-интерфейсы (основные шлюзы для VLAN). 

<a href="https://ibb.co/xLPFwtd"><img src="https://i.ibb.co/vqgXf6R/10.jpg" alt="10" border="0"></a>

## При тестировании соединения между ПК, результатом был успешный пинг с ПК PC-A, а также успешно выполненная команда tracert с PC - B, в которой 
## был виден маршрут, проходящий через саб-интерфейс 30.1.

<a href="https://ibb.co/B3F05bk"><img src="https://i.ibb.co/DWT0Hhd/11.jpg" alt="11" border="0"></a>

<a href="https://ibb.co/2vN0dH0"><img src="https://i.ibb.co/6HBcFLc/12.jpg" alt="12" border="0"></a>
