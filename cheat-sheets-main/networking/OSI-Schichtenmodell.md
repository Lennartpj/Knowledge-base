In der Computer- und Netzwerktechnik haben sich Schichtenmodelle etabliert, um komplexe Vorgänge in einzelnen Schritten aufzugliedern. Jeder Schritt oder auch jede Aufgabe wird als Schicht in einem Schichtenmodell übereinander dargestellt.

Das OSI-Schichtenmodell ist ein Referenzmodell für herstellerunabhängige Kommunikationssysteme bzw. eine Design-Grundlage für Kommunikationsprotokolle und Computernetze.

OSI bedeutet Open System Interconnection (Offenes System für Kommunikationsverbindungen) und wurde von der ISO (International Organization for Standardization), das ist die Internationale Organisation für Normung, als Grundlage für die Bildung von offenen Kommunikationsstandards entworfen.

Das OSI-Schichtenmodell besteht aus 7 Schichten und basiert auf dem DoD-Schichtenmodell. Im Vergleich zum DoD-Schichtenmodell ist das OSI-Schichtenmodell feiner und detaillierter gegliedert. Jede Schicht definiert für die Kommunikation zwischen zwei Systemen bestimmte Aufgaben und Funktionen. Für jede Schicht existieren Verfahren und Protokolle, die bestimmte Aufgaben erfüllen, und der übergeordneten Schicht eine bestimmte Dienstleistung zur Verfügung stellen.

Die gestrichelten Linien sollen zeigen, dass eine virtuelle Verbindung auf den Schichten zwischen den Endsystemen besteht.  
Bei der Kommunikation zwischen zwei Systemen durchläuft die Kommunikation oder der Datenfluss alle 7 Schichten des OSI-Schichtenmodells mindestens zwei Mal. Einmal beim Sender und einmal bei Empfänger. Je nachdem, wie viele Zwischenstationen die Kommunikationsstrecke aufweist, durchläuft die Kommunikation auch hier mehrmals das Schichtenmodell in Teilen oder auch ganz.

### Protokolle im OSI-Schichtenmodell

Protokolle sind eine Sammlung von Regeln zur Kommunikation auf einer bestimmten Schicht des OSI-Schichtenmodells. Die Protokolle einer Schicht sind zu den Protokollen der über- und untergeordneten Schichten weitestgehend transparent, so dass die Verhaltensweise eines Protokolls sich wie bei einer direkten Kommunikation mit dem Gegenstück auf der Gegenseite darstellt.  
Die Übergänge zwischen den Schichten sind Schnittstellen, die von den Protokollen verstanden werden müssen. Weil manche Protokolle für ganz bestimmte Anwendungen entwickelt wurden, kommt es auch vor, dass sich Protokolle über mehrere Schichten erstrecken und mehrere Aufgaben abdecken. Dabei kommt es vor, dass in manchen Verbindungen einzelne Aufgaben in mehreren Schichten und somit mehrfach ausgeführt werden.

### Einteilung des OSI-Schichtenmodells

-   Das OSI-Schichtenmodell besteht aus 7 Schichten. 
-   Jeder Schicht ist eine bestimmte Aufgabe zugeordnet.
-   Einzelne Schichten können angepasst, zusammengefasst oder ausgetauscht werden.
-   Die Schichten 1..4 sind transportorientierte Schichten.
-   Die Schichten 5..7 sind anwendungsorientierte Schichten.
-   Das Übertragungsmedium ist nicht festgelegt.

### Schicht 1: Bitübertragungsschicht / Physical Layer

##### Maßnahmen und Verfahren zur Übertragung von Bitfolgen

Die Bitübertragungsschicht definiert die elektrische, mechanische und funktionale Schnittstelle zum Übertragungsmedium. Die Protokolle dieser Schicht unterscheiden sich nur nach dem eingesetzten Übertragungsmedium und -verfahren. Das Übertragungsmedium ist jedoch kein Bestandteil der Schicht 1.

### Schicht 2: Sicherungsschicht / Data Link Layer

Logische Verbindungen mit Datenpaketen und elementare Fehlererkennungsmechanismen

Die Sicherungsschicht sorgt für eine zuverlässige und funktionierende Verbindung zwischen Endgerät und Übertragungsmedium. Zur Vermeidung von Übertragungsfehlern und Datenverlust enthält diese Schicht Funktionen zur Fehlererkennung, Fehlerbehebung und Datenflusskontrolle.  
Auf dieser Schicht findet auch die physikalische Adressierung von Datenpaketen statt.

### Schicht 3: Vermittlungsschicht / Network Layer

##### Routing und Datenflusskontrolle

Die Vermittlungsschicht steuert die zeitliche und logische getrennte Kommunikation zwischen den Endgeräten, unabhängig vom Übertragungsmedium und der Topologie. Auf dieser Schicht erfolgt erstmals die logische Adressierung der Endgeräte. Die Adressierung ist eng mit dem Routing (Wegfindung vom Sender zum Empfänger) verbunden.

### Schicht 4: Transportschicht / Transport Layer

##### Logische Ende-zu-Ende-Verbindungen

Die Transportschicht ist das Bindeglied zwischen den transportorientierten und anwendungsorientierten Schichten. Hier werden die Datenpakete einer Anwendung zugeordnet.

### Schicht 5: Kommunikationsschicht / Session Layer

##### Prozess-zu-Prozess-Verbindungen

Die Kommunikationsschicht organisiert die Verbindungen zwischen den Endsystemen. Dazu sind Steuerungs- und Kontrollmechanismen für die Verbindung und dem Datenaustausch implementiert.

### Schicht 6: Darstellungsschicht / Presentation Layer

##### Ausgabe von Daten in Standardformate

Die Darstellungsschicht wandelt die Daten in verschiedene Codecs und Formate. Hier werden die Daten zu oder von der Anwendungsschicht in ein geeignetes Format umgewandelt.

### Schicht 7: Anwendungsschicht / Application Layer

##### Dienste, Anwendungen und Netzmanagement

Die Anwendungsschicht stellt Funktionen für die Anwendungen zur Verfügung. Diese Schicht stellt die Verbindung zu den unteren Schichten her. Auf dieser Ebene findet auch die Dateneingabe und -ausgabe statt.

### Kurzbeschreibung des OSI-Schichtenmodells

7. Schicht / **Anwendung**: Funktionen für Anwendungen, sowie die Dateneingabe und -ausgabe.  
6. Schicht / **Darstellung**: Umwandlung der systemabhängigen Daten in ein unabhängiges Format.  
5. Schicht / **Kommunikation**: Steuerung der Verbindungen und des Datenaustauschs.  
4. Schicht / **Transport**: Zuordnung der Datenpakete zu einer Anwendung.  
3. Schicht / **Vermittlung**: Routing der Datenpakete zum nächsten Knoten.  
2. Schicht / **Sicherung**: Segmentierung der Pakete in Frames und Hinzufügen von Prüfsummen.  
1. Schicht / **Bitübertragung**: Umwandlung der Bits in ein zum Medium passendes Signal und physikalische Übertragung.

Hinweis: Die Endgeräte der Endsysteme und das Übertragungsmedium sind aus dem OSI-Schichtenmodell ausgeklammert. Trotzdem kann es sein, dass die Endgeräte in der Anwendungsschicht und das Übertragungsmedium in der Bitübertragungsschicht vorgegeben sind.

### Das OSI-Schichtenmodell in der Praxis

Das OSI-Schichtenmodell wird sehr häufig als Referenz herangezogen, wenn es darum geht, Abläufe einer Kommunikation oder Nachrichtenübermittlung darzustellen. Doch eigentlich ist das DoD-Schichtenmodell ([TCP/IP](tcp_ip)) viel näher an der Realität.  
Das Problem des OSI-Schichtenmodells ist die Standardisierungsorganisation ISO, die einfach zu schwerfällig war, um in kürzester Zeit einen Rahmen für die Aufgaben von Protokollen und Übertragungssystemen in der Netzwerktechnik auf die Beine zu stellen. TCP/IP dagegen war frei verfügbar, funktionierte und verbreitete sich mit weiteren Protokollen rasend schnell. Der ISO blieb nichts anderes übrig, als TCP/IP im OSI-Schichtenmodell zu berücksichtigen.  
Neben TCP/IP haben sich noch weitere Netzwerkprotokolle entwickelt. Die wurden jedoch irgendwann von TCP/IP abgelöst. Fast alle Netzwerke arbeiten heute auf der Basis von TCP/IP.

In der folgenden Tabelle werden die verschiedensten Protokolle, Übertragungs- und Vermittlungstechniken den Schichten des OSI-Modells zugeordnet.  
Viele Protokolle und Übertragungsverfahren nutzen mehr als nur eine Schicht. Deshalb kann eine vollständige und korrekte Darstellung der Tabelle nicht gewährleistet werden.

|Schicht|Name|Protokolle|
| --- |:---:|----|
| Schicht 7     | Anwendung|[[Telnet]], [[FTP]], [[HTTP]], [[SMTP]], NNTP |
| Schicht 6     | Darstellung|[[Telnet]], [[FTP]], [[HTTP]], [[SMTP]], NNTP, NetBIOS |
| Schicht 5     | Kommunikation|[[Telnet]], [[FTP]], [[HTTP]], [[SMTP]], NNTP, NetBIOS, TFTP |
| Schicht 4     | Transport|[[TCP]], [[UDP]], SPX, NetBEUI |
| Schicht 3     | Vermittlung|[[IP]], IPX, ICMP, T.70, T.90, X.25, NetBEUI |
| Schicht 2     | Sicherung|LLC/MAC, X.75, V.120, ARP, HDLC, PPP |
| Schicht 1     | Übertragung| Ethernet, Token Ring, FDDI, V.110, X.25, Frame Relay, V.90, V.34, V.24 |

Auch wenn nur die Schichten von 1 bis 7 offiziell definiert sind, gelten steht im allgmeinen Sprachgebraucht die Schicht 0 für die Verkabelung und die Hardware. Die Schicht 8 stellt den Anwender mit seinen Anforderungen oder die Politik dar. Die Schicht 9 ist die Religion oder ein Dogma.