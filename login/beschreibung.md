# Login Service

URI: ${domain}/rest/login
Beispiel: http(s)://beispiel.econoffice.com/rest/login

## GET
Zeigt alle Angaben zum aktuell authentifizierten Benutzer.

Parameter: keine

Erfolg - der Benutzer ist eingeloggt (Http-Status: 200 - OK)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.get.xml), 
* [JSON](https://github.com/daturainformatik/econOfficeREST-API/login/login.get.json)

Misserfolg - Kein Benutzer ist eingeloggt (Http-Status: 401 - Unauthorized):
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.unauthorized.xml), 
* [JSON](https://github.com/daturainformatik/econOfficeREST-API/login/login.unauthorized.json)

## POST
Loggt den Benutzer ein. 

Parameter:
* username: Es wird erwartet, dass der username in der Form *username*@*kundenname* vorliegt
* password: Das Passwort des Benutzers (Die Verschlüsselung erfolgt über SSL)

Erfolg - Benutzerangaben stimmen (Http-Status: 200 - OK)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.post.xml), 
* [JSON](https://github.com/daturainformatik/econOfficeREST-API/login/login.post.json)

Misserfolg - Angabe fehlt (Http-Status: 400 - Bad Request)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.bad_request.xml),
* [JSON](https://github.com/daturainformatik/econOfficeREST-API/login/login.bad_request.json),

Misserfolg - Authentifizierung schlägt fehl (Http-Status: 401)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.unauthenticated.xml)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.unauthenticated.json)

## DELETE
Loggt den Benutzer aus.

Parameter: keine

Erfolg - Der Benutzer war eingeloggt (Http-Status: 303 - Redirect)
Es findet aus technischen Gründen ein Weiterleitung auf eine andere Seite statt (${domain}/rest/bye).

Die dortige Antwort hat immer den Http-Status: 200 - OK)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.bye.xml)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.bye.json)

Misserfolg - Der Benutzer ist nicht eingeloggt (Http-Status: 401)
* [XML](https://github.com/daturainformatik/econOfficeREST-API/login/login.unauthorized.xml), 
* [JSON](https://github.com/daturainformatik/econOfficeREST-API/login/login.unauthorized.json)
