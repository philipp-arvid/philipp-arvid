Blog Nr.2 


10.01.2023 
Zuerst gab es heute die Noten für unser letztes Projekt. Dazu gab es noch einige Rückmeldungen und uns wurde etwas zum neuen Projekt und den Möglichkeiten erzählt. Wir haben uns aufgrund des Erfolgreichen Projekts des letzten Halbjahres entschlossen weiterhin zusammenzuarbeiten. Die Grundidee des neue Projekts haben wir uns schon im letzten Halbjahr überlegt. Heute haben wir dann die Projektseite und den Blog für unser Projekt erstellt. Wir haben uns noch genauer überlegt wie wir das Projekt umsetzten wollen.

11.01.2023 
Heute haben wir uns überlegt, welche Teile wir für unser projekt benötigen und fragen welche von denen schon in der schule vorzufinden sind, und welche wir uns selber beschaffen werden. Anschließend haben wir den Schuhkarton mit Aluminiumfolie ausgekleidet und uns danach schonmal einige videos und Websiten angeguckt, um schnmal einige Informationen zu sammlen wie genau wir unser projekt relisieren können. Außerdem haben wir uns über den Wärmesensor besonders informiert und überlgen uns nun , wie wir den Ntc Therministor kalibirieren können. Dafür haben wir auch schon einen generellen Aufbau, wie man den Ntc Therministor steuert. Diesen wollen wir dann nächste Woche kalibrieren.

17.01.2023

Heute haben wir die ersten Materialien zusammen getragen. Nun haben wir eine 25 Watt Glühbirne und müssen uns jetzt überlegen, wie oder welchen Transistor wir brauchen um Strom aus der Steckdose steuern zu können. Als nächstes müssen wir uns auch übelergen, wie wir unseren Wärmesensor kalibrieren. Doch dies ist nicht ganz einfach, da der Npc Wärmesensor nicht linear funktioniert. 


18.01.2023

Heute haben wir einen ersten Schritt geschafft. Wir haben es geschafft, auch nach Problemen den Wiedertstand des NTCs auszulesen. Als nächstes müssen wir den NTC Wiederstan in eine Temperatur umrechnen.  https://forum.arduino.cc/t/ol-temperatur-messen-welcher-oltemperaturgeber-kfz/152055/12#msg1170722
https://www.mymakerstuff.de/2018/05/18/arduino-tutorial-der-temperatursensor/

24.01.2023
heute haben wir weiter recherchiert, wie man einen Ntc Wiedersandswert in Temperarur umrechnet. Da haben wir eine wuelle schon gefunden, doch leider hat das noch nicht geklappt- hier ist der code damit wir nicht immer ein halbe stunde wieder auf dem Stand von der stunde davor kommen müssen LOOOOLLLL.
int sensorPin = A0;
int bitwertNTC = 0;
long widerstand1=1000;                   //Ohm
int bWert =3950;                           // B- Wert vom NTC
double widerstandNTC =0;
double kelvintemp = 273.15;                // 0°Celsius in Kelvin
double Tn=kelvintemp + 25;                 //Nenntemperatur in Kelvin
double TKelvin = 0;                        //Die errechnete Isttemperatur
double T = 0;                              //Die errechnete Isttemperatur

void setup() {

  Serial.begin(9600);
}

void loop() {
     
  Serial.println("Sensormessung:  ");
  bitwertNTC = analogRead(sensorPin);      // lese Analogwert an A0 aus
  widerstandNTC = widerstand1*(((double)bitwertNTC/1024)/(1-((double)bitwertNTC/1024)));

                                           // berechne den Widerstandswert vom NTC
  TKelvin = 1/((1/Tn)+((double)1/bWert)*log((double)widerstandNTC/widerstand1));
                                           // ermittle die Temperatur in Kelvin
  T=TKelvin-kelvintemp;                    // ermittle die Temperatur in °C

  Serial.println("Analog: ");              //
  Serial.println(bitwertNTC);              //
  Serial.println("NTC- Widerstand: ");     //Gebe die ermittelten Werte aus

  Serial.println(widerstandNTC);           //
  Serial.println("Temperatur: ");          //Gebe die ermittelten Werte aus
  Serial.println(T);                       //
 
delay(1000);                               // Warte eine Sekunde und mache alles nochmal
  
}

25.01.2023

heute wasserkocher, weiter probiert, mehrere websites, herr buhl hat nicht geklappt, B wert ist abhänging von der dfunktion , neuer Thermistor mit board für nächste woche, auch selbser probiert mit float

8.3
Ventilator

