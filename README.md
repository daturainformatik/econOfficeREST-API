# econOffice<sup>&reg;</sup> REST-API

An dieser Stelle finden Sie die Spezifikationen der verfügbaren REST-APIs.

Leider ist im allgmeinen nicht völlig klar definiert, wodurch sich *POST*- und *PUT*-Requests unterscheiden.
In der Regel werden mittels *POST* neue Resourcen erstellt, und mittels *PUT* bestehende Resourcen geändert.
Die econOffice<sup>&reg;</sup> REST-API hält sich an diese Konvention.

* Responses sind grundsätzlich in den Formaten XML und JSON verfügbar.
* Responses können in mehreren Versionen (d.h. Strukturierung/Umfang) vorliegen. Eine Beschreibung der einzelnen Versionen finden Sie bei der Beschreibung des jeweiligen Services.
* Responses werden mittels des Parameters *asFile=true* als Datei-Stream übermittelt. D. h. Die Antwort kann als Datei gespeichert werden.

Vorhandene REST-Services:

|Service|URL|GET|POST|PUT|DELETE|
|---|---|:-:|:-:|:-:|:-:|
|[Authentifizierung](/login)|login|&#10004;|&#10004;|&#10008;|&#10004;|
|[Mandanten](/mandator)|mandator|&#10004;|(&#10004;)|(&#10004;)|(&#10004;)|
|[Wechselkurse](/exchangeRates)|exchangeRates|&#10004;|(&#10004;)|&#10008;|&#10008;|
[Kontakt-Liste](/contacts/contactAddress)|contactAddresses|&#10004;|&#10008;|&#10008;|&#10008;|
[Kontakt](/contacts/contactAddress)|contact|&#10004;|(&#10004;)|(&#10004;)|(&#10004;)|
[Einstellungen](/settings/settingList)|settings|&#10004;|&#10008;|&#10008;|&#10008;|
[Einstellung](/settings/setting)|setting|&#10004;|(&#10004;)|(&#10004;)|(&#10004;)|

Legende

|Symbol|Beschreibung|
|:-:|---|
|&#10004;|Vorhanden|
|(&#10004;)|Entsteht gerade|
|&#10008;|Gibt es nicht|
