# econOffice<sup>&reg;</sup> REST-API

An dieser Stelle finden Sie die Spezifikationen der verfügbaren REST-APIs.

Leider ist im allgmeinen nicht völlig klar definiert, wodurch sich *POST*- und *PUT*-Requests unterscheiden.
Bei uns werden mittels *POST* bestehende Resourcen geändert, und mittels *PUT* neue Resourcen erzeugt.
Die econOffice<sup>&reg;</sup> REST-API hält sich an diese Konvention.

* Responses sind grundsätzlich in den Formaten XML und JSON verfügbar.
* Responses können in mehreren Versionen (d.h. Strukturierung/Umfang) vorliegen. Eine Beschreibung der einzelnen Versionen finden Sie bei der Beschreibung des jeweiligen Services.

Vorhandene REST-Services:

|Service|URL|GET|POST|PUT|DELETE|
|---|---|:-:|:-:|:-:|:-:|
[Authentifizierung](/login)|login|&#10004;|&#10004;|&#10008;|&#10004;|
[Kontakt-Adresse](/contacts/contactAddress)|contactAddress|&#10004;|&#10004;|&#10004;|&#10004;|
[Kontakt-Liste](/contacts/contactAddresses)|contactAddresses|&#10004;|&#10008;|&#10008;|&#10008;|
[Vollständiger Kontackt](/contacts/contact)|contact|&#10004;|&#10008;|&#10008;|&#10008;|
[Wechselkurse](/exchangeRates)|exchangeRates|&#10004;|&#10008;|&#10008;|&#10008;|
[Dateien](/files/file)|files|&#10004;|&#10008;|&#10004;|&#10008;|
[Einstellungen](/settings/settingList)|settings|&#10004;|&#10008;|&#10008;|&#10008;|
[Einstellung](/settings/setting)|setting|&#10004;|&#10008;|&#10008;|&#10008;|
[System Vorgaben](/system)|system|&#10004;|&#10008;|&#10008;|&#10008;|

Legende

|Symbol|Beschreibung|
|:-:|---|
|&#10004;|Vorhanden|
|&#10008;|Gibt es nicht|
