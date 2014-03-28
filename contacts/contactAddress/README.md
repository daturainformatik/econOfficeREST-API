[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)

[Kontakte](https://github.com/daturainformatik/econOfficeREST-API/tree/master/contacts)
[Kontakt-Adressen](https://github.com/daturainformatik/econOfficeREST-API/tree/master/contacts/contactAddresses)
[Kontakt](https://github.com/daturainformatik/econOfficeREST-API/tree/master/contacts/contact)

# Kontakt-Adresse
Ermöglicht das Bearbeiten einer einzelnen Kontakte Adresse

<table>
<tr><td>URI</td><td>${domain}/rest/contactAddress/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/contactAddress/1?contactNumber=42</td></tr>
</table>

## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

1. [Kontakt Adresse Nr. 16382](http://dws.econoffice.ch/rest/contactAddress/1?contactNumber=16382)
2. [Kontakt Adresse mit der ID=340AE820CD890000](http://dws.econoffice.ch/rest/contactAddress/1?recordRid=340AE820CD890000)

# GET
Zeigt eine einzelne Kontaktadresse an

Parameter:

	* `contactNumber` ganze Zahl, welche die Kontakt-Adresse eindeutig identifiziert
	* `recordRid` interne, eindeutig Resource Id
	
**Erfolg** *Die passende Kontaktadresse(Status 200 OK)*

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
</response>
```

# POST
Überschreibt eine einzelne Kontaktadresse mit den als Payload (json/xml) übergeben Werten und gibt die neu gespeicherte Kontaktadresse zurück

# PUT
Erstellt aus dem übergebenen Payload (json/xml) eine neue Kontakt Adresse und gibt diese zurück

# DELETE
Ändert den Status einer Kontakt Adresse auf gelöscht. 