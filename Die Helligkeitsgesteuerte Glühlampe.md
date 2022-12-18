# Die helligkeitsgesteuerte Glühlampe
## Links

1. [Stundenprotokolle](https://github.com/philipp-arvid/philipp-arvid/blob/main/README.md)
2. [Einleitung](#Einleitung)
3. [Entwicklung des Projekts](#Entwicklung)
4. [Fazit](#Fazit)

<h1>1. Einleitung</h1> <a name="Einleitung"></a>

<h3>1.1 Das Team</h3>

Als Team haben sich Arvid Späth und Philipp Rinne zusammengeschlossen. Dies haben wir aufgrund vorheriger erfolgreicher Team-/Gruppenarbeiten gemacht. 
Außerdem waren wir beide sehr interessiert an Informatik und waren uns einig, dass wir viel Arbeit in das Projekt stecken wollen. 
Des Weiteren waren wir uns einig, dass wir ein Physical Computing Projekt durchführen wollen. 
Also haben alle Vorstellungen zueinander gepasst und wir haben unser Projekt zusammen gestartet

 <h3>1.2 Der Arduino</h3>

Das Projekt ... ist wie schon gesagt ein Physical Computing Projekt.
Dies ist, unserer Meinung nach, besonders spnnend, weil man die Software und Hardware kombiniert. Wir hatten jeder besondere Interesse in einem Gebiet. 
Arvid interessiert besonders die Software und Philipp die Hardware. 
Dies passte gut zusammen, da wir beide uns besonders in unserem Bereich informierten und dann dem anderen jeweils die ausführungen und den Aufbau erklären konnten.
Dies klappte sehr gut, weil wir den anderen Bereich , welcher dann vom Partner erklärt wurde, deutlich schneller verstanden. 
Besonders gereitzt hat uns am Arduino, dass man die Theorie sozusagen mit der Praxis verbinden kann.
Also kann man seine Idee auch in der Realität umsetzen und diese kann eventuell auch in der Zukunft genutzt werden. 
Darüber haben wir uns im Fazit noch genauer Gedanken gemacht.

<h3>1.3 Genutzte Programme</h3>

Arduino App
Die Arduino App ist natürlich die Grundlage unseres Projekts. Über diese haben wir unser Projekt gesteuert. Wir haben mit einem Arduino UNO gearbeitet.
Über die Aruino App haben wir den Arduino gesteuert, welcher dann durch die Anweisungen die Helligkeit der Glühbirne steuert.
Für dies Programm haben uns am Anfang Videos geholfen. Am Ende war es aber besonders die Website der App, welche uns geholfen hat. 
Bei dieser gab es die allgemeinen Erklärungen, welche wuir dann auf unser Projekt gut übertragen konnten

github
github wurde als programm für die Stundenprotokolle und Projektseite genutzt. 
Dies war sehr passend, weil Github ein Dienst zurVersionsverwaltung zur Software-Entwicklu8ng ist. 
Also Konnte man hier sehr gut das Projekt dokumentieren, da man gut Bilder und auch den Code vom Arduino einfügen kann.

Fritzing
<h1>Entwicklung des Projekts</h1> <a name="Entwicklung"></a>

<h3>2.1 Vorgehen </h3>

Am Anfang hat Herr Buhl uns erstmal gesagt, dass wir die Grundlagen des Arduinos kennenlernen sollen. 
Also haben wir mit einfach ganz einfachen Code eine LED zum leuchten gebracht.
Danach haben wir sie zum Blinken genbracht und daraufhin haben wir mehrere  LEDs eingebaut. 
Also haben wir erst die einafchsten Grundlagen gelernt und sie dann in das Projekt eingebaut. Am Anfang haben wir es dann natürlich weiterentwickelt.
Dieses Vorgehen haben wir als sehr gut erachtet und somit bei den weiteren Versuchen auch umgesetzt. Dies gilt für die Photoiode und auch die Glühlampe. 
Also haben wir  die Photoiode erst Werte aufnehmen lassen und gesehen. Ab dann wussten wir, wie sie funktioniert und haben sie mit der LED kombiniert. 
Die Glühlampe haben wir erst ohne Arduino angemacht, um die Grundlagen wie Stromkreis, usw. wieder aufzufrischen.
Dann haben wir die Glühlampe mit dem Arduino gesteuert und zulatzt dann mit den Photoioden kombiniert.
Außerdem hatten wir eine sehr gute Teamarbeit aufgrund der unterschiedlich stärkeren Interessen. 
Da wir aber auch am anderen Thema interessiert waren und die vorherigen Schritte auch erklärt bekommen haben, 
konnten wir bei Problemen dem anderen sehr effektiv helfen. Da es immer mal Probleme gab, haben wir uns beide mit beiden Themen viel beschäftigt und sie verstanden.
Am Anfang haben wir viel verscuht mit Videos zu lernen und de Sachen zu verstehen.
Mit der Zeit haben wir aber gemerkt, dass wir uns schon so gut auskennen, dass wir die meisten Fehler oder auch einige Pläne durch logisches Denken umsetzen können.
Außerdem haben wir mehr auf der Arduino-Seite gelesen. Denn sobald es spezieller wird, gibt es weniger verständliche Videos. 
Also haben wir am Ende unser Projekt durch nachdenken über Fehler und die Arduino-Seite beendet. Dies ging deutlich schneller und war erfolgreicher.


<h3> 2.2 Die Idee</h3>

Als Gruppe haben wir uns ja wie schon gesagt auf ein Projekt des physical Computings geeinigt.
Dann haben wir uns einige Projekte angeguckt und haben uns überlegt, dass wir auch etrwas messen und steuern möchten.
Dabei haben wir uns überlegt, dass wir mit Licht arbeiten wollen, weil dies eine gute Herausforderung darstellt, weil es aufgrund der schnell wechselnden Helligkeit,
schwierig ist, die Helligkeit zu steuern. Dies hätte zu stark schwankenden Werten kommen können. Aber trotz der möglichen Probleme wollten wir das Projekt angehen.
Dies wollten wir auf einen Schuhkarton übertragen, weil wir nicht das Material haben, um das Projekt in einem Raum auszuführen. 
In den ersten beiden Einzelstunden und einer Doppelstunde haben wir uns überlegt, dass wir dieses Projekt entwickelt und uns überlegt, dass wir es umsetzen wollen.
Dann haben wir das Projekt gestartet. Der Ablauf und die Entwicklungen sind dann in unseren Stundenprotokollen sichtbar.

<h3> 2.3 Softwaretechnische Umsetzung </h3>
 Die Aufgabe des Software ist es, die gemessenen Daten der Photodioden zu kombinieren und dann die Glühlampe in Abhängigkeit dieser Daten zu steuern. Dabei übernimmt offensichtlich der Arduino diese Aufgabe. 
 
<details>
	<summary>Auschnitt des Codes</summary>
	
```c
int licht;
int licht2;
	
	
void setup() {
	
	  Serial.begin(9600);
}
	
void loop() {

  licht= analogRead(0);
  licht2= analogRead(1);
  delay(20);

  Serial.println(licht + licht2);

}	
	
```
	
</details>
 

<li>
Der Ausschnitt zeigt das Erfassen der Lichtintensitäten durch die beiden Photodioden. Am Anfang werden die zwei Variablen Licht und Licht2 eingeführt, die für das gemessene Licht der beiden eingebauten Photodioden stehen. Mit Serial.beginn(9600) wird generell der Serielle Monitor eingeführt, bei dem wir dann später unsere erfassten Lichtintensitäten ablesen können. Danach haben wir den beiden vorgestellten Variablen einne zugehörigen Input des Arduinos zugewiesen. Jetzt entsprechen die beiden VAriablen jeweils den gemessenen Werten bei AnalogRead(0) und AnalogRead(1). Dazu haben wir noch eine Verzögerung der Messungen eingeführt, da dies später gegen Rückkopplungen hilft. Als letztes haben wir die beiden VAriablen dann zusammen addiert und beschreiben, dass diese vom Seriellen MOnitor angezeigt werdnen sollen. Somit werden nu die beiden gemessen Lichtintensitäten der beiden Photodioden über einen seriellen Monitor mit iener Verzögerung von 20 Millisekunden angezeigt.
</li>

 
<details>
	<summary>Auschnitt des Codes</summary>
	
```c
	
const int transistor = 10;
int aus;
	
void setup() {
	
  pinMode (10, OUTPUT);	
	
}
	
void loop() {
	
          aus = 255-map(licht + licht2, 150, 800, 0, 255);
	
          if (licht + licht2 > 800)
          aus=0;
          if (licht + licht2 < 150)
          aus=255;

  analogWrite(transistor, aus);
				   
}
				   
```
	
</details>
 
	
	
	
<h3> 2.4 Hadwaretechnische Umsetzung </h3>
 
<h3> 2.5 Das Endprodukt </h3>


<h1>3. Fazit</h1> <a name="Fazit"></a>
 

Wir ziwehen ein sehr positivwes Fazit, weil wir beide viel Spaß am Projekt hatten. Durch das beidseitige Interesse gab es auch immer eine sehr produktive Zusammenarbeit.
Mit dem Endprojekt sind beide sehr zufrieden. Wir konnten leider den Zielwert nicht umsetzen, aber mussten einsehen, dass dies bei der Arbeit mit Helligkeit sehr schwierig wäre. 
Zu beginn war es eine sehr effektive gemeinsame Pklanung, welche wir dann mit der Zeit gut umsetzen konnten.
Aufgrund unserer guten Arbeit waren wir früher fertig und konnten unser Projekt auf Rat von Herrn Buhl noch durch eine Glühlampe verbessern.
Wir sind sehr froh die Idee jetzt in wirklichkeit umgesetzt zu haben. Dies freut und fasziniert uns an dem physical computing. 
Insgesamt haben wir nun gute Kentnisse im Bereich des Arduinos. Dies gilt für die Software und die Hardware. 
Das Voranbringen des Projekts lief sehr gut, da wir beide ei9nen großen Willen hatten.
Wir haben unhs auch 2 mal am Wochenende zusammengesetzt und am Projekt weitergearbeitet. 
Auch wenn es manchmal längere Phasen ohne Erfolg gab überwog die Freude über das Lösen diese Probems dann umso mehr.
Aufgrund der guten Zusammenarbeit, der Freude und des Erfolgs (welche auch durch die frühe fertigstellung gezeigt wurde), 
haben wir uns entschieden auch im 2. Halbjahr wieder zusammenarbeiten. Ein gutes Klima in der Gruppe ist wichtig, da sonst keine effektive Zu8sammenarbeit stattfinden kann.
Da es bei speziell diesem Projekt keine großen Verbesserungen, welche auch für uns möglich sind, mehr gibt haben wir uns entschieden in eine ähnliche Richtung zu gehen.
Für unser nächstes Projekt arbeiten wir wieder, aufgrund des Interesses und der Vorkentnisse, mit dem physical computing. Einen genaueren Plan, für das kommende Projekt, gibt es in unserem Ausblick.

<h3> 3.1 Nutzung im Alltag </h3>

Wir haben uns ein Physical Computing Projekt ausgesucht, weil uns, wie schon gesagt, der Bezug zur Realität interessiert. 
Somit haben wir uns auch während der Projektentwickulung immer wieder überlegt, wofür man das Projekt im Alltag nutzen könnte.
Als erste möglichkeit ist es ganz normal das Licht im Haus oder vor dem Haus somit zu regeln.
Dies würde dazu führen, dass das Licht nicht unnötig bei Helligkeit an ist, oder es halb dunkel ist. 
Wenn man den Strom direkt aus der Stromquelle schon steuert, ist dies auch dutlich umweltfreundlicher, da man nicht immer den ganzen Strom braucht.
Dies würde auch für einen selber zu einem Ersparnis werden, weil man weniger Strom bezahlt. 
Das gleiche gilt für Laternen in der Stadt. 
Auch im Auto könnte man dies einbauen, weil somit das Unfallrisiko gemindert wird, weil das Licht automatisch gesteuert wird und somit nicht vergessen wird anzumachen. 
Des Weiteren blendet es den entgegenkommenden und vor einem fahrenden Verkehr nicht, weil das Licht von dort such wahrgenommen wird und das eigene somit geschwächt wird.
Also kann man diese "Erfindung" invielen und auch wichtigen Bereichen des Alltags nutzen. Es dient nicht nur dem Aussehen, wie am Haus, sondern auch der Sicherheit, wie im Auto.

<h3> 3.2 Ausblick </h3>

Für die Zukunft haben wir uns überlegt, dass wir weiter mit dem Arduino arbeiten wollen, weil wir jetzt schon ein gutes Grundwissen dazu haben. 
Wir wollen aber nicht mehr mit der Helligkeit, sondern mit der wärme arbeiten. 
Unser Ziel ist es nämlich, dasswir durch eine Glühlampe, welche wärme abgibt, die Temperatur im Raum steuern können. 
Also messen wir diesmal die Temperatur, statt die Helligkeit, um auch noch etwas neues zu dem bereits bekannten zu lernen. 
Bei diesem Projekt ist uns besonders wichtig, dass die Wärme auch wirklich gehalten oder hergestellt wird. Dies ist auch noch eine veränderung, 
weil man mit der HElligkeit keinen genauen Wert erreichen kann.
