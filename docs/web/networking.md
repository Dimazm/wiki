# Networking
На сегодняшний день использование клиентов служб мгновенного обмена сообщениями (instant messanger) стало незаменимым средством для всех пользователей Интернета. Существует множество клиентов (Skype, WhatsApp, Viber, ICQ и т. д.), о которых каждый слышал и которые мы ежедневно используем. Все они работают по определенным правилам, т.е. реализуют определенные *протоколы взаимодействия*.

**Protocol** — это по сути правила обмена информацией, которые описывают каким образом обмениваются информацией взаимодействующие стороны. Например: существует *дипломатический протокол*, где дипломаты в определенных случаях должны говорить фразы из определенного набора слов, фраз и другая сторона делает то же самое.

В *сетевом взаимодействии* - вы посылаете определенные байты и ждете в ответ определенные байты. Этот обмен и есть *протокол*. Если он соблюдается обеими сторонами, то они смогут о чем-нибудь договориться.


## Сетевые модели
Существуют 2 сетевые модели:
- `OSI` - теоритическая (существует только в теории) 
- `TCP/IP` - практическая (используется на практике)

![Network's models](/img/web/logical-mapping-between-OSI-and-TCP-IP.png)

Если рассматривать полную сетевую модель **OSI** (**Open System Interconnection** — взаимодействие открытых систем), то прикладного программиста для Web затрагивают в основном протоколы *Прикладного уровня* — `HTTP`, `FTP`, `SMTP`, `SNMP` и протоколы *Транспортного уровня* — `TCP` и `UDP`.

Согласно протоколу **IP** (**Internet Packet**), каждый узел (компьютер, switch и т.п.) в сети имеет свой IP-адрес. На данный момент интернет работает по протоколу **IPv4**, где IP адрес записывается 4 числами от `0` до `255` - например, `127.0.0.1`. Существует и другой способ идентификации компьютеров в сети через доменное имя, которое более удобное и нагляднее идентифицирует компьютер, чем простой набор чисел (например, `github.com`). В Интернете существуют специальные сервера **DNS** (**Domain Name System**), которые осуществляют преобразование доменного имени в IP-адрес и наоборот.

**TCP** протокол базируется на IP для доставки пакетов, но добавляет два важных свойства :
- установление соединения между приложениями
- использование портов (не просто узлов)

Таким образом, для идентификации компьютера (**host**) в сети используется IP-адрес; для идентификации приложения TCP добавляет понятие порта. **Порт** - это целое число от `1` до `65535` указывающее, какому приложению предназначается пакет.

Java имеет достаточно простой в использовании встроенный сетевой интерфейс, который упрощает связь через сокеты *TCP/IP* или *UDP*. *TCP* обычно используется чаще, чем *UDP*.


### TCP Networking
Обычно клиент открывает *TCP/IP*-соединение с сервером. Затем клиент начинает обмениваться информацией с сервером. Когда клиент завершает работу с сервером, он закрывает соединение.

![TCP Networking](/img/web/tcp-networking.png)

Клиент может отправлять несколько запросов через открытое соединение. Фактически, клиент может отправлять столько данных, сколько сервер готов к приему. Сервер также может закрыть соединение, если он захочет.


### UDP Networking
UDP работает немного иначе, чем *TCP*. Используя *UDP*, соединение между клиентом и сервером отсутствует. Клиент может отправлять данные на сервер, и сервер может (или не может) получать эти данные. Клиент никогда не узнает, были ли данные получены на другом конце. То же самое верно для данных, отправленных другим способом от сервера к клиенту.

Поскольку нет гарантии доставки данных, протокол *UDP* имеет меньшие накладные расходы протокола.