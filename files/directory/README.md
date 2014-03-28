[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)&nbsp;|&nbsp;[Datei](https://github.com/daturainformatik/econOfficeREST-API/tree/master/files/file)

# Directory
<table>
<tr><td>URI</td><td>${domain}/rest/directory/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/directory/1?path=my.path.to.directory</td></tr>
</table>

## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

[Unterverzeichnisse vom Pfad 'ad_address'](http://dws.econoffice.ch/rest/rest/directory/1?path=ad_address)

# GET
Zeigt alle Dateien und Unterordner des Datei-Pfades an.

Parameter:
	* `path` Der benötigte Pfad
	
```xml
<response>
    <status>0</status>
    <resource>[resource]</resource>
    <client>client_1</client>
    <username>[user]</username>
    <version>1</version>
    <created>2014-03-28T09:27:37.921+01:00</created>
    <timeInMillis>552</timeInMillis>
    <directory>
        <folder>
            <recordRid>339A6791DFEA0001</recordRid>
            <path>ad_address</path>
            <folders>
                <folder>
                    <recordRid>33AE246E91B90000</recordRid>
                    <path>ad_address.contracts</path>
                    <folders/>
                    <files/>
                </folder>
                <folder>
                    <recordRid>33AE27CC99070000</recordRid>
                    <path>ad_address.correspondence</path>
                    <folders/>
                    <files/>
                </folder>
                <folder>
                    <recordRid>33AE27CC99070001</recordRid>
                    <path>ad_address.accountingSystem</path>
                    <folders/>
                    <files/>
                </folder>
                <folder>
                    <recordRid>33AE27CC99070002</recordRid>
                    <path>ad_address.importantEmails</path>
                    <folders/>
                    <files/>
                </folder>
                <folder>
                    <recordRid>33B725D2974B0000</recordRid>
                    <path>ad_address.notesMemos</path>
                    <folders/>
                    <files/>
                </folder>
                <folder>
                    <recordRid>33B725D2974B0001</recordRid>
                    <path>ad_address.confirmations</path>
                    <folders/>
                    <files/>
                </folder>
                <folder>
                    <recordRid>33D65A935CC50000</recordRid>
                    <path>ad_address.diverse</path>
                    <folders/>
                    <files/>
                </folder>
            </folders>
            <files/>
        </folder>
    </directory>
</response>
```
