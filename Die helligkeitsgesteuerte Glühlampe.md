# Die helligkeitsgesteuerte Glühlampe
## Links

 [Stundenprotokolle](https://github.com/philipp-arvid/philipp-arvid/blob/main/README.md)
1. [Einleitung](#Einleitung)
2. [Entwicklung des Projekts](#Entwicklung)
3. [Fazit](#Fazit)

<h1>1. Einleitung</h1> <a name="Einleitung"></a>

<h3>1.1 Das Team</h3>

Als Team haben sich Arvid Späth und Philipp Rinne zusammengeschlossen. Dies haben wir aufgrund vorheriger erfolgreicher Team-/Gruppenarbeiten gemacht. Außerdem waren wir beide sehr interessiert an Informatik und waren uns einig, dass wir viel Arbeit in das Projekt stecken wollen. Des Weiteren waren wir uns einig, dass wir ein Physical-Computing Projekt durchführen wollen. Also haben alle Vorstellungen zueinander gepasst und wir haben unser Projekt zusammen gestartet.

 <h3>1.2 Der Arduino</h3>

Das Projekt "Helligkeitsgesteuerte Glühlampe" ist wie schon gesagt ein Physical-Computing Projekt.
Dies ist, unserer Meinung nach, besonders spannend, weil man Software und Hardware kombiniert. Wir hatten jeder besonderse Interesse in einem Gebiet. 
Arvid interessierte sich besonders für die Software des Arduinos und Philipp für die Hardware, die wir zusammen mit dem Modell Arduino UNO kombiniert haben. 
Dies passte gut zusammen, da wir beide uns besonders in unserem Bereich informierten und dann dem anderen jeweils die Ausführungen und den Aufbau erklären konnten.
Dies klappte sehr gut, weil wir den anderen Bereich, welcher dann vom Partner erklärt wurde, deutlich schneller verstanden haben und so auch effektiv arbeiten konnten. Aber natürlich haben wir den Großteil der Arbeit zusammen am Computer gemacht und konnten uns so recht schnell ein gutes Grundverständnis über die Funktionalitäten des Arduinos erarbeiten. Mit der Zeit sind uns auch erst die vielen Möglichkeiten mit dem Arduino seine Ideen in die Realität umsetzen, welche sich möglicherweise als tatsächlich nützlich erweisen. 


<h3>1.3 Genutzte Programme</h3>

Arduino-IDE

Das Arduino Programm ist natürlich die Grundlage unseres Projekts und der Software-Teil des Arduino UNOs. Mit dem Programm lassen sich Sketches schreiben, die die Funktionsweise des Arduinos programmieren und unser Projekt ermöglichen. 

Github

Github wurde als Programm für die Stundenprotokolle und Projektseite genutzt. Github ist ein Dienst zur Versionsverwaltung zur Software-Entwicklung, weshalb sich hier gut Projekte mit Bildern und Codes dokumentieren lassen. 

Fritzing

Fritzing ist eine Software mit der man die Hardware, also unsere Steckverbindungen, digital und übersichtlich darstellen kann.

<h1>Entwicklung des Projekts</h1> <a name="Entwicklung"></a>

<h3>2.1 Vorgehen </h3>

Am Anfang hat Herr Buhl uns  gesagt, dass wir die Grundlagen des Arduinos kennenlernen sollen. Also haben wir mit einem ganz einfachen, vorinstallierten Code eine LED zum Leuchten gebracht. Danach haben wir sie zum Blinken genbracht und daraufhin haben wir mehrere LEDs eingebaut. 
Also haben wir erst die Grundlagen gelernt, um dann von dort, Schritt für Schritt mehr Wissen zu erarbeiten. Dieses Vorgehen haben wir haben wir durch das Projekt beibehalten, also haben wir zum Beispiel die Photodiode erst Werte aufnehmen lassen und diese im seriellen Monitor uns anzeigen lassen und erst anschließend eine LED im Aufbau hinzugefügt. Erst wenn wir verstehen, wie ein Teil unseres Gesamtprojekts funktioniert, gehen wir einen Schritt weiter. So haben wir auch später, im Verlauf des Projektes die Glühlampe erst ohne Arduino angebracht und zum leuchten gebracht, um die Grundlagen wie Stromkreis, usw. wieder aufzufrischen. Dann haben wir die Glühlampe mit dem Arduino in Kombination mit dem Transistor gesteuert und zuletzt dann mit den Photodioden vervollständigt. Da es immer mal Probleme gab, haben wir viel, gerade in unserem Bereich der Verwendung des Arduinos, auch recht viel recherchiert. Viel haben uns Youtube Videos und Seiten wie Arduino Reference geholfen, um ein besseres Verständnis zu erlangen und so unsere Problem zu lösen. Doch manchmal haben wir uns auch selber, kreativ Lösungen zu Problemen erschlossen, was auch überaschend gut funktioniert hat. Somit konnten wir insgesamt zielgerichtet mit der Kombination aus Recherche und Anwendung bereits erlerntem Wissens auf ein neues Problem, unser Projekt gut fertigstellen. 


<h3> 2.2 Die Idee</h3>

Wie oben erkärt, haben wir uns für ein Projekt mit Physical-Computings geeinigt.
Dann haben wir uns einige Projekte angeguckt und haben uns überlegt, dass wir auch etwas messen und steuern möchten.
Dabei haben wir uns überlegt, dass wir mit Licht arbeiten wollen, weil dies eine gute Herausforderung darstellt, weil es aufgrund der schnell wechselnden Helligkeit,
schwierig ist, die Helligkeit zu steuern. Dies hätte zu stark schwankenden Werten kommen können, aber trotz der möglichen Probleme haben wir uns dazu entschieden das Projekt anzugehen. Dabei schwebte uns ein Raum vor, der mit Lichtsensoren ausgestattet ist und durch ein verschliessbares Fenster, oder eine Art Tür mit Tageslicht befüllt werden kann. Dann haben wir uns überlegt, dass es im Raum eine Lampe geben sollte, die Abhängig von dem Licht im Raum hell beziehungsweise dunkel leuchtet. Dabei soll der Arduino so programmiert sein, dass er die Informationen von den Lichtsensoren im Raum aufnimmt und sie so verarbeitet, dass als Konsequenz eine Lampe stark oder schwach leuchtet. Das Ziel ist immer ein bestimmte Helligkeit im Raum zu haben, dass es automatisiert nie dunkel werden kann. 


<h3> 2.3 Softwaretechnische Umsetzung </h3>
 Die Aufgabe der Software ist es, die gemessenen Daten der Photodioden zu kombinieren und dann die Glühlampe in Abhängigkeit dieser Daten zu steuern. Dabei übernimmt offensichtlich der Arduino diese Aufgabe. 
 
 
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
 

<li>Der Ausschnitt zeigt das Erfassen der Lichtintensitäten durch die beiden Photodioden. Am Anfang werden die zwei Variablen Licht und Licht2 eingeführt, die für das gemessene Licht der beiden eingebauten Photodioden stehen. Mit Serial.beginn(9600) wird generell der Serielle Monitor eingeführt, bei dem wir dann später unsere erfassten Lichtintensitäten ablesen können. Danach haben wir den beiden vorgestellten Variablen einen zugehörigen Input des Arduinos zugewiesen. Jetzt entsprechen die beiden Variablen jeweils den gemessenen Werten bei AnalogRead(0) und AnalogRead(1). Dazu haben wir noch eine Verzögerung der Messungen eingeführt, da dies später gegen Rückkopplungen hilft. Dies haben wir in Form der Delay-Funktion umgesetzt. Delay(20) heißt also, dass alle 20 Millisekunden gemessen wird. Als letztes haben wir die beiden Variablen dann zusammen addiert und beschreiben, dass diese vom Seriellen Monitor angezeigt werden sollen. Somit werden nur die beiden gemessen Lichtintensitäten der beiden Photodioden über einen seriellen Monitor mit einer Verzögerung von 20 Millisekunden angezeigt. </li>

 
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
 
<li>In Diesem Ausschnitt haben wir die Verwertung der Lichtintensitäten zu einem Wert für die Glühlampe programmiert. Zu Beginn bezeichnen wir den Transistor mithilfe einer Variable und halten die Variable konstant am Wert 10 mit "const". Als nächstes legen wir fest, dass der 10. Pin als Output dient, denn dort ist nämlich der Transistor angeschlossen, was wir vorher mit der Variable Transistor entspricht 10 veranschaulicht haben. Als Nächstes haben wir den Operator "Map" verwendet mit dem wir die gemessenen Lichtintensitäten in einen Ausgangswert übersetzen. Dafür haben wir zuerst die Variable ausformuliert, die den Ausgangswert entspricht und daher aus dem Map-Operator hervorgeht. Bei der Map-Funktion setzt man Parameter für den zu "mappenden" Wert ein, also in diesem Fall 150 als niedrigster möglicher gemessener Wert und 800 als höchster. Vor diesen Parametern setzt man den Wert der "gemappt" werden soll, also in diesem Fall "Licht+Licht2". Als nächstes setzt man Werte für andere Parameter ein, auf die, die vorherig in den anderen Parametern, in Kontext gesetzten Messwerte, übersetzt werden sollen. Dort haben wir 0 und 255 eingesetzt, dies liegt daran, dass wir "Analogwrite" benutzen und diese Funktion einen Wert von 0 bis 255 ausgeben kann. Also werden nun die gemessenen Lichtintensitäten, die von 150 bis 800 reichen können auf Werte von 0 bis 255 "übersetzt". Dies bedeutet, dass wenn zum Beispiel der Wert 800 gemessen wird, also das Maximum des Parameters des gemessenen Lichts, dies entsprechend auch in das Maximum für die in zu übersetzenden Parameter übersetzt wird. In diesem Fall wäre das also so, dass dann ein Wert bei "AnalogWrite" für 255 ausgegeben wird. Genau so wird zum Beispiel, wenn genau die Mitte von den Parametern 150 bis 800 gemessen wird, auch genau die Hälfte von 255 als Wert für "AnalogWrite" ausgegeben.        </li>
	
	
	
<li>Nun haben wir nur noch das Problem, dass wir es zwar geschafft haben Werte von Lichtintensitäten auf einen Wert für den Ausgang, also für den Transistor zu übersetzen, aber, dass dies nicht die richtigen Werte sind. Denn wenn zum Beispiel eine hohe Lichtintensität gemessen wird, würde dies bedeuten, dass auch ein hoher Wert ausgegeben wird, da der Lichtintensitäten Wert ja zunächst nur auf die Parameter von 0 bis 255 übersetzt wird. Aber dies würde auch bedeuten, dass dadurch bei viel Licht, auch die Glühbirne stark leuchtet, da ja auch ein hoher Wert ausgegeben wird. Also haben wir uns überlegt, dass das Maximum von den Werten die "AnalogWrite" annehmen kann, also 255, von dem gemessen Wert, der durch die Map-Funktion übersetzt wurde, subtrahiert wird. Denn wir wollen ja genau das Gegenteil: Wenn es hell ist soll es Dunkel werden und nicht anders herum. Dies ist mit der eben beschreiben Rechnung gegeben, denn wenn nun wieder zum Beispiel ein Wert von 800 gemessen wird, wird er zunächst auf einen Wert von 255 übersetzt und dann wird das Maximum, also 255 mit dem gemessen Wert, also 255 subtrahiert. Dadurch erhalten wir bei einer hohen Intensität, eine Glühlampe, die aus ist.  </li>	
	

<li>Anschließend haben wir noch ein Maximum und ein Minimum mit dem If() Operatoren formuliert. Das dient dazu, dass die Glühlampe mit Sicherheit nicht mehr leuchtet, auch wenn die gemessenen Werte 800 übertreffen. Denn wenn man nicht diese Grenzen formulieren würde, dann ist die Glühlampe nämlich einfach mit einer relativ mittleren Leuchtkraft aktiv, wenn "licht+licht2" den Wert 800 übertreffen. Da dies nicht von uns gewollt ist, haben wir die Obergrenze und Untergrenze formuliert, bei der es genau anders herum ist: Wenn Lichtintensitäten von niedriger als 150 gemessen werden, dann leuchtet sie auch mittelstark. Man könnte vorschlagen, dass man einfach die Parameter bei der Map-Funktion nach oben und unten hin ausweitet, da man dann ja das Problem von zu hohen oder niedrigen Werten ja dann behoben hätte, doch dies macht das "mappen" insgesamt nur unpräziser und ungenauer, wenn die Parameter zu groß sind, und da diese Parameter auch nur selten über- oder unterschritten werden, haben wir uns für den Operator If() entschieden. Hierbei haben wir das so geschrieben, dass wenn ein Wert unter 150 gemessen wird, der Output einen Wert von 255 (also dem Maximum) ausgibt, und wenn ein Wert über 800 gemessen, ein Wert von 0 ausgesendet wird( also geht die Glühlampe aus). Als Allerletztes haben wir dann "AnalogWrite" an der Stelle 10 ( den Wert für die Variable des Transistors) einen Output, der den  Wert von der Variable "aus" annimmt, welcher durch die eben beschriebene Weise berechnet wird. Dadurch, dass das im Loop passiert, haben wir einen funktionstüchtigen Code geschrieben, der die Glühlampe abhängig von der Helligkeit steuer kann. </li>
	
<details>
	<summary>fertiger Code</summary>
	
```c
	
const int transistor = 10;
int aus;
int licht;
int licht2;

void setup() {
	
  pinMode (10, OUTPUT);
	
  Serial.begin(9600);
	
}
	
void loop() {

  licht= analogRead(0);
  licht2= analogRead(1);
  delay(20);

  Serial.println(licht + licht2);

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
	
	
![neuste version_bb](https://user-images.githubusercontent.com/111414095/208496925-124610f5-ae61-4112-80e6-65ce1994ffc3.jpg)


	

	
<details>
	<summary>Bild</summary>	
	
   ![](IMG_2247.jpeg)
	
</details>	
	
Alle genutzten Teile konnten uns von der Schule gestellt werden.
	
<li>Als "Raum" haben wir einen Schuhkarton gewählt, weil wir mit den vorhandenen Materialien nicht einen Raum ausstatten konnten und dieser auch sehr gut alle Gegebenheiten eines normalen Raumes simulieren kann. Ein Schuhkarton war das perfekte Produkt, weil man ihn gut abdunkeln und wieder erhellen kann. Außerdem kann man durch ein Loch die Kabel des Arduinos mit dem PC verbinden und hatte somit nicht immer einen Lichtschlitz im Deckel.   </li>	
	
	
<li>Die Glühlampe, die unsere Lichtquelle darstellt ist eine reguläre Glühlampe mit 6V, die auch aus dem Inventar der Schule stammt. Am Anfang des Projekts haben wir noch mit LEDs gearbeitet, doch diese wurden im Laufe der Zeit mit dieser Glühlampe ersetzt.    </li>

<li>Damit diese 6V Glühlampe gesteuert werden kann, brauchten wir eine externe Energiequelle. Dafür haben wir ein externes Netzteil genutzt. Diese haben wir dann an die Steckdose angeschlossen und konnten es in den Stromkreis einbinden. Dadurch hat die Glühlampe genügend Strom bekommen, um zu leuchten.   </li>

<li>Ein weiterer Teil, das Herzstück, ist der Arduino. Dieser ist die Grundlage, weil jede Messung und Steuerung vom Arduino ausgeht. Dieser stellt nämlich die Verbindung zwischen Software und Hardware da. Bei der Hardware des Arduinos handelt es sich um das sogenannte Arduino-Board und die Software übernimmt das Programm Arduino IDE, welche den Sketch, also das Steuerprogramm, erstellt. Der Mikrocontroller steuert seine Ausgänge je nach Programmierung in Beziehung zu seinen Eingängen. Somit ist es für uns Möglich unsere automatisierte Glühbrine zu betreiben. Alle Messwerte, welche durch die Photodioden eingehen, gibt der Arduino durch den Seriellen Monitor an. Außerdem liest er sie ab und aufgrund unseren Codes führt er dann die programmierten Anweisungen aus. Diese gibt der PC wieder an das Arduino-Board, welches die Stromstärken dann an die bestimmten Stellen weiterleitet.   </li>

<li>Des Weiteren haben wir Photodioden genutzt, weil wir die Lichtintensität im vorliegendem Karton messen müssen, um die Glühlampe zu regulieren. Die Photodiode ist die klassische Messung, welche man in Verbindung mit einem Arduino nutzt. Die Photodiode dient wie ein Wiederstand. Denn wenn es Hell ist, führt der innere Photoeffekt zu einer Spannung.  Dann wird der Strom an den Arduino weitergeleitet, wo er mit der Software in einen Wert umgerechnet wird (im Video zu sehen). Wenn es Hell ist, wird also ein höherer Wert angezeigt, weil mehr Strom fließt und ein gegenteiliger Effekt entsteht bei wenig Licht. Wir haben zwei Photoioden genutzt, welche an verschiedenen Stellen des Steckbretts angebracht sind, damit die durchschnittliche Helligkeit im Raum ermittelt werden kann.   </li>

	
<li>Außerdem haben wir einen Transistor verwendet. Dieser war auch im Inventar der Stormarnschule vorzufinden und dieser nimmt eine ganz wichtige Funktion in unserem Aufbau ein. Denn der Transistor ist dafür zustandig, dass wir die Helligkeit der Glühlampe steuern können. Durch den Transistor, der wie ein Verstärker vom Strom wirkt, können wir die 6V Glühlampe mit dem Ardiono, der nur höchstens 5V ausgeben kann, steuern. Zu beginn haben wir dies, wie man sehen kann, mit einem externen Netzteil gemacht, um genügend Spannung in den Stromkreis zu bringen und erst die Möglichkeit zu haben die Glühlampe zu betreiben. ALs Nächstes kommt der Transistor ins Spiel. Dieser sorgt dafür, dass der Strom für die Glühlampe verstärkt wird, wenn es dunkler wird. Denn ein Transistor ist aus einem Emitter, einem Kollektor und der Basis aufgebaut. Durch Kollektor und Emitter fließt Strom abhängig davo, wie viel Strom durch die Basis fließt. Dabei wirkt die Basis als Schalter und Verstärker. Die Basis wird bei unserem Aufbau vom 10. Pin vom Arduino gesteuert und je nachdem, wie viel Strom dort, abhängig von der Lichtintensität durchgegeben wird, kann Strom durch den Kollektor und den Emitter fließen. Dadurch bekommt unsere Glühbrine dann abhängig von der Basis Strom zugeführt und leuchtet oder leuchtet nicht.    </li>
	
 	
	
	

 
<h3> 2.5 Das Endprodukt </h3>
Youtube Link: https://youtu.be/EAZcYoLfER0

<h1>3. Fazit</h1> <a name="Fazit"></a>
 

Wir ziehen ein sehr positives Fazit, weil wir beide viel Spaß am Projekt hatten. Durch das beidseitige Interesse gab es auch immer eine sehr produktive Zusammenarbeit.
Mit dem Endprodukt sind beide sehr zufrieden. 
Zu Beginn war es eine sehr effektive gemeinsame Planung, welche wir dann mit der Zeit gut umsetzen konnten.
Aufgrund unserer guten Arbeit waren wir früher mit der Umsetzung der grundlegenden Idee fertig und konnten unser Projekt auf Rat von Herrn Buhl noch durch eine Glühlampe verbessern und mehr Kenntnisse für das nächste Projekt sammeln.
Insgesamt haben wir nun grundsätzliche Kenntnisse im Bereich des Arduinos erlernt und hoffen basierend auf diesem Wissen ein deutlich komplexeres nächstes Projekt zu erarbeiten. Wir haben uns auch einige Male am Wochenende zusammengesetzt und am Projekt weitergearbeitet, wodurch wir schnell unsere Ziele erreicht haben und recht viel Zeit hatten, um unsere Erfahrungen zu verschriftlichen. Auch wenn es manchmal längere Phasen ohne Erfolg gab überwog die Freude über das Lösen dieses Problems dann umso mehr, wenn ein Problem gelöst wurde, welche sich über mehrere Stunden hinweg gezogen hatte. Wir haben uns entschieden auch im 2. Halbjahr wieder zusammenarbeiten. 
	
<h3> 3.1 Nutzung im Alltag </h3>

Wir haben uns ein Physical-Computing-Projekt ausgesucht, weil uns, wie schon gesagt, der Bezug zur Realität interessiert. 
Somit haben wir uns auch während der Projektentwicklung immer wieder überlegt, wofür man das Projekt im Alltag nutzen könnte.
Als erste Möglichkeit ist es ganz normal das Licht im Haus oder vor dem Haus somit zu regeln.
Dies würde dazu führen, dass das Licht nicht unnötig bei Helligkeit an ist, oder es halb dunkel ist. 
Wenn man den Strom direkt aus der Stromquelle schon steuert, ist dies auch deutlich umweltfreundlicher, da man nicht immer den ganzen Strom braucht.
Dies würde auch für einen selber zu einem Ersparnis werden, weil man weniger Strom bezahlt. 
Das gleiche gilt für Laternen in der Stadt. 
Auch im Auto könnte man dies einbauen, weil somit das Unfallrisiko gemindert wird, weil das Licht automatisch gesteuert wird und somit nicht vergessen wird anzumachen. 
Des Weiteren blendet es den entgegenkommenden und vor einem fahrenden Verkehr nicht, weil das Licht von dort such wahrgenommen wird und das eigene somit geschwächt wird.
Also kann man diese "Erfindung" in vielen und auch wichtigen Bereichen des Alltags nutzen. Es dient nicht nur dem Aussehen, wie am Haus, sondern auch der Sicherheit, wie im Auto.

<h3> 3.2 Ausblick </h3>

Für die Zukunft haben wir uns überlegt, dass wir weiter mit dem Arduino arbeiten wollen, weil wir jetzt schon ein gutes Grundwissen dazu haben. 
Wir wollen aber nicht mehr mit der Helligkeit, sondern möglichst mit Wärme arbeiten. 
Wir haben uns schonmal überlegt, dass wir durch eine Glühlampe, welche nicht nur Licht sondern auch Wärme abgibt, die Temperatur im Raum steuern beziehungsweise auf einen bestimmten Wert konstant halten wollen. Also messen wir diesmal die Temperatur, statt die Helligkeit, um auch noch etwas neues zu dem bereits bekannten zu lernen. Auch hier ist die Gefahr von Rückkopplungen groß- und genau das ist also hier die Herausforderung, der wir uns stellen wollen. Dabei können wir nun PID verwenden, worauf wir in unserer ersten Arbeitsphase gestoßen sind. Wir freuen uns schon sehr auf dieses Projekt und die einhergenden Probleme, die wir hoffentlich nochmals lösen können!

