Unter Verschlüsselung versteht man Verfahren und Algorithmen, die Daten mittels digitaler bzw. elektronischer Codes oder Schlüssel inhaltlich in eine nicht lesbare Form umwandeln. Diesen Vorgang bezeichnet man als Verschlüsseln. Gleichzeitig wird dafür gesorgt, dass nur mit dem Wissen eines Schlüssels die geheimen Daten wieder entschlüsselt werden können.  
Anstatt von Verschlüsselung spricht man auch von Chiffrierung, was das gleiche meint.

### Verschlüsselungsverfahren

Ein Verschlüsselungsverfahren besteht aus einem Algorithmus zum Verschlüsseln und Entschlüsseln, sowie Verfahren zum Schlüsselaustausch, Prüfung der Authentizität und Integrität.  
Die bekannten Verschlüsselungsverfahren teilen sich in symmetrische, asymmetrische und hybride Verschlüsselungsverfahren auf. Bei den hybriden Verschlüsselungsverfahren wird ein symmetrisches und asymmetrisches Verschlüsselungsverfahren miteinander kombiniert.

### Symmetrische Verschlüsselung

![Symmetrische Verschlüsselung](https://www.elektronik-kompendium.de/sites/net/bilder/19070411.png)  

Die symmetrische Verschlüsselung wird auch als Secret-Key-Verfahren bezeichnet. Es basiert auf einer mathematischen Funktion, die einen Klartext in Abhängigkeit eines Schlüssels (digitaler Code) in einen Geheimtext umwandelt. Beim Entschlüsseln wird der Geheimtext mit dem selben Schlüssel wieder in den Klartext umgewandelt.  
Eine symmetrische Verschlüsselung eignet sich am besten für das Verschlüsseln von Dateien, Verzeichnissen und Laufwerken. Bei der Datenübertragung sind diese Verfahren weniger geeignet, weil man sich um einen sicheren Schlüsselaustausch und deren Verteilung kümmern muss.

### Asymmetrische Verschlüsselung

![Asymmetrische Verschlüsselung](https://www.elektronik-kompendium.de/sites/net/bilder/19070412.png)  

Die asymmetrische Verschlüsselung wird auch als Public-Key-Verfahren bezeichnet. Der wesentliche Unterschied zur symmetrischen Verschlüsselung ist, dass die asymmetrische Verschlüsselung mit zwei Schlüsseln (unterschiedliche digitale Codes) arbeitet. Einen zum Verschlüsseln und den anderen zum Entschlüsseln. Wobei der Schlüssel zum Verschlüsseln öffentlich ist und der Schlüssel zum Entschlüsseln geheim bleiben muss. Man spricht auch vom Public-Key und vom Private-Key.  
Beide Schlüssel sind ein Schlüsselpaar, dass dem Empfänger einer Nachricht gehört.  
Damit ein Sender einem Empfänger eine verschlüsselte Nachricht schicken kann, muss der Empfänger seinen öffentlichen Schlüssel dem Absender bekannt machen.

### Prinzip der hybriden Verschlüsselung

![Hybride Verschlüsselungsverfahren](https://www.elektronik-kompendium.de/sites/net/bilder/09080714.png)

1.  Zuerst wird ein zufälliger Sitzungsschlüssel für die symmetrische Verschlüsselung generiert, mit der die Kommunikation verschlüsselt wird.
2.  Dann verschlüsselt der Sender diesen Sitzungsschlüssel mit dem öffentlichen Schlüssel des Empfängers (asymmetrische Verschlüsselung).
3.  Der Sender schickt dann den asymmetrisch verschlüsselten Sitzungsschlüssel an den Empfänger.
4.  Mit seinem privaten Schlüssel kann der Empfänger den Sitzungsschlüssel entschlüsseln (asymmetrische Verschlüsselung).
5.  Danach werden die Daten mit Hilfe des Sitzungsschlüssels verschlüsselt übertragen (symmetrische Verschlüsselung).

Ein anderes hybrides Verfahren funktioniert so: Man denkt sich einen symmetrischen Sitzungsschlüssel, verschlüsselt die Daten damit und verschlüsselt den symmetrischen Schlüssel mit dem öffentlichen Schlüssel des Empfängers mit einem asymmetrischen Verfahren. Den verschlüsselten Sitzungsschlüssel hängt man für den Empfänger an. Der kann ihn mit seinem privaten Schlüssel entschlüsseln. Anschließend kann er mit dem symmetrischen Sitzungsschlüssel die Daten entschlüsseln.