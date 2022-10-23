 **SMTP** ([Simple Mail Transfer Protocol](https://www.elektronik-kompendium.de/sites/net/0903081.htm)) ist ein Kommunikationsprotokoll für die Übertragung
 von E-Mails. Die Kommunikation erfolgt zwischen einem E-Mail-Client und einem SMTP-Server
 (Postausgangsserver) oder zwischen zwei SMTP-Server.  Für den Austausch der E-Mails sind die Mail Transfer Agents (MTAs) zuständig. Untereinander verständigen sich die MTAs mit dem SMTP-Protokoll. 
 Neben SMTP gibt mit POP und IMAP noch zwei weitere Protokolle für den E-Mail-Austausch. Diese beiden Protokoll dienen jedoch nur dazu, um E-Mail abzuholen oder online zu verwalten. SMTP dagegen ist ein Kommunikationsprotokoll, das E-Mails entgegennehmen und weiterleiten kann

## Troubleshooting

### TLS

1. Prepare encoded strings for your mail username and password

```bash
echo -ne "mail@example.net" | base64
```

2. Connect to mail server

```bash
openssl s_client -starttls smtp -connect smtp.example.com:587
```

3. Send HELO

```smtp
EHLO
```

4. Authenticate

```smtp
AUTH LOGIN
<your-encoded-username>
<your-encoded-password>
```

If that's successful the mail server should return `235 2.7.0 Authentication successful`.
