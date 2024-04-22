Лох-несское чудовище существует! Или нет?
Выяснить это можно только с помощью глубоководного фотоэхолота, а он есть у единственной лаборатории поблизости.
Сайт лаборатории: t-nessy-ksevs93q.spbctf.net

<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p1.png?raw=true" alt="qr"/>
</p>
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p2.png?raw=true" alt="qr"/>
</p>
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p3.png?raw=true" alt="qr"/>
</p>

Далее поищем кве для сервиса и находим это:
https://github.com/jhonnybonny/CVE-2024-23334
Работает в нашем случае
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p4.png?raw=true" alt="qr"/>
</p>

Далее придется покопаться в бурпе
Интересны три пользователя
```
underlab:x:2000:2000:,,,:/home/underlab:/bin/bash
tech:x:2200:2200:,,,:/home/tech:/bin/bash
elison:x:2300:2300:,,,:/home/elison:/bin/bash
```

Путем довольно долгого перебора было найдено:
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p6.png?raw=true" alt="qr"/>
</p
 
Соответственно
Путем довольно долгого перебора было найдено:
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p7.png?raw=true" alt="qr"/>
</p
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p8.png?raw=true" alt="qr"/>
</p

Скачиваем и распаковываем, в папке home\tech\.ssh имеем ключи:
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p9.png?raw=true" alt="qr"/>
</p

Коннектимся с ними
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p10.png?raw=true" alt="qr"/>
</p
 
Посмотрим что делали на машине
Коннектимся с ними
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p11.png?raw=true" alt="qr"/>
</p

Теперь у нас есть доступ на elison
Коннектимся с этими данными к нему
<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p12.png?raw=true" alt="qr"/>
</p
Тут не так богато, зато есть странный known_hosts
Оказалось, он зашифрован и его нужно расшифровать
https://github.com/chris408/known_hosts-hashcat
И того после всех манипуляций получил

```
f4ebb37e08c970f4ba4ae4214ab4ee221c465375:07987c3edb4058ef07080566ba7ba2a71b269f9c:38.54.117.194
```
Коннектимся и получаем флаг, который я не успел сдать)

<p align="center">
 <img src="https://github.com/ggPonchik/Tinkoff-CTF-2024/blob/main/p13.png?raw=true" alt="qr"/>
</p




