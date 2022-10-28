Das Transmission Control Protocol, kurz TCP, ist Teil der Protokollfamilie [TCP/IP](TCP_IP). TCP ist ein verbindungsorientiertes Protokoll und soll maßgeblich Datenverluste verhindern, Dateien und Datenströme aufteilen und Datenpakete den Anwendungen zuordnen können.

### Aufgaben und Funktionen von TCP

-   Segmentierung (Data Segmenting): Dateien oder Datenstrom in Segmente teilen, Reihenfolge der Segmente wieder herstellen und zu Dateien oder einem Datenstrom zusammensetzen
-   Verbindungsmanagement (Connection Establishment and Termination): Verbindungsaufbau und Verbindungsabbau
-   Fehlerbehandlung (Error Detection): Bestätigung von Datenpaketen und Zeitüberwachung
-   Flusssteuerung (Flow Control): Dynamische Auslastung der Übertragungsstrecke
-   Anwendungsunterstützung (Application Support): Adressierung spezifischer Anwendungen und Verbindungen durch Port-Nummern 
---
## TCP Ports

| Port Number | Usage |
|---|---|
| 20 | File Transfer Protocol ([[FTP]]) Data Transfer|
| 21|File Transfer Protocol ([[FTP]]) Command Control
|22|Secure Shell ([[SSH]])
|23|[[Telnet]] - Remote login service, unencrypted text messages
|25|Simple Mail Transfer Protocol ([[SMTP]]) E-mail Routing
|53|Domain Name System ([[DNS]]) service
|80|Hypertext Transfer Protocol ([[HTTP]]) used in World Wide Web
|110|Post Office Protocol ([[POP3]]) used by e-mail clients to retrieve e-mail from a server
|119|Network News Transfer Protocol ([[NNTP]])
|123|Network Time Protocol ([[NTP]])
|143|Internet Message Access Protocol ([[IMAP]]) Management of Digital Mail
|161|Simple Network Management Protocol ([[SNMP]])
|194|Internet Relay Chat ([[IRC]])
|443|HTTP Secure ([[HTTPS]]) HTTP over [[TLS]]/[[SSL]]