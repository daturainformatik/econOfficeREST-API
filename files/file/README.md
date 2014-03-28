[Übersicht](https://github.com/daturainformatik/econOfficeREST-API)&nbsp;|&nbsp;[Verzeichnisse](https://github.com/daturainformatik/econOfficeREST-API/tree/master/files/directory)

# Directory
<table>
<tr><td>URI</td><td>${domain}/rest/file/${version}/${pfad}/${dateiname}</td></tr>
<tr><td>Beispiel</td><td>http(s)://beispiel.econoffice.com/rest/file/1/my/path/to/file.ext</td></tr>
</table>

## Online-Beispiele

Für die Authorisierung die Nutzer-Identifikation (Benutzer-ID@Kunden-ID) und Passwort eingegen. Auswahl:

- demo@client_1, secret
- root@client_1, datura

## GET
Gibt eine gespeicherte Datei zurück.

1. Version 1: Zur Anzeige ['welcome_en.txt' am Pfad 'codes.emails'](http://dws.econoffice.ch/rest/file/1/codes/emails/welcome_en.txt)

2. Version 2: Zum Download ['welcome_en.txt' am Pfad 'codes.emails'](http://dws.econoffice.ch/rest/file/2/codes/emails/welcome_en.txt)

Parameter:

* Pfad, durch `/` getrennt, nach der Versionnummer
* Dateiname am Ende; es wird jeweils die neueste Datei dieses Namens zurückgegeben
* Datei-Resource-Id (recordRid) am Ende; es wird genau diese Datei zurückgegben

## PUT
Erlaubt das Hochladen von 1-*n* Dateien in ein Verzeichnis. Es ist möglich mehrere Dateien gleichen Namens in einem Verzeichnis zu haben.
Mittels GET wird dann jeweils die jüngste Datei zurückgegeben, ausser man verwendet statt des Dateinamens die Resource Id der gewünschten Datei


Format: multipart/form-data

Zwingende Parameter:

* `utilizer.table` die Tabelle, zu der diese Datei(en) gehört 
* `utilizer.recordRid` eindeutige Identifikation des dazugehörigen Datensatzes (zu welchem Datensatz aus dieser Tabelle gehört die Datei?)
* `path` der Pfad unter dem die Datei abgelegt werden soll
* `description` ein Text um den Inhalt der Datei zu beschreiben
* `files` Parameter unter dem die Dateien zu finden sind
	
Bei Erfolg werden die Meta-Daten der gespeicherten Dateien zurückgegeben
