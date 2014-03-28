[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)

[Einstellungen](https://github.com/daturainformatik/econOfficeREST-API/tree/master/settings/settingList)

# Setting
<table>
<tr><td>URI</td><td>${domain}/rest/setting/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/setting/1?path=application.userprofile.adAddress/td></tr>
</table>

## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

[Einstellung zum Benutzerprofil Feld 'Strasse'](http://dws.econoffice.ch/rest/setting/1?path=application.userprofile.adAddress.street)

## GET
Parameter: `path` Der Pfad zur Einstellung

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<response>
	<status>0</status>
	<timeInMillis>232</timeInMillis>
	<client>client_1</client>
	<version>1</version>
	<created>Wed Nov 27 14:03:48 CET 2013</created>
	<setting>
		<recordRid>0000000000000012</recordRid>
		<path>application.userprofile.adAddress.street</path>
		<translations>
			<term>street</term>
			<de>Strasse und Hausnummer</de>
		</translations>
		<values>
			<priority>mandatory</priority>
			<validator>String[3,32]</validator>
			<type>String</type>
		</values>
	</setting>
</response>
```