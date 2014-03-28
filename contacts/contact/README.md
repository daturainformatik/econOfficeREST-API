[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)|
[Kontakte](https://github.com/daturainformatik/econOfficeREST-API/tree/master/contacts)|
[Kontakt-Adressen](https://github.com/daturainformatik/econOfficeREST-API/tree/master/contacts/contactAddresses)|
[Kontakt-Adresse](https://github.com/daturainformatik/econOfficeREST-API/tree/master/contacts/contactAddress)|

# Kontakt
<table>
<tr><td>URI</td><td>${domain}/rest/contact/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/contact/1?contactNumber=42</td></tr>
</table>

## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

1. [Daten des Adress-Dossiers mit der Nummer 20812, von Ziswyler Laura](http://dws.econoffice.ch/rest/contact/1?contactNumber=20812)
2. [Daten des Adress-Dossiers mit der Nummer 16119 (zum Ausprobieren einfach die Adress-Nummer ändern)](http://dws.econoffice.ch/rest/contact/1?contactNumber=16119)

## GET

```xml
<response>
	<status>0</status>
	<resource>[resource]</resource>
	<client>client_1</client>
	<username>[user]</username>
	<version>1</version>
	<created>2014-03-28T08:38:18.362+01:00</created>
	<timeInMillis>97</timeInMillis>
	<contact>
		<recordRid>340A648BCD890000</recordRid>
		<contactNumber>16119</contactNumber>
		<salutation>Herr</salutation>
		<letterOpening>Sehr geehrter Herr Weber</letterOpening>
		<sortName>Weber Stefan</sortName>
		<sortPlace>Waldstatt</sortPlace>
		<sortMail>9104</sortMail>
		<keyName>Weber Stefan</keyName>
		<keyLocation>Waldstatt</keyLocation>
		<status>1</status>
		<nameRid>340A648BCD890000</nameRid>
		<addressRid>340A648BCD890001</addressRid>
		<structuredName>
			<lastname>Weber</lastname>
			<firstname>Stefan</firstname>
		</structuredName>
		<structuredAddress>
			<street>Dorf 166</street>
			<postalCode>9104</postalCode>
			<city>Waldstatt</city>
		</structuredAddress>
		<unstructuredName>
			<name3>Herr</name3>
			<name4>Stefan Weber</name4>
		</unstructuredName>
		<unstructuredAddress>
			<address1>Dorf 166</address1>
			<address2>9104 Waldstatt</address2>
		</unstructuredAddress>
		<phonenumbers/>
		<emailAddresses/>
		<websites/>
		<otherMedia/>
		<customFields/>
	</contact>
</response>
```

## POST/PUT/DELETE
Erfolgt nicht direkt am Address Dossier, sondern über die dazugehörige Kontaktadresse oder die untegeordneten Knoten (`phonenumbers`, `emailAddresses`, `websites` usw.)
