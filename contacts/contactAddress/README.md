[Übersicht](../..)

[Kontakte](../)

# Kontakt-Adresse(n)
Gibt eine Liste von Kontakt-Adressen zurück, auf die alle Suchparameter zutreffen.

<table>
<tr><td>URI</td><td>${domain}/rest/contactAddresses/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/contactAddresses/1?stucturedAddress.postalCode=800&structuredName.lastname=Me</td></tr>
</table>

### Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

1. [Postleitzahl beginnend mit dem Wert '8' und Nachname beginnend mit 'ack'](http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=8&structuredName.lastname=Ack)
2. [Postleitzahl beginnend mit dem Wert '9' und Nachname beginnend mit 'web'](http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=9__4&structuredName.lastname=Web)
3. [Postleitzahl beginnend mit dem Wert '9' und endend mit '4', und Nachname beginnend mit 'web'](http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=9__4&structuredName.lastname=Web)



# GET
Beschreibung fehlt

# POST/PUT/DELETE
Steht nicht zur Verfügung
