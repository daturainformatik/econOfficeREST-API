# econOffice<sup>&reg;</sup> REST-API

An dieser Stelle finden Sie die Spezifikationen der verfügbaren REST-APIs.

Leider ist im allgmeinen nicht völlig klar definiert, wodurch sich *POST*- und *PUT*-Requests unterscheiden.
In der Regel werden mittels *POST* neue Resourcen erstellt, und mittels *PUT* bestehende Resourcen geändert.
Die econOffice<sup>&reg;</sup> REST-API hält sich an diese Konvention.

* Responses sind grundsätzlich in den Formaten XML und JSON verfügbar.
* Responses können in mehreren Versionen (d.h. Strukturierung/Umfang) vorliegen. Eine Beschreibung der einzelnen Versionen finden Sie bei der Beschreibung des jeweiligen Services.
* Responses werden mittels des Parameters *asFile=true* als Datei-Stream übermittelt. D. h. Die Antwort kann als Datei gespeichert werden.

Vorhandene REST-Services:

* Authentifizierung: [login](/login)
* Mandanten: [mandator](/mandator)
* Wechselkurse: [exchangeRates](/exchangeRates)
* Kontakt-Liste: [contactList](/contacts/contact)
* Kontakt-Adresse: [contactAddress](/contacts/contactAddress)
