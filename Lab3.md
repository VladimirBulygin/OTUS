### Лабораторная работа №3. Рачёт подсетей IPv4.

## Задача №1.

Дано:
IP-адрес узла:	192.168.200.139
Исходная маска подсети:	255.255.255.0
Новая маска подсети:	255.255.255.224

Новая маска 224, в двоичном виде: 11100000, следовательно количество бит подсети - 27
                                                          количество созданных подсетей (2 в степени 27) -134217728.
                                                          количество бит узлов - 5 (32 - 27)
                                                          количество узлов в сети (2 в степени 5 минус 2) - 30
                                                          Адрес сети: 192.168.200.0 (получен путём логической операции "И" между маской и ip адресом узла)
                                                          IPv4-адрес первого узла в этой подсети: 192.168.200.1
                                                          IPv4-адрес последнего узла в этой подсети: 192.168.200.31 (используется 19 маска, т.е. 3 бита от предпоследнего октета
                                                          поэтому складываются оставшиеся числа матрицы 1+2+4+8+16=31)
                                                          Широковещательный IPv4-адрес в этой подсети: 192.168.200.32
                                                         
## Задача №2.

Дано:
IP-адрес узла:	10.101.99.228
Исходная маска подсети:	255.0.0.0
Новая маска подсети:	255.255.128.0

Новая маска 128, в двоичном виде: 10000000, следовательно количество бит подсети - 17
                                                          количество созданных подсетей (2 в степени 17) -131072.
                                                          количество бит узлов - 15 (32 -17)
                                                          количество узлов в сети (2 в степени 15 минус 2) - 32766
                                                          Адрес сети: 10.101.0.0 (получен путём логической операции "И" между маской и ip адресом узла)
                                                          IPv4-адрес первого узла в этой подсети: 10.101.0.1
                                                          IPv4-адрес последнего узла в этой подсети: 10.101.127.254 (используется 17 маска, т.е. 1 бит от                                                                                   предпоследнего октета, поэтому 127 это последнее число перед битом сети 128, а 254 предпоследний бит 4ого октета.
                                                          Поэтому последним адресом будет последнее число 3его октета 127 и 254 (11111110) 
                                                          Широковещательный IPv4-адрес в этой подсети: 192.168.200.32.
                                                          



