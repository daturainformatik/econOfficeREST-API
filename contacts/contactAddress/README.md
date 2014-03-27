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
2. [Postleitzahl beginnend mit dem Wert '9' und Nachname beginnend mit 'web'](http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=9&structuredName.lastname=Web)
3. [Postleitzahl beginnend mit dem Wert '9' und endend mit '4', und Nachname beginnend mit 'web'](http://dws.econoffice.ch/rest/contactAddresses/1?structuredAddress.postalCode=9__4&structuredName.lastname=Web)



# GET
Parameter: die einzelnen Felder der XML-contactAddress-Knoten 

Bei Erfolg: Status 200 OK
```xml
<response>
  <status>0</status>
  <resource>/contactAddresses</resource>
  <client>test_dws</client>
  <username>valid_user@test</username>
  <version>1</version>
  <created>2014-03-27T16:48:12.495+01:00</created>
  <timeInMillis>54</timeInMillis>
  <startRow>0</startRow>
  <endRow>1</endRow>
  <totalRows>1</totalRows>
  <data>
    <contactAddress>
      <recordRid>1000000000000021</recordRid>
      <contactNumber>21</contactNumber>
      <sortName>SortName21</sortName>
      <keyName>KeyName21</keyName>
      <keyLocation>KeyPlace21</keyLocation>
      <status>0</status>
      <nameRid>1000000000000021</nameRid>
      <addressRid>2000000000000021</addressRid>
      <structuredName>
        <title>Titel21</title>
          <lastname>Lastname21</lastname>
          <firstname>Firstname21</firstname>
          <nameAddon>NameAdd21</nameAddon>
        <addressPerson>0</addressPerson>
      </structuredName>
      <structuredAddress>
        <street>Street21</street>
        <postalCode>Zip21</postalCode>
      </structuredAddress>
      <unstructuredName>
        <name4>Name4_21</name4>
      </unstructuredName>
      <unstructuredAddress>
        <address1>Address1_21</address1>
      </unstructuredAddress>
    </contactAddress>
  </data>
</response>
```

# POST/PUT/DELETE
Steht nicht zur Verfügung
