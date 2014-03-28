[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)

[Einstellung](https://github.com/daturainformatik/econOfficeREST-API/tree/master/settings/setting)

# Setting
<table>
<tr><td>URI</td><td>${domain}/rest/settings/${version}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/settings/1?path=application.userprofile.adAddress/td></tr>
</table>

## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

[Alle Einstellung zum Benutzerprofil](http://dws.econoffice.ch/rest/settings/1?path=application.userprofile)

## GET
Parameter: `path` Der Pfad zur Einstellung

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<settings>
    <status>0</status>
    <resource>[resource]</resource>
    <client>client_1</client>
    <username>[user]</username>
    <version>1</version>
    <created>2014-03-28T10:17:54.122+01:00</created>
    <timeInMillis>529</timeInMillis>
    <setting>
        <recordRid>0000000000000006</recordRid>
        <path>application.userprofile</path>
        <translations>
            <term>userprofile</term>
            <de>Registrierung</de>
        </translations>
        <values/>
    </setting>
    <childs>
        <child>
            <setting>
                <recordRid>0000000000000008</recordRid>
                <path>application.userprofile.adName</path>
                <translations>
                    <term>adName</term>
                    <de>Namensfelder</de>
                </translations>
                <values/>
            </setting>
            <childs>
                <child>
                    <setting>
                        <recordRid>0000000000000009</recordRid>
                        <path>application.userprofile.adName.lastname</path>
                        <translations>
                            <term>lastname</term>
                            <de>Nachname</de>
                        </translations>
                        <values>
                            <priority>mandatory</priority>
                            <validator>String[3,32]</validator>
                            <type>String</type>
                        </values>
                    </setting>
                    <childs/>
                </child>
                <child>
                    <setting>
                        <recordRid>0000000000000010</recordRid>
                        <path>application.userprofile.adName.firstname</path>
                        <translations>
                            <term>firstname</term>
                            <de>Vorname</de>
                        </translations>
                        <values>
                            <priority>optional</priority>
                            <validator>String[2,32]</validator>
                            <type>String</type>
                        </values>
                    </setting>
                    <childs/>
                </child>
            </childs>
        </child>
        <child>
            <setting>
                <recordRid>0000000000000011</recordRid>
                <path>application.userprofile.adAddress</path>
                <translations>
                    <term>adAddress</term>
                    <de>Adressfelder</de>
                </translations>
                <values/>
            </setting>
            <childs>
                <child>
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
                    <childs/>
                </child>
            </childs>
        </child>
        <child>
            <setting>
                <recordRid>3715F32933290009</recordRid>
                <path>application.userprofile.docFile</path>
                <translations>
                    <term>docFile</term>
                    <de>Dokumente</de>
                    <en>Documents</en>
                </translations>
                <values/>
            </setting>
            <childs>
                <child>
                    <setting>
                        <recordRid>3715F3293329000A</recordRid>
                        <path>application.userprofile.docFile.user-image</path>
                        <translations>
                            <term>user-image</term>
                            <de>Bildchen</de>
                            <en>User image</en>
                        </translations>
                        <values>
                            <priority>optional</priority>
                            <validator>None</validator>
                            <type>STRING</type>
                        </values>
                    </setting>
                    <childs/>
                </child>
            </childs>
        </child>
    </childs>
</settings>
```
