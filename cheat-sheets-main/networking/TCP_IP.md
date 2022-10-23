Die Abkürzung TCP/IP steht für die beiden Protokolle Transmission Control Protocol (TCP) und Internet Protocol ([[IP]]). Zusammen mit vielen weiteren Protokollen ist TCP/IP eine Protokoll-Familie für die Vermittlung und den Transport von Datenpaketen in einem dezentral organisierten und globalen Netzwerk. Um hier eine durchgängige Kommunikation von Host zu Host über Netzgrenzen hinweg zu ermöglichen, bedarf es Kommunikationsprotokolle, die im LAN (Local Area Network) und im WAN (Wide Area Network) angewendet werden.  
Der Erfolg des Internets, als ein weltweit verfügbares Kommunikationsnetz, ist zum großen Teil auch die Protokolle rund um TCP/IP zu verdanken.


![Stern-Topologie](https://www.elektronik-kompendium.de/sites/net/bilder/05032714.gif)![](https://www.elektronik-kompendium.de/sites/net/bilder/03092711.gif)![](https://www.elektronik-kompendium.de/sites/net/bilder/05032716.gif)


### Aufgaben und Funktionen von TCP/IP

Die zentrale Aufgabe von TCP/IP ist dafür Sorgen zu tragen, dass Datenpakete innerhalb eines dezentralen Netzwerks beim Empfänger ankommen. Dafür stellt TCP/IP die folgenden zentralen Funktionen bereit.

-   Logische Adressierung / Logical Addressing (IP)
-   Wegfindung / Routing (IP)
-   Fehlerbehandlung und Flussteuerung / Error Control and Flow Control (TCP)
-   Anwendungsunterstützung / Application Support (TCP/UDP)
-   Namensauflösung / Name Resolution (DNS)

Die Besonderheiten und Probleme der paketorientierten Datenübertragung sind sehr vielfältig und erfordern deshalb spezielle Lösungen und Funktionen, die an dieser Stelle nicht alle berücksichtigt werden. Die folgende Darstellung und Beschreibung ist also nur eine Auswahl der wichtigsten Funktionen.

### Vorteile von TCP/IP

TCP/IP hat mehrere entscheidende Vorteile. Jede Anwendung ist mit TCP/IP in der Lage über jedes Netzwerk Daten zu übertragen und auszutauschen. Dabei ist es egal, wo sich die Kommunikationspartner befinden. Das Internet Protocol (IP) sorgt dafür, dass das Datenpaket sein Ziel erreicht und das Transmission Control Protocol (TCP) steuert die Datenübertragung und sorgt für die Zuordnung von Datenstrom und Anwendung.

Für die Anwendungen soll die Art und Weise der physikalischen und logischen Datenübertragung keine Rolle spielen. Der Anwender soll sich auch nicht um Verbindungsaufbau und -abbau kümmern müssen. So lange der Anwender eine korrekte Adresse kennt, wird sich TCP/IP um den Verbindungsaufbau, -abbau und die Übertragung zum Ziel kümmern. Ganz egal welche Anwendung oder welcher Übertragungsweg verwendet wird.

-   TCP/IP ist ein weltweit gültiger Standard und an keinen Hersteller gebunden.
-   TCP/IP kann auf einfachen Computern und auf Supercomputern implementiert werden.
-   TCP/IP ist in LANs und WANs nutzbar.
-   TCP/IP macht die Anwendung vom Übertragungssystem unabhängig.

### Nachteile von TCP/IP

Allerdings ist TCP/IP alles andere als eine effiziente Methode um Daten zu übertragen. Die Daten werden in kleine Datenpakete aufgeteilt. Damit der Empfänger eines Datenpakets weiß, was er damit machen soll, wird dem Datenpaket ein Kopfdatensatz, der als Header bezeichnet wird, vorangestellt. Pro Datenpaket ergibt sich ein Verwaltungsanteil von mindestens 40 Byte pro TCP/IP-Datenpaket. Nur wenn Datenpakete von mehreren kByte gebildet werden, bleibt der Verwaltungsanteil im Vergleich zu den Nutzdaten (Payload) gering.

Wenn die Anwendung bestimmte Anforderungen an das Übertragungssystem stellt, dann lässt sich das nur sehr schwer realisieren. Die systeminterne Kommunikation zwischen Anwendung und Übertragungssystem über TCP/IP hinweg ist nicht vorgesehen.  
Auch lässt sich ein koordinierten Austausch von Verbindungsqualität und -anforderungen zwischen Netzknoten nur sehr schwer netzüberbreifend realisieren. Es gibt zwar Quality of Service (QoS). Doch das ist optional und erfordert die Kontrolle über das Netzwerk, was in einem dezentral organisierten Netzwerk, wie dem Internet, nicht vorgesehen ist.

Man spricht in diesem Zusammenhang auch von Netzneutralität. Die Netzneutralität fordert, dass jedes Paket gleich behandelt wird. Das hat den Nachteil, dass bestimmte Datenpakete nicht priorisiert werden können. Das hat wiederum die Konsequenz, dass bestimmte Anwendungen im Internet mit TCP/IP nicht gut funktionieren.

TCP IP