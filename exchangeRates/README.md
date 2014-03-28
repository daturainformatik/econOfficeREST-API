[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)

# Wechselkurse (currencyExchangeRates)
Zeigt die Wechselkurse eines Mandanten an

<table>
<tr><td>URI</td><td>${domain}/rest/exchangeRates/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/currencyExchangeRate/1?mandatorId=public_2</td></tr>
</table>


## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

[Wechselkurse von Mandant 'public_2'](http://dws.econoffice.ch/rest/currencyExchangeRate/1?mandatorId=public_2)

## GET
Zeigt die aktuell verwendeten Buchungs- und Bewertungskurse eines Mandanten an.

Parameter:

* `mandatorId` eindeutige Identifikation des Mandanten
* `isoText` eindeutiger ISO-Code der Währung z. B. CHF
* `password` Passwort, falls erforderlich

```xml
<response>
	<status>0</status>
	<resource>[resource]</resource>
	<client>client_1</client>
	<username>[user]</username>
	<version>1</version>
	<created>2014-03-28T09:14:22.972+01:00</created>
	<timeInMillis>106</timeInMillis>
	<mandator>
		<recordRid>0000000000000003</recordRid>
		<mandatorId>public_2</mandatorId>
		<requiresPassword>false</requiresPassword>
		<userInformation>
			<short>Demo-Bereich</short>
			<medium>Mandant: Demo</medium>
			<long>Demo</long>
		</userInformation>
		<balanceDate>
			<month>1</month>
			<day>0</day>
		</balanceDate>
		<currency>
			<isoCode>CHF</isoCode>
		</currency>
	</mandator>
	<data>
		<currencyExchangeRate>
			<booking>
				<date>20140101</date>
				<rate>1.21</rate>
				<source>database</source>
			</booking>
			<currency>
				<isoCode>EUR</isoCode>
			</currency>
			<valuation>
				<date>20130101</date>
				<rate>1.2</rate>
				<source>database</source>
			</valuation>
		</currencyExchangeRate>
	</data>
</response>
```	

## POST
noch nicht spezifiziert; würde eine neuen Wechselkursangabe einfügen

## PUT
noch nicht spezifiziert; würde eine bestehende Wechselkursangabe ändern

## DELETE
nicht erlaubt
