# Лабораторная работа №5. Основы сетевой безопасности.

# Топология.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/syctJsY/image.jpg" alt="image" border="0"></a>

### Часть 1. Настройка основных параметров.

#### Перед началом работы была выполнена команда на отключение поиска DNS - no ip domain-lookup.
#### В следующих шагах был установлен пароль на привилигерованный режим, консоль и линии vty от 0 до 4 и от 5 до 15. Также была выполнена команда service password-encryption для шифрования открытых паролей в конфигурации.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/WkRKxTM/2.jpg" alt="2" border="0"></a>

### В соответствии с инструкцией, был создан баннер с текстом о запрете несанкционированного доступа.

<a href="https://ibb.co/GFpYd8X"><img src="https://i.ibb.co/N7CDFJX/2.jpg" alt="2" border="0"></a>

### Далее был прописан IP-адрес для интерфейса Gigabitethernet 0/1.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/cxY7Q1M/3.jpg" alt="3" border="0"></a>

### Также был прописан IP-адрес для компьютера и выполнен пинг на шлюз:

<a href="https://ibb.co/4ZL6wFT"><img src="https://i.ibb.co/GvDKfd2/4.jpg" alt="4" border="0"></a>

### Во второй части лабораторной работы было задано имя маршрутизатора, домен для устройства, имя пользователя и пароль для подключения к маршрутизатору через SSH.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/c32p4bm/8.jpg" alt="8" border="0"></a>

### Далее были сгенерированы ключи SSH длиной 512 бит.

<a href="https://ibb.co/gtTD4Zk"><img src="https://i.ibb.co/p4z3hjY/17.png" alt="17" width="1000" border="0"></a>

### В рамках выполнения пунктов 4 и 5, были активированы протоколы SSH и telnet с помощью команды transport input. Способом входа был выбран Local. В заключение произведено сохранение текущей конфигурации.

<a href="https://imgbb.com/"><img src="https://i.ibb.co/721ghHJ/10.jpg" alt="10" border="0"></a>

### Аналогичным с маршрутизатором образом был настроен свитч: 

<a href="https://ibb.co/3M9BWkk"><img src="https://i.ibb.co/jWPgGHH/120.png" alt="120" width="1000" border="0"></a>

### При тестировании подключения к свитчу по SSH, подключение завершилось успешно:

<a href="https://ibb.co/SvgqwbB"><img src="https://i.ibb.co/7yD7tPK/20.png" alt="20" width="1000" border="0"></a>

### Часть 4. Настройка SSH с использованием CLI.

### С помощью CLI коммутатора была использована команда ssh -l admin 192.168.1.1 и выполнено подключение к CLI роутера.

### Далее были выполнены последовательно следующие действия: возвращение в сеанс свитча (Ctr+Shift+6 x), возвращение на R1, завершение сеанса с маршрутизатором по SSH.

<a href="https://ibb.co/0JF8d1Z"><img src="https://i.ibb.co/pXRG9NZ/22.png" alt="22" border="0"></a>

### Ответы на контрольные вопросы: 1) В устройствах Cisco (в эмуляторе Packet Tracer) доступны верии 1 и 2. 
###                                2) Необходимо создать пользователя командой username c использованием контекста privilege, выбрать уровень привилегий для нового пользователя.



