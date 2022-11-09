# Informatikprojekt: X

### Stundenprotokolle<a name="einf"></a>



[Stundenprotokolle](#einf)  
[Stunde vom 16.8](#1)  
[Stunde vom 17.8](#2)  
[Stunde vom 23.8](#3)
[Stunde vom 24.8](#4)
[Stunde vom 30.8](#5)




### <a name="1"></a>Stunde vom 16.8
   
 In unserer ersten informatikstunde hat herr buhl uns unsere projektaufgabe erklärt, und github gezeigt. 
 Dazu haben wir noch einige projekte von ehemaligen Schülern gesehen.Diese gingen in verschiedene richtungen und wir konnten uns auf github einen ersten überblick über 
 unsere optionen verschaffen. 

### <a name="2"></a>Stunde vom 17.8

In den heutigen Informatikstunden haben wir uns nochmal näher mit den früheren Projekten beschäftigt. 
Wir haben uns die verschiedenen Möglichkeiten alle ausführlich angeguckt und haben entschieden, dass wir etwas in Richtung Physical Computing machen wollen. 
Außerdem haben wir uns mit den verschiedenen Arduinos beschäftigt und überlegen uns nun welches Projekt genau wir machen wollen. 
Es gibt schon erste Ideen wie, dass man wenn ein Mensch im Raum ist die Lichthelligkeit kostant hält.
Die Helligkeit im raum soll gemessen werden und dann wird die Helligkeit einer Lampe gesteuert, sodass es im Raum immer gleich hell ist.
Bei dieser Idee wird die Anweisung durch Bewegungs und Lichtsensoren gesteuert.

### <a name="3"></a>Stunde vom 23.8

Heute haben wir uns final entschieden das in der vorherigen Stunde geplante Projekt umzusetzten. Außerdem haben wir nach den benötigten Materialien recherchiert und 
haben uns diese rausgesucht. Für den Arduino haben wir uns auf der Webiste zu den verschiednen Modellen informiert und haben uns entschlossen einen Arduinio mit
Internet verbindung zu verwenden. Zudem haben wir uns vorerst Lichtsensoren rausgesucht und haben wir uns für eine LED Lampe, bei welcher man die Lichtintensität
abhängig von der Stromstärke dimmen kann, entschieden.


### <a name="4"></a>Stunde vom 24.8

In der heutigen doppelstunde haben wir das erste Mal mit dem arduino experimentiert. wir haben zuerst eine LED zum blinken gebracht. Dies hat sofort geklappt. Als wir dies geschafft haben hatten wir die Aufgabe einen Schalter mit einzubauen. Bei dieser Aufgabe gab es deutlich mehr schwierigkeiten als bei der ersten Aufgabe. Am Ende haben wir auch dies geschafft. Wie man im Bild sieht, ist der Aufbau etwas komplizierter als bei der ersten Aufgabe. Durch diese Experimente haben wir erste Schritte mit dem Arduino gelernt und außerdem, wie man in der Arduino-App programmiert.

### <a name="5"></a>Stunde vom 30.8

In der heutigen Stunde haben wir zuerst nach einem passendem weissen LED Strip recherchiert. Wir haben versucht einen 5V Strip zu finden, da wir dann keinen Mosfar benutzen müssten. Dananch haben wir wieder experimentiert und versucht mit einem fotosensor Licht zu messen und dies erflogreicht geschafft. Wir haben nämlich den Fotosensor an den Arduino angeschlossen. Dann wurden diese an den Computer weitergegeben, bei welchem wir sie durch den "serielle Monitor" ablesen konnten. Dann haben wir noch gesteuert, wie oft die Werte gem,essen werden sollen, da sie sonst dauerhaft gemessen wwerden und dies bei unserem Projekt sehr wahrscheinlich zu Rückkopplungen führen würde.

31.08

Zuerst haben wir den Aufbau aus der gestrigen Stunde wiederholt und dann haben wir uns weiter informiert und wollten dann den erflogreich verbundenen fotosensor mit einer LED verbinden. Unser Ziel war es, dass die LED leuchtet wenn der Fotosensor ein niedrigen Wert misst, also wenn es dunkler wird, und entsprechend bei einem hohen wert, also wenn es heller wird, aus geht. Also wird die Halligkeit der LED durch die Messwerte des Fotosensors gesteuert. Dies haben wir letztendlich auch geschafft. Zuerst haben wir dies mit einem "if" geschafft. Das heißt, wenn die Helligkeit, welche der Fotosensor unterschreitet, geht die LED an. Dann haben wir uns über Arduino Map informiert und haben durch dies die Helligkeit gesteuert. Die Helligkeitswerte haben wir also in AnalogWrite werte übersetzt und "gemapt". Dadurch gab der Arduino dann eine bestimmte Voltzahl aus und die LED leuchtet verschieden Hell. 
Video einfügen

06.09

Heute haben wir den aufbau letzer Woche wieder aufgebaut und haben uns weitere Funktionen auf der Arduino website über den Arduino durchgelesen, damit wir es schaffen einen richtwert zu definieren, bei dem ein Lichtwert erreicht wird und somit keine veränderung der LED mehr stattfindet. Dazu haben wir weitere Planungen übernommen, wie wir benötigtes Material organisieren.
07.09

In dieser Doppelstunde haben wir einige funktionen versucht, doch leider hat es noch nicht geklappt, Wir haben unter anderem die == Funktion sowie die define() funktion. Des Weiteren haben wir nun andere Funktionen rausgesucht, die wir in der nächtsen Strunde probieren wrrden. Außerdem haben wir überlegt, wie wir die Schwankungen in der Helligkeit verringern können. Dadurch waren wir wieder auf der Seite des arduinos. DOrt haben wir 2 sachen probiert. Diese haben aber leidder noch nicht gelklappt

13.09

In dieser Stunde haben wir den Aubau mit dem Photosensor und der LED nochmals aufgebaut und anschliessend haben wir uns überlegt, dass man mit einer (if) funktion eine Helligkeit erhalten könnte, dass die Led durch die Messungen keine so großen Schwankungen hat. Aktuell passiert es nämlich, dass es ganz dunkel ist und dann die LED genz hell wird. dadurch ist es dann zu hell und die LED wird wieder dunkler. Mit der if Funktion ist unser Ziel, dass der Strom, welcher zu der LED fließt nur ein bisschen in jeder Messung verändert wird. Wenn dies oft passiert ist die LED auch nach einer kurzen Zeit angepasst. Dies werden wir in der morgigen Doppelstunde programmieren und ausprobiere.

14.09
Heute haben wir den ganzen Aufbau in den Schuhkarton gebaut, welches später unser "Zimmer" sein soll. Durch diese Umsetzung kann unser Aufbau jetzt erhalten werden und wir müssen nicht jede Stunde wiederholen, was uns immer 5- 10 Minuten kostete.

https://forum.arduino.cc/t/mehrere-lmp36-temperatursensoren-mittelwert-bilden-ethernetshield/180756

27.09.22
recherchiert wie man MIttelwert bei Arduino bildet , array funktion und millis funktiuon, 
In der heutigen Informatikstunfe haben wir weiter versucht herauszufinden, wie man einen Mittelwert bildet. Dies haben wir zuerst mit der Array- Funktion und dananch mit der Millis-Funktion produziert

28.09.2022
weiter reherchiert, mittelwert problem durch adition gelöst, maximum definiert ( if funktion) also ehm zu hell bedeutet LED aus 

26.10.2022
fehler behoben, mit herr buhl, felher beim kompillieren ,    alten aufbau aufgebaut,     Versuch aufbau glühlampe, recherche, selbst versuicht aufzubaue ( nicht geglückt) pro0nhlenm: aus Arduino nur 5 volt, glühlampe braucht 6 volt. Mithilfe externen Netzteil und Transistor ptroblem umgehen. 

1.11 
ausgefallen

2.11 Glühlampe eingebaut
8,11
Problem ösung map geht nicht, leuchten mit photodioden rechercvhe
