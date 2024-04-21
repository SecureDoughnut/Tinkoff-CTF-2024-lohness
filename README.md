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
underlab:x:2000:2000:,,,:/home/underlab:/bin/bash
tech:x:2200:2200:,,,:/home/tech:/bin/bash
elison:x:2300:2300:,,,:/home/elison:/bin/bash

Путем довольно долгого перебора было найдено:
