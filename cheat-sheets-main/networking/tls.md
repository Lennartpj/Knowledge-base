TLS ist ein Protokoll, das der Authentifizierung und Verschlüsselung von Internetverbindungen dient. TLS schiebt sich als eigene Schicht zwischen [[TCP]] und den Protokollen der Anwendungs- und Darstellungsschicht. In der Regel geht es darum, die Echtheit des kontaktierten Servers durch ein Zertifikat zu garantieren und die Verbindung zwischen Client und Server zu verschlüsseln.

Obwohl man in der Regel TLS verwendet, ist die Bezeichnung [[SSL]] immer noch üblich. Häufig werden beide Bezeichnungen synonym verwendet.

TLS (Version 1.0) hat seinen Ursprung in SSL, das von Netscape in den 1990er Jahren für den Browser "Netscape Navigator" entwickelt wurde. Die Weiterentwicklung von SSL wurde mit der Version 3 beendet. Danach übernahm die [IETF][https://www.ietf.org/about/] (Internet Engineering Task Force) die Weiterentwicklung und Normierung. Daraus entstand 1999 der Standard TLS (Transport Layer Security).  
TLS ist bis auf ein paar Details mit SSL identisch. Die Unterschiede zwischen TLS Version 1 und SSL Version 3 reichen jedoch aus, dass beide zueinander inkompatibel sind. TLS verwendet zur Authentifizierung der Daten HMAC und erzeugt die Schlüssel mit der Funktion PRF.

Als Mindeststandard schreibt das BSI, als für die Sicherheit der bundesbehördlichen IT-Systeme zuständige Behörde, TLS 1.3 oder TLS 1.2 mit Diffie-Hellman-Schlüsselaustausch vor.



## TLS im OSI-Schichtenmodell

Im [[OSI-Schichtenmodell]] ist TLS auf Schicht 5, der Sitzungsschicht angeordnet. Im DoD-Schichtenmodell, das für TCP/IP verwendet wird, ist TLS auf der Transportschicht als Transportverschlüsselung über TCP und unterhalb der Anwendungsprotokolle zugeordnet. Dabei arbeitet TLS völlig transparent. So können theoretisch alle denkbaren Anwendungsprotokolle TLS zum Verschlüsseln benutzen. Dabei muss aber jedes Anwendungsprotokoll TLS explizit beherrschen.   
So wird beispielsweise aus dem unverschlüsselten HTTP (Hypertext Transfer Protocol) das verschlüsselte HTTPS (Hypertext Transfer Protocol Secure). Ebenso ist es möglich E-Mails über TLS beim POP-Server verschlüsselt abzurufen oder an den SMTP-Server verschlüsselt zu übermitteln. Auch hier bekommen die Protokolle einen "Secure"-Zusatz (SMTPS, POPS, IMAPS).  
TLS ist inzwischen nicht nur auf HTTPS oder andere Kommunikationsprotokolle beschränkt. Verfahren wie EAP-TLS, EAP-TTL, PEAP und auch das LDAP-Protokoll verwenden TLS.