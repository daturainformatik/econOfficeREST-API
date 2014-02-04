[Übersicht](../..)

[Kontakte](../)

# Kontakt-Adresse
Gibt eine List von Kontakt-Adressen zurück, auf die alle Suchparameter zutreffen.

<table>
<tr><td>URI</td><td>${domain}/rest/contactAddresses/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/contactAddresses/1?stucturedAddress.postalCode=800&structuredName.lastname=Me</td></tr>
</table>

'Datura Web Services' Life-Beispiele:

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:
- demo@client_1, secret
- root@client_1, datura
- 
<table>
<tr><td>Demo-01</td><td>http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=8&structuredName.lastname=Ack</td></tr>
<tr><td></td><td>- Postleitzahl beginnend mit dem Wert '8' und Nachname beginnend mit 'ack'</td></tr>
<tr><td>Demo-02</td><td>http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=88&structuredName.lastname=Web</td></tr>
<tr><td></td><td>- Postleitzahl beginnend mit dem Wert '88' und Nachname beginnend mit 'web'</td></tr>
</table>


# GET
Beschreibung fehlt

# POST/PUT/DELETE
Steht nicht zur Verfügung
