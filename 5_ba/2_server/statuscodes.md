# Statuscodes

## 100: Continue

Die Anfrage wurde dem Server korrekt übertragen und der Server wartet auf weitere Anweisungen des Clients zur Ausführung dieser Anfrage.

## 102: Processing

Bei zeitintensiven Anfragen wird dieser Status Code verwendet, um ein Timeout zu vermeiden.

## 200: OK

Dieser Status Code wird ausgegeben, wenn die Anfrage korrekt und ohne Fehler ausgeführt wurde. Zum Beispiel wenn eine angefragte Seite oder ein Dokument verfügbar ist und an den Client übertragen wurde.

## 301: Moved Permanently

Die vom Client angeforderten Daten wurden permanent auf eine andere Adresse verschoben bzw. umgeleitet und die alte Adresse ist nicht mehr gültig. Dabei wird direkt mit angegeben unter welcher neuen Adresse die Daten nun zu finden sind.

Für die Suchmaschinenoptimierung ist dieser Status Code besonders wichtig. Wenn sich beispielsweise bei einem Relaunch die URL-Struktur ändert oder Seiten gelöscht werden, sollte ein 301-Redirect eingerichtet werden, um 404-Fehlerseiten zu vermeiden und damit das Suchmaschinenranking abzuwerten.

Durch die Umleitung steuern Sie den Crawler und leiten Ihn auf eine andere Seite weiter, welche die gleichen oder ähnliche Inhalte hat. Der Vorteil von 301-Redirects ist, dass der Linkjuice (Verknüpfungsstärke) vererbt wird. Das bedeutet, dass die Anzahl und Qualität von Backlinks der alten Seite auf die neue Seite übertragen werden und dieser Linkjuice somit nicht verloren geht.

Auch bei einem Wechsel der Domain sollten Sie auf korrekte Weiterleitungen achten und die Seiten 1:1 weiterleiten, anstatt alle Unterseiten auf die Startseite zu leiten. Da der Google-Bot beim Crawlen Ihrer Seite spätestens ab der vierten oder fünften Weiterleitung aufhört, sollten Sie lange Weiterleitungsketten vermeiden.

## 302: Moved Temporarily

Mit dem HTTP Status Code 302 wird eine temporäre Weiterleitung bezeichnet, da die Ressource nur vorrübergehend unter einer anderen Adresse zu finden ist. Bei der Suchmaschinenoptimierung ist es sehr wichtig zwischen 301 und 302 zu unterscheiden, da bei einer 302-Weiterleitung kein Linkjuice vererbt wird und dieser somit unter Umständen verloren geht. Die ursprüngliche Adresse bleibt bei einem Status Code 302 weiterhin gültig, sodass der Googlebot diese Seite weiterhin indexiert.

## 400: Bad Request

Der Client hat eine Anfrage mit Syntaxfehlern geschickt, sodass die Anfrage nicht vom Server bearbeitet werden kann. Die Anfrage sollte korrigiert und erneut gesendet werden.

## 404: Not Found

Der Status Code 404 ist einer der häufigsten Fehlercodes und wird dann ausgegeben, wenn die vom Client angeforderte Ressource nicht vom Server gefunden wurde. Das ist in der Regel dann der Fall, wenn die angeforderte URL nicht oder nicht mehr existiert. Dafür kann es verschiedene Gründe geben:

Der Client hat eine falsche URL angefordert, die nie existierte.
Die angeforderten Daten wurden an einem neuen Ort abgelegt und die internen Links wurden nicht angepasst.
Tote Links: Aus externen Quellen wird auf eine URL verlinkt, deren Ressourcen umgezogen wurden, sodass die URL veraltet ist und nicht angepasst wurde.
Durch 404 Fehler wird nicht nur die Nutzerfreundlichkeit Ihrer Webseite eingeschränkt, je nach Anzahl der 404 Fehler kann dadurch auch das Ranking Ihrer Seite von Google schlechter ausfallen. In der Google Search Console finden Sie heraus, welche Seiten mit 404 Fehlern von dem Googlebot beim Crawlen gefunden wurden. Auch interne und externe Verlinkungen dieser URL finden Sie dort, sodass diese angepasst werden können.

404 Fehler können Sie ganz einfach durch 301-Redirects beheben. Wie bereits im Abschnitt zum 301 Status Code beschrieben, ist dies besonders bei einem Relaunch oder einem Domain-Umzug wichtig, da Seiten die nicht umgeleitet werden sonst mit dem HTTP Status Code 404 ausgegeben werden.

## 410: Gone

Dieser Status Code signalisiert, dass die angeforderte Ressource nicht mehr existiert und es auch keine alternative Adresse gibt. Dieser Status Code wird von Serveradministratoren genutzt, wenn die Ressource dauerhaft entfernt wird.

## 500: Internal Server Error

Dieser HTTP Status Code steht für einen internen Serverfehler, sodass die angeforderte Ressource nicht zurückgeliefert werden kann. Dieser erscheint häufig bei Fehlerhaften Einträgen in der .htaccess-Datei.

## 503: Service Unavailable

Aufgrund von hohen Datenaufkommen oder Wartungsarbeiten kann es dazu kommen, dass der Dienst derzeit nicht verfügbar ist. Der Server steht also temporär nicht zur Verfügung, unter Umständen steht in der Statusmeldung auch, wann die Anfrage erneut gesendet werden kann.
