# Informatikprojekt: X

### Stundenprotokolle<a name="einf"></a>
16.8 
   
 In unserer ersten informatikstunde hat herr buhl uns unsere projektaufgabe erklärt, und github gezeigt. 
 Dazu haben wir noch einige projekte von ehemaligen Schülern gesehen.Diese gingen in verschiedene richtungen und wir konnten uns auf github einen ersten überblick über 
 unsere optionen verschaffen. 

17.8

In den heutigen Informatikstunden haben wir uns nochmal näher mit den früheren Projekten beschäftigt. 
Wir haben uns die verschiedenen Möglichkeiten alle ausführlich angeguckt und haben entschieden, dass wir etwas in Richtung Physical Computing machen wollen. 
Außerdem haben wir uns mit den verschiedenen Arduinos beschäftigt und überlegen uns nun welches Projekt genau wir machen wollen. 
Es gibt schon erste Ideen wie, dass man wenn ein Mensch im Raum ist die Lichthelligkeit kostant hält.
Die Helligkeit im raum soll gemessen werden und dann wird die Helligkeit einer Lampe gesteuert, sodass es im Raum immer gleich hell ist.
Bei dieser Idee wird die Anweisung durch Bewegungs und Lichtsensoren gesteuert.

23.08

Heute haben wir uns final entschieden das in der vorherigen Stunde geplante Projekt umzusetzten. Außerdem haben wir nach den benötigten Materialien recherchiert und 
haben uns diese rausgesucht. Für den Arduino haben wir uns auf der Webiste zu den verschiednen Modellen informiert und haben uns entschlossen einen Arduinio mit
Internet verbindung zu verwenden. Zudem haben wir uns vorerst Lichtsensoren rausgesucht und haben wir uns für eine LED Lampe, bei welcher man die Lichtintensität
abhängig von der Stromstärke dimmen kann, entschieden.

24.08

In der heutigen doppelstunde haben wir das erste Mal mit dem arduino experimentiert. wir haben zuerst eine LED zum blinken gebracht. Dies hat sofort geklappt. Als wir dies geschafft haben hatten wir die Aufgabe einen Schalter mit einzubauen. Bei dieser Aufgabe gab es deutlich mehr schwierigkeiten als bei der ersten Aufgabe. Am Ende haben wir auch dies geschafft. Wie man im Bild sieht, ist der Aufbau etwas komplizierter als bei der ersten Aufgabe. Durch diese Experimente haben wir erste Schritte mit dem Arduino gelernt und außerdem, wie man in der Arduino-App programmiert.

30.08

In der heutigen Stunde haben wir zuerst nach einem passendem weissen LED Strip recherchiert. Wir haben versucht einen 5V Strip zu finden, da wir dann keinen Mosfar benutzen müssten. Dananch haben wir wieder experimentiert und versucht mit einem fotosensor Licht zu messen und dies erflogreicht geschafft. Wir haben nämlich den Fotosensor an den Arduino angeschlossen. Dann wurden diese an den Computer weitergegeben, bei welchem wir sie durch den "serielle Monitor" ablesen konnten. Dann haben wir noch gesteuert, wie oft die Werte gem,essen werden sollen, da sie sonst dauerhaft gemessen wwerden und dies bei unserem Projekt sehr wahrscheinlich zu Rückkopplungen führen würde.

31.08

Zuerst haben wir den Aufbau aus der gestrigen Stunde wiederholt und dann haben wir uns weiter informiert und wollten dann den erflogreich verbundenen fotosensor mit einer LED verbinden. Unser Ziel war es, dass die LED leuchtet wenn der Fotosensor ein niedrigen Wert misst, also wenn es dunkler wird, und entsprechend bei einem hohen wert, also wenn es heller wird, aus geht. Also wird die Halligkeit der LED durch die Messwerte des Fotosensors gesteuert. Dies haben wir letztendlich auch geschafft. Zuerst haben wir dies mit einem "if" geschafft. Das heißt, wenn die Helligkeit, welche der Fotosensor unterschreitet, geht die LED an. Dann haben wir uns über Arduino Map informiert und haben durch dies die Helligkeit gesteuert. Die Helligkeitswerte haben wir also in AnalogWrite werte übersetzt und "gemapt". Dadurch gab der Arduino dann eine bestimmte Voltzahl aus und die LED leuchtet verschieden Hell. 
Video einfügen
