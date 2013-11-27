[Übersicht](../)

# Login Service

URI: ${domain}/rest/login

Beispiel: http(s)://beispiel.econoffice.com/rest/login

## GET
Zeigt alle Angaben zum aktuell authentifizierten Benutzer.

Parameter: keine

Erfolg - der Benutzer ist eingeloggt (Http-Status: 200 - OK)

```xml
  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <response>
      <client>demo</client>
      <version>1</version>
      <created>Mon Oct 21 14:10:17 CEST 2013</created>
      <user>
          <authUserRid>0000000000000001</authUserRid>
          <username>demo</username>
          <email>demo@example.com</email>
          <contact>
              <resourceId>0000000000000001</resourceId>
              <contactNumber>1</contactNumber>
              <structuredName>
                  <companyLine1>Datura Informatik + Organisation AG</companyLine1>
                  <companyLine2>Software Entwicklung und Design</companyLine2>
                  <addressPersonal>true</addressPersonal>
              </structuredName>
              <structuredAddress/>
              <unstructuredName/>
              <unstructuredAddress>
                  <line1>Churerstrasse 22</line1>
                  <line2>8808 Pfäffikon SZ</line2>
              </unstructuredAddress>
              <phonenumbers>
                  <phone>
                      <note>Hauptnummer</note>
                      <number>+41 44 555 0000</number>
                      <resourceId>C000000000000005</resourceId>
                  </phone>
              </phonenumbers>
              <emailAddresses>
                  <email>
                      <emailAddress>mailto:demo@example.com</emailAddress>
                      <note>Allgemein</note>
                      <resourceId>C000000000000001</resourceId>
                  </email>
              </emailAddresses>
              <websites>
                  <website>
                      <note>Firmen-Website</note>
                      <resourceId>C000000000000002</resourceId>
                      <url>http://www.example.com</url>
                  </website>
                  <website>
                      <note>Produkte-Website</note>
                      <resourceId>C000000000000003</resourceId>
                      <url>http://www.example.biz</url>
                  </website>
                  <website>
                      <note>Web-App</note>
                      <resourceId>C000000000000004</resourceId>
                      <url>http://demo.example.org/webApp</url>
                  </website>
              </websites>
              <otherMedia/>
              <customFields>
                  <customField>
                      <customLabel>
                          <labelCode>date-of-birth</labelCode>
                          <de>date-of-birth</de>
                      </customLabel>
                      <customValue/>
                  </customField>
                  <customField>
                      <customLabel>
                          <labelCode>date-of-death</labelCode>
                          <de>date-of-death</de>
                      </customLabel>
                      <customValue/>
                  </customField>
                  <customField>
                      <customLabel>
                          <labelCode>hobbies</labelCode>
                          <de>hobbies</de>
                      </customLabel>
                      <string/>
                  </customField>
                  <customField>
                      <customLabel>
                          <labelCode>assests</labelCode>
                          <de>assests</de>
                      </customLabel>
                      <string/>
                  </customField>
              </customFields>
          </contact>
          <mandators>
              <Mandator>
                  <resourceId>373B9E211E210000</resourceId>
                  <mandatorId>Mandant_01</mandatorId>
                  <requiresPassword>false</requiresPassword>
                  <short>undefined</short>
                  <medium>undefined</medium>
                  <long>undefined</long>
                  <balanceDate>
                      <month>12</month>
                      <day>31</day>
                  </balanceDate>
                  <currency>
                      <isoCode>CHF</isoCode>
                  </currency>
              </Mandator>
              <Mandator>
                  <resourceId>373B9E221E22001F</resourceId>
                  <mandatorId>Mandant_03</mandatorId>
                  <requiresPassword>true</requiresPassword>
                  <short>undefined</short>
                  <medium>undefined</medium>
                  <long>undefined</long>
                  <balanceDate>
                      <month>6</month>
                      <day>30</day>
                  </balanceDate>
                  <currency>
                      <isoCode>EUR</isoCode>
                  </currency>
              </Mandator>
              <Mandator>
                  <resourceId>373B9E221E220273</resourceId>
                  <mandatorId>Mandant_07</mandatorId>
                  <requiresPassword>false</requiresPassword>
                  <short>undefined</short>
                  <medium>undefined</medium>
                  <long>undefined</long>
                  <balanceDate>
                      <month>12</month>
                      <day>31</day>
                  </balanceDate>
                  <currency>
                      <isoCode>CHF</isoCode>
                  </currency>
              </Mandator>
          </mandators>
          <roles>
              <role>
                  <roleRid>0000000000000001</roleRid>
                  <name>admin</name>
                  <de>Administrator</de>
                  <en>Administrator</en>
                  <permissions>
                      <permission>
                          <de>Leistungserfassung</de>
                          <en>Recording of performance</en>
                          <permissionRid>0000000000000001</permissionRid>
                      </permission>
                      <permission>
                          <de>Hauptbuch</de>
                          <en>Ledger</en>
                          <permissionRid>0000000000000002</permissionRid>
                      </permission>
                      <permission>
                          <de>Debitoren</de>
                          <en>Debtors</en>
                          <permissionRid>0000000000000003</permissionRid>
                      </permission>
                  </permissions>
              </role>
              <role>
                  <roleRid>0000000000000003</roleRid>
                  <name>guest</name>
                  <de>Gast</de>
                  <en>Guest</en>
                  <permissions/>
              </role>
              <role>
                  <roleRid>0000000000000002</roleRid>
                  <name>user</name>
                  <de>Benutzer</de>
                  <en>User</en>
                  <permissions/>
              </role>
          </roles>
      </user>
  </response>
```

Misserfolg - Kein Benutzer ist eingeloggt (Http-Status: 401 - Unauthorized):

```xml
  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <response>
      <error>The current Subject is not authenticated.  Access denied.</error>
  </response>
```

## POST
Loggt den Benutzer ein. 

Parameter:
* username: Es wird erwartet, dass der username in der Form *username*@*kundenname* vorliegt
* password: Das Passwort des Benutzers (Die Verschlüsselung erfolgt über SSL)

Erfolg - Benutzerangaben stimmen (Http-Status: 200 - OK)

Gleiche Antwort, wie bei GET (siehe dort)


Misserfolg - Parameter fehlt (Http-Status: 400 - Bad Request)

```xml
  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <response>
      <error>Der notwendige Parameter 'username' enthält keine Wert.</error>
  </response>
```

Misserfolg - Authentifizierung schlägt fehl (Http-Status: 401)

```xml
  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <response>
      <error>Authentifizierung fehlgeschlagen.</error>
  </response>
```

## DELETE
Loggt den Benutzer aus.

Parameter: keine

Erfolg - Der Benutzer war eingeloggt (Http-Status: 303 - Redirect)

Es findet aus technischen Gründen ein Weiterleitung auf eine andere Seite statt (${domain}/rest/bye).

Die dortige Antwort hat immer den Http-Status: 200 - OK)

```xml
  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <response>
      <client>demo</client>
      <version>1</version>
      <created>Mon Oct 21 14:59:41 CEST 2013</created>
      <message>Bye</message>
  </response>
```

Misserfolg - Der Benutzer ist nicht eingeloggt (Http-Status: 401)

```xml
  <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
  <response>
      <error>The current Subject is not authenticated.  Access denied.</error>
  </response>
```
