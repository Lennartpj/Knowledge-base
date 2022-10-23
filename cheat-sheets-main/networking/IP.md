Die wichtigste Aufgabe von IP (Internet Protocol) ist, dass jeder Host in einem dezentralen TCP/IP-Netzwerk gefunden werden kann. Dazu wird jedem Hardware-Interface (Netzwerkkarte oder -adapter) eine logische IPv4-Adresse zugeteilt.  
Die IPv4-Adresse ist mit den Angaben zu Straße, Hausnummer und Ort einer Anschrift vergleichbar.

-   [Meine öffentliche IP-Adresse?](https://www.elektronik-kompendium.de/sites/net/1306291.htm)

### NEU 5. Auflage der Netzwerktechnik-Fibel

Die 5. Auflage der Netzwerktechnik-Fibel ist vollständig überarbeitet und als gedrucktes Buch, als eBook im PDF-Format und als Bundle erhältlich.

Die Netzwerktechnik-Fibel ist ein Buch über die Grundlagen der Netzwerktechnik, Übertragungstechnik, [TCP/IP](tcp_ip), Dienste, Anwendungen und Netzwerk-Sicherheit.

### Aufbau einer IPv4-Adresse

Damit die IPv4-Adresse von Hardware und Software einfach verarbeitet werden kann, liegt sie in einem Bitcode bzw. einer Bitfolge aus Einsen (1) und Nullen (0) vor. Sie ist somit maschinenlesbar. Die Bitfolge hat 32 Stellen bzw. ist 4 Byte (32 Bit) groß.

|Schreibweise|Beispiel-Adresse|
|---|---|---|---|---|
|Binär/Dual|0111 1111|0000 0000|0000 0000|0000 0001
|Hexadezimal|7F|00|00|01
|Dezimal|127|0|0|1

Zur einfacheren Lesbarkeit und auch zur Segmentierung werden die 32 Bit einer IPv4-Adresse in jeweils 8 Bit (1 Byte) aufgeteilt und durch einen Punkt voneinander getrennt. Dabei kann jedes Byte durch die achtstellige 1er- und 0er-Folge einen dezimalen Wert von 0 bis 255 annehmen. Das sind 256 Werte pro Stelle. Die binäre IPv4-Adresse 01111111.00000000.00000000.00000001 ergibt die IPv4-Adresse 127.0.0.1.

Obwohl die dezimale Schreibweise üblich ist, können IPv4-Adressen auch als hexadezimale Zahl oder Oktalzahl angegeben werden. Beides ist in der Praxis unüblich und deshalb wenig sinnvoll. Die Besonderheit bei IPv4-Adressen in oktaler Schreibweise ist die Kennzeichnung mit einer führenden Null. Betriebssysteme wie zum Beispiel ab Windows 8.1, Ubuntu 13.10 und Mac OS X 10.9 halten sich an diese Regel. Das bedeutet, gibt man in die Browser-Adresszeile eine IPv4-Adresse mit führender Null ein, dann wird eine oktale Zahl angenommen und in die dezimale Darstellung umgerechnet. Anschließend wird eine Verbindung zu dieser Adresse aufgebaut. Aus diesem Grund sollte man führende Nullen bei der dezimalen Schreibweise von IPv4-Adressen generell weglassen.

-   Falsche Schreibweise: 127.000.000.001
-   Richtige Schreibweise: 127.0.0.1

### Struktur im IPv4-Adressraum

Der IPv4-Adressraum umfasst 32 Bit und reicht von 0.0.0.0 bis 255.255.255.255. Rein rechnerisch ergibt sich aus einer 32-Bit-Adresse eine Anzahl von 2 hoch 32 Adressen. Das entspricht über 4 Milliarden Adressen. Als man den Adressraum definierte, entsprach das damals ungefähr der Weltbevölkerung. Damals war es undenkbar, dass jeder Mensch irgendwann mal eine IPv4-Adresse brauchen, geschweige denn, dass jemand ein persönliches Endgerät (Smartphone) mit einer IPv4-Adresse mit sich herumtrage würde.

Für jede IP-Adresse müsste ein IP-Router wissen, wo sich der entsprechende Host befindet. Das wäre bei 4 Milliarden IPv4-Adressen ein sehr großer Datenbestand, der bei jedem Datenpaket erneut durchlaufen werden müsste, um den Host zu finden. Außerdem müsste jeder Router auf dem Weg zum Host den Vorgang wiederholen. Das würde viel Rechenleistung und Speicherkapazität voraussetzen, die in der Anfangszeit von TCP/IP undenkbar war. Aus diesem Grund hat man dem IPv4-Adressraum eine gewisse Struktur gegeben, um die Routing-Entscheidungen in den Routern einfacher zu machen. Insbesondere vor dem Hintergrund, dass damals die Verfügbarkeit von Rechenleistung und Speicher geringer war.

Im Prinzip hat man sich eine Art Verzeichnis überlegt, wo drin steht, wo sich eine IPv4-Adresse im Netzwerk befindet. Bei Telefonnummern kennen wir die Aufteilung in Ländervorwahl, Ortsvorwahl und Teilnehmerrufnummer. So eine Struktur hatte man sich auch bei IPv4-Adressen vorgestellt. Damit IP-Router möglichst effizient arbeiten können, wurden IPv4-Adressen anfangs hierarchisch zugeteilt. Das hat aber nicht sehr lange funktioniert. Wegen einem zu geringen Adressraum gilt die regionale Zuteilung, wie bei Telefonnummer, nicht mehr.

 

| | Netzadressen | Hostadresse | Netzklasse | Subnetzmaske | CIDR-Suffix |
|---|---|---|:---:|---|---|
| IPv4-Adresse | xxx |.yyy.yyy.yyy | A|255.0.0.0|/8 
|Subnetzmaske|255|.0.0.0| |
|IPv4-Adresse|xxx.xxx|.yyy.yyy|B|255.255.0.0|/16
|Subnetzmaske|255.255.|.0.0
|IPv4-Adresse|xxx.xxx.xxx|.yyy|C|255.255.255.0|/24
|Subnetzmaske|255.255.255|.0

Trotzdem bilden IPv4-Adressen eine Hierarchie ab. Jede IPv4-Adresse besteht im Prinzip aus zwei Teilen. Dem Netz (Subnetz) bzw. der Netzadresse (Netz-ID) und dem Host bzw. der Hostadresse (Host-ID). Beide Teile werden in der IP-Adresse abgebildet.  
Für das IP-Routing ist nur die Netzadresse wichtig. Und die Hostadresse ist nur für den Router wichtig, in dessen Netz sich der Host befindet.   
Bei einer IPv4-Adresse ist der vordere Teil die Netzadresse und der hintere Teil die Hostadresse. Die Teilung findet typischerweise an einem Punkt (".") statt. Aber nicht immer. An welcher Stelle genau die IPv4-Adresse in Netz und Host geteilt wird, dass entscheidet die Netzklasse, die Subnetzmaske oder das CIDR-Suffix.

-   [Netzklasse](https://www.elektronik-kompendium.de/sites/net/2011221.htm)
-   [Subnetzmaske](https://www.elektronik-kompendium.de/sites/net/0907201.htm)
-   [CIDR](https://www.elektronik-kompendium.de/sites/net/2011231.htm)

Durch die Strukturierung entstanden jedoch Lücken im Adressraum, der nicht genutzt wird und der im Prinzip auch nie genutzt werden kann. Das Entstehen von Lücken nennt man Fragmentierung des IPv4-Adressraums. Das hat dazu geführt, dass ein Teil des Adressraums nicht nutzbar ist. Dazu gehört zum Beispiel der Adressbereich von 0.0.0.0 bis 0.255.255.255.  
In den nutzbaren Adressbereichen ist die erste und letzte Adresse eines Subnetzes immer durch das ganze Netz und die Broadcast-Adresse belegt. Welche das genau sind, hängt von der Aufteilung der Subnetze ab. Beispielsweise sind bei einem /28-Netz mit insgesamt 16 IPv4-Adressen (2 hoch 4 gleich 16) deshalb nur 14 IPv4-Adressen nutzbar. Im kleinsten Netz (/30) mit vier IPv4-Adressen sind sogar nur zwei IPv4-Adressen nutzbar. Die anderen zwei sind durch die Strukturierung (Netz- und Broadcast-Adresse) verschwendet.