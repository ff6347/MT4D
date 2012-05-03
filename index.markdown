---
layout: default
title: Mehr Zeit für Gestaltung
---
#Bachelor Arbeit von Fabian Morón Zirfas
#Mehr Zeit für Gestaltung
<!-- <br /> <a href="images/connectedNodes.jpg"><img src="images/connectedNodes.jpg" width="100%" alt="" /></a>
 -->
<br>
#####Inhalt  
<br>
<div id="index">

<h2><a href="#01">1 Einleitung</a></h2>
<h3><a href="#02">&emsp;1.1 Bevor sie Einsteigen</a></h3>
<br>
<div><h2><a href="#03">2 Wann soll ich Scripten?</a></h2>
<ul>
<li><a href="#37">&emsp;&emsp;2.0.1 Welche Operationen sollen ausgeführt werden?</a></li>
<li><a href="#38">&emsp;&emsp;2.0.2 Wie komplex sind die Operationen?</a></li>
<li><a href="#39">&emsp;&emsp;2.0.3 Wie ist das Zeitfenster und wann muss das Produkt fertig sein?</a></li>
<li><a href="#40">&emsp;&emsp;2.0.4 Wie oft muss diese Tätigkeit ausgeführt werden?</a></li>
<li><a href="#41">&emsp;&emsp;2.0.5 Lässt sich die Automation auch auf andere ähnliche Bereiche anwenden oder mit geringen Aufwand abstrahieren?</a> </li>
<li><a href="#42">&emsp;&emsp;2.0.6 Wie sehr ist sie von Umgebungsvariablen abhängig?</a></li>
<li><a href="#43">&emsp;&emsp;2.0.7 Soll die Automation von dritten Benutzt werden?</a></li>
<li><a href="#44">&emsp;&emsp;2.0.8 Ist der Prozess linear oder bedarf es einer Rückkopplung zum Benutzer?</a></li>
</ul>
<h3><a href="#04">&emsp;2.1 Das Beispiel targetengine</a></h3>
<ul><li><a href="#45">&emsp;&emsp;2.1.1 Existieren bereits Automationen in dem Sektor und wenn ja lassen sich diese abwandeln?</a></li>
<li><a href="#46">&emsp;&emsp;2.1.2 Bietet die API direkten Zugriff auf die benötigten Funktionen oder braucht es eine Workaround?</a></li>
</ul>
<h3><a href="#05">&emsp;2.2 Das Beispiel try char</a></h3></div>
<br>
<h2><a href="#07">3 Szenarien</a></h2>
<h3><a href="#08">&emsp;3.1 Der Einsatz - das Beispiel image matrix</a></h3>
<h4><a href="#33">&emsp;&emsp;3.1.1 Ergebnisse - image matrix</a></h4>
<h3><a href="#09">&emsp;3.2 image matrix - Schritt für Schritt.</a></h3>
<h3><a href="#10">&emsp;3.3 Das Beispiel great power</a></h3>

<br>
<h2><a href="#12">4 Ein Werkzeug - AEMap</a></h2>
<br>
<h2><a href="#11">5 Die Angst</a></h2>
<br>
<h2><a href="#06">6 Fazit </a></h2>
<br>
<h2><a href="#13">7 Die kleine Terminologie</a></h2>
<ul>
<li><a href="#14">&emsp;7.01 Was ist Code?</a></li>
<li><a href="#15">&emsp;7.02 Was ist ein Programm?</a></li>
<li><a href="#16">&emsp;7.03 Was ist ein Algorithmus?</a></li>
<li><a href="#17">&emsp;7.04 Was ist die Syntax?</a></li>
<li><a href="#18">&emsp;7.05 Was ist Pseudocode?</a></li>
<li><a href="#19">&emsp;7.06 Was ist ein Compiler?</a></li>
<li><a href="#20">&emsp;7.07 Was ist eine IDE (Integrated Development Envoirement)?</a></li>
<li><a href="#21">&emsp;7.08 Was ist Hello World?</a> </li>
<li><a href="#22">&emsp;7.09 Was ist Syntax-Highlighting?</a></li>
<li><a href="#23">&emsp;7.10 Was ist eine API (Application Programming Interface)?</a></li>
<li><a href="#24">&emsp;7.11 Was ist Objektorientierung?</a></li>
<li><a href="#25">&emsp;7.12 Was sind Funktionen/Methoden</a>?</li>
<li><a href="#26">&emsp;7.13 Was ist ein Bug?</a></li>
<li><a href="#27">&emsp;7.14 Was ist Debugging?</a></li>
<li><a href="#28">&emsp;7.15 Was ist ein Workaround?</a>  </li>
<li><a href="#29">&emsp;7.16 Welche Konventionen gibt es?</a></li>
<li><a href="#30">&emsp;7.17 Herkunft von JavaScript</a></li>
<li><a href="#31">&emsp;7.18 Was ist der Unterschied zwischen JavaScript und ExtendScript?</a></li>
<li><a href="#32">&emsp;7.19 Was sind Pointer</a></li>
</ul><br>
<h2><a href="#34">8 Refenrenzen</a></h2>
<br>
<h2><a href="#35">9 Weblinks</a></h2>
<br>
<h2><a href="#36">10 Quellen</a></h2>
</div>
<br>  

-------------
  
<br>
##<span id="overlay"><a href="#02" title="Next" >&darr;</a></span><a id="01"></a>1 Einleitung <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Diese Arbeit setzt sich mit der Automation von Design-Prozessen auseinander. Sie ist an Designer gerichtet die einen rohen Überblick bekommen wollen wie Arbeitsprozesse automatisiert werden können und soll als Hilfestellung dienen einen Einstieg in das Schreiben von Skripten für Grafikanwendungen. Sie ist keine komplette Anleitung zum Erlernen von Programmier Grundkenntnissen, diese können für viele verschieden Sprachen im "World Wide Web" gefunden werden, sondern eine Auseinandersetzung was Automation durch Programmierung für Designer leisten kann und welche Bereiche sie nicht abdeckt. Im ersten Abschnitt soll dem Leser kurz erläutert werden was er benötigt um zu Skripten um dann im zweiten Teil zu analysieren wann dies sich lohnt. Hier wird an einem kurzen Beispielen erläutert wo Probleme auftreten können und an einem weiteren wie solche Problem klug umschifft werden können. Im dritten Teil folgt ein Szenario an dem Schritt für Schritt die Logik und Funktionsweise eines Skriptes erklärt wird und ein weiteres Szenario mit einer einzeiligen und doch nützlichen Lösung. Der vierte Teil behandelt  eine wirkliche Anwendung. Anhand dieser wird das Ausmaß das dies annehmen kann gezeigt. Es folgt im fünften Teil ein Auseinandersetzung mit der Frage woher die Abwehrhaltung gegen Computersprachen herrühren kann. Im sechsten Teil, dem Fazit, wird der Erkenntniszuwachs aus all dem zusammengefasst. Es folgt noch eine weiterer Abschitt mit Erläuterungen zur Teilweise verwendeten Terminologie. Dieser Abschnitt sollte jedoch nicht linear gelesen werden sondern als Referenz dienen. Zum Abschluss stehen die Referenzen, Weblinks und Quellenverweise.  
<br>
###<span id="overlay"><a href="#03" title="Next" >&darr;</a></span><a id="02"></a>1.1 Bevor sie Einsteigen <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Bevor sie weiterlesen einige Hinweise. Wenn sie noch keine Erfahrungen mit Programmierung gemacht haben lassen sie sich nicht abschrecken. Es werden einige für den Laien unverständliche Zeilen vorkommen und einige die sich aus dem Kontext oder den Namen der <a href="#25">Funktionen</a> erschliessen lassen. Falls sie die Beispiele in Abschnitt Eins und Zwei ausprobieren möchten lesen sie den Abschnitt <a href="#21">7.08 Was ist Hello World?</a> zuerst. Dort wird erklärt wie und wo sie Skripte schreiben und ausführen können. Es werden Fachausdrücke vorkommen die ebenfalls im Abschnitt <a href="#13">7 Die kleine Terminologie </a>erklärt werden. Ab dem Abschnitt <a href="#07">3 Szenarien</a> steigen wir dann voll in das Lesen und wenn sie möchten Schreiben von Skripten ein. Dafür sollte zumindest der eben genannte Abschnitt "Was ist Hello World?" einmal nachvollzogen worden sein. Wenn die dort dargestellten Zusammenhänge und Konstrukte zu komplex sind verschaffen sie sich etwas Übung. Es existiert eine schöne Webseite genannt [codecademy.com](http://www.codecademy.com/#!/exercises/0) auf der sie in einigen lustigen Aufgaben durch die Grundlagen von JavaScript geführt werden. Wenn mal etwas nicht funktioniert - verzweifeln sie nicht. Kontrollieren sie ihre Schreibweise und suchen sie sich weiterführende Informationen im Netz. Die einfachste Möglichkeit ist den gewünschten Befehl samt JavaScript <a href="http://lmgtfy.com/?q=alert()+JavaScript">(z.B. "alert() JavaScript")</a> in einer Suchmaschine einzugeben. Da das Netz voll von JavaScript ist spuckt es in 99% der Fälle auch die richtige Dokumentation aus. Werfen sie ebenfalls einen Blick in die Referenz-Liste. Dort finden sie viele Ressourcen für "Scripting" die ihnen den Einstig erleichtern werden.  
Um in diesem html Dokument zu manövrieren können sie entweder normal scrollen oder sie benutzen die &darr; &uarr; Pfeile. Der &darr; bringt sie zum nächsten Abschnitt. der &uarr; bringt sie wieder zurück zum Index. Sie werden ebenfalls kleine [?] am Ende eines Absatzes finden. Drücken sie auf diese drauf - sie enthalten Zusatzinformationen und Querverwiese.<a href="#" class="show_hide" rel="#slidingDiv0">[?]</a><div id="slidingDiv0">Herzlichen Glückwunsch. Sie haben eine Zusatzinformation gefunden. drücken sie auf das [x] um diese Kiste wieder zu schliessen.</div>   


##<span id="overlay"><a href="#04" title="Next" >&darr;</a></span><a id="03"></a>2 Wann soll ich Skripten? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

> Scripting languages assume that there already exists a collection of useful components written in other languages. Scripting languages aren't intended for writing applications from scratch; they are intended primarily for plugging together components  
> Scripting: Higher Level Programming
for the 21st Century by John K. Ousterhout ([online](http://www.tcl.tk/doc/scripting.html))

Auch wenn Aufgaben auf unterschiedliche Weise mit verschiedenen Programmiersprachen gelöst werden können haben sich spezielle Anwendungsgebiete für die einzelnen Sprachen ergeben. Ganz unabhängig davon, dass sich in unserem Fall Adobe Anwendungen mit JavaScript ansprechen lassen macht es Sinn eine Skriptsprache zu verwenden um die bereits in höheren Sprachen implementierten Funktionen zu verbinden. JavaScript ist unser Kleber. Wir müssen das Rad nicht neu erfinden. Wir können jedoch unseren Arbeitsablauf durch gezielte Befehlsketten von repetitive Aufgaben befreien. Ich bin mir sicher dass ein Grossteil aller Gestalter die vorgefertigte Software für ihre Arbeit verwenden schon einmal an den Punkt kamen wo sie sich dachten: "Warum kann mein Programm DAS nicht", "es ist doch alles da. Der Knopf und danach diesen Knopf!".<a href="#" class="show_hide" rel="#slidingDiv1">[?]</a><div id="slidingDiv1">DAS steht hier für eine gewünschte Funktionsweise</div>  
Scripting erlaubt es uns diese beiden Knöpfe mit einander zu verbinden. Das bedeutet dann, dass wir unsere Arbeit um einen "Klick" reduziert haben. Wir haben zwei Knöpfe durch Verkettung auf einen neuen Knopf gelegt. Natürlich klingt die Reduktion um einen Klick vernachlässigbar. Wenn Jedoch diese zwei Klicks 100 mal ausgeführt werden müssen und wir durch logische Anweisung diese ebenfalls auf nur einen Knopf zusammenführen können ist der Zeitgewinn enorm. Ebenfalls muss hier erwähnt werden das viele der Probleme die in einem Gestaltungs-Prozess auftreten nicht zum ersten mal bei eben dieser Person auftreten. Für den Bereich Scripting von Adobe Anwendungen gibt es im Netz viele Seiten und Foren die sich mit diesem Thema befassen. Im Bereich JavaScript gibt es noch viele mehr, da JavaScript auch verwendet wird beziehungsweise entwickelt wurde um Browser zu steuern. Aufgrund dessen ist die Dokumentation mehr als ausgiebig. Es Bedarf nur etwas Übung um die gefundenen Beispiele zu lesen und auf die eigene Problemstellung zu abstrahieren.  

    
#Hierbei sei zu beachten! 
Scripting kann keine Design Entscheidungen fällen. Es existiert kein Algorithmus der Ästhetik simuliert.<a href="#" class="show_hide" rel="#slidingDiv2">[?]</a><div id="slidingDiv2"> Ein Algorithmus ist ein logische Verkettung von Operationen siehe Abschnitt <a href="#16">7.03 Was ist ein Algorithmus?</a></div>  Um eine spannende Komposition zu schaffen braucht der Gestalter "nur" drei geometrische Grundformen zu erzeugen und diese im richtigen Verhältnis zu einander anzuordnen. Um dies programmatisch zu lösen müsste ein Skript mehrere hundert mal ausgeführt werden. Jedes mal mit einer kleinen Veränderung der Koordinaten der obig genannten drei Objekte. Davon mal ganz abgesehen, dass der Autor irgendwann entscheiden muss welche Komposition knackig ist. Was das Skript leisten kann ist anhand von bestimmten Rahmenparametern eine Fülle von Varianten zu liefern die von Hand Sehnenscheidenentzündungen hervorrufen würde.
Programmieren ist nicht einfach. Es ist wie eine neue Sprache lernen. Stellen sie sich vor sie sind in einem fremden Land dessen Sprache sie nicht beherrschen. Sie werden zuerst Probleme haben. Dann lernen sie ihre Grundbedürfnisse zu decken. Ab einem gewissen Punkt können sie Tageszeitungen lesen und Inhalte erfassen und abstrahieren. Eines Tages werden sie feststellen, dass sie in der Sprache Träumen. Der Vorteil an Computersprachen im Vergleich zu "Menschensprachen" ist das in der Computersprache kein Raum für Interpretation ist. Jede Aussage MUSS eindeutig sein. In der Kommunikation mit Menschen MUSS interpretiert werden. In Schriftform ist auch kein Raum für Interpretation. Die <a href="#17">Syntax</a> muss valide sein. Dies ist ein Vorteil. Es zwingt zu Genauigkeit. Dennoch - eine Sprache lernen ist keine leichte Aufgabe.  
Daher sollten sie bevor sie in die Tiefen von JavaScript abtauchen um ein Problem zu lösen entscheiden:  
  
- Welche Operationen sollen ausgeführt werden?
- Wie komplex sind die Operationen?
- Wie ist das Zeitfenster und wann muss das Produkt fertig sein?
- Wie oft muss diese Tätigkeit ausgeführt werden?
- Lässt sich die Automation auch auf andere ähnliche Bereiche anwenden oder mit geringen Aufwand abstrahieren?
- Wie sehr ist sie von Umgebungsvariablen abhängig?
- Soll die Automation von dritten Benutzt werden?
- Ist der Prozess linear oder bedarf es einer Rückkopplung zum Benutzer?

Und einige Punkte die sich hauptsächlich durch Recherche abarbeiten lassen  

- Existieren bereits Automationen in dem Sektor und wenn ja lassen sich diese abwandeln?
- Bietet die <a href="#23">API</a> direkten Zugriff auf die benötigten Funktionen oder braucht es eine <a href="#28">Workaround</a>? 

Diese Analyse kann keine genauen Angaben über Zeit und Aufwand machen da dies immer auch vom Erfindungsreichtum des Autors abhängig ist. Der Kreative kommt hier schneller zum Ziel.

- <span id="overlay"><a href="#38" title="Next" >&darr;</a>Welche Operationen sollen ausgeführt werden?</span><a id="37"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Programme oder Skripte schreiben ist nicht wie "Scribbeln". Wir können beim Telefonieren eine Stift in die Hand nehmen und drauf los kritzeln. Beim Programmieren muss das Ergebnis bereits definiert sein bevor geschrieben wird. Natürlich ergeben sich auch während des Schreibens neue Ideen, dennoch muss eine konkreten Vorstellung existieren was das Ziel sein soll. Auch dies ist mit Sprechen zu vergleichen. Erst Denken dann Reden.  

- <span id="overlay"><a href="#39" title="Next" >&darr;</a>Wie komplex sind die Operationen?</span><a id="38"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Wenn eine Fülle von unterschiedlichen Operationen ausgeführt werden soll, müssen auch entsprechend viele Anweisungen an das Programm erfolgen und der Autor muss sich auf eine längere Entwicklungszeit einstellen. Wenn es im Gegensatz darum geht eine Hand voll Operationen 1000 mal auszuführen kann es sein, daSs sich der Kern des Skriptes auf 10 Zeile reduziert. DIES bedeutet auch, dasS die Zeit für Entwicklung und Debuggingrelativ gering sein können und sich der Zeitaufwand lohnen kann.<a href="#" class="show_hide" rel="#slidingDiv9">[?]</a><div id="slidingDiv9"> Ein Bug ist ein Fehler im Programm. Debugging ist der Prozess der Fehlersuche. Siehe Abschnitt <a href="#26">7.13 Was ist ein Bug?</a> und <a href="#27">7.14 Was ist Debugging?</a></div> 
  
- <span id="overlay"><a href="#40" title="Next" >&darr;</a>Wie ist das Zeitfenster und wann muss das Produkt fertig sein?</span><a id="39"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Auch hier muss abhängig von der Komplexität des Skriptes und dem eigenem Vermögen geurteilt werden ob dies in dem gegebenen Zeitraum Recherchiert, Entworfen, Geschrieben und "debugged"  werden kann. Hinzu kommt, dass das Ergebnis meist nur ein Teilergebnis ist und noch weiterverarbeitet werden muss. Es ist davon auszugehen das etwaige tiefere Fehler erst während des vollem Einsatzes auftreten. Wenn dies in dem entsprechendem Zeitraum nicht zu bewerkstelligen ist sollte von einer Entwicklung abgesehen werden.

- <span id="overlay"><a href="#41" title="Next" >&darr;</a>Wie oft muss diese Tätigkeit ausgeführt werden?</span><a id="40"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Wenn das Skript nur ein einziges mal ausgeführt werden soll, sollte man sich fragen wo darin der Nutzen liegt. Es kann natürlich sein das dies Sinn und Zweck hat und sollte nur bedingt ausschlaggebend sein. Hierbei gilt es zu Unterscheiden das einmalig 1000 mal einen Knopf drücken bereits eine Hilfe sein kann. Einmalig 1000 mal unterschiedliche Knöpfe drücken ist eine Aufgabe die doch besser manuell geschieht.  

- <span id="overlay"><a href="#42" title="Next" >&darr;</a>Lässt sich die Automation auch auf andere ähnliche Bereiche anwenden oder mit geringen Aufwand abstrahieren?</span><a id="41"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Wenn dies der Fall ist steigt der Nutzen der Arbeit. Der einmalige Aufwand ein Programm oder Skript für eine immer wieder kehrende beziehungsweise ähnliche Aufgabe zu schreiben reduziert sich im "Nachhinein" durch jede Ausführung. Dies soll heissen: Durch das Schreiben des Programms das ich immer wieder verwende spare ich Zeit in der Zukunft. 

- <span id="overlay"><a href="#43" title="Next" >&darr;</a>Wie sehr ist sie (Die Aufgabe) von Umgebungsvariablen abhängig?</span><a id="42"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Kann das Skript unabhängig von allen Variablen die der Benutzer setzen kann ausgeführt werden vereinfacht das den Aufwand. Bei einer Abhängigkeit erfordert es immer erst einer Abfrage des "Ist-Status".  
Ein kleines Beispiel: In Illustrator oder InDesign wird die aktuelle Auswahl des aktiven Dokuments in einer Liste genannt "selection" geführt. <a href="#" class="show_hide" rel="#slidingDiv3">[?]</a><div id="slidingDiv3"> Das selbstgeschriebene Programm ist in diesem Fall aussen vor. Wie bereits oben erwähnt setzt das Programm alle Möglichkeiten voraus. Das Skript hingegen greift auf bestehende Komponenten zu.</div> 
{% highlight js %}
	app.activeDocument.selection;
{% endhighlight %}
In dieser Liste liegen Einzelne Objekte die Text sein können oder eine Vektor-Form oder ein Bild. All diese haben gemeinsame Eigenschaften aber auch spezielle. Es muss also bevor eine Eigenschaft genutzt oder verändert werden kann eine Abfrage stattfinden welche Art von Objekt enthalten ist. Das nachfolgende Beispiel funktioniert in InDesign und Illustrator gleich. Es wird der Name des ersten Objekts in der Selektion abgefragt, wenn dies eine Textkiste ist gibt das Skript eine Meldung zurück.   

{% highlight js %}
  	// InDesign & Illustrator
  	var firstListItem = app.activeDocument.selection[0]; // first object in selection 
  		if(firstListItem instanceof TextFrame){ /* check the type */
  		alert("I am a " + firstListItem.constructor.name);    // and name it
  	}
  {% endhighlight %}  

<br /> <a href="images/ai_id_textframe.png"><img src="images/ai_id_textframe.png" width="100%" alt="" /></a>


Viele solcher Abfrage können ein Skript schnell komplex werden lassen. Oder anders ausgedrückt je universeller der Nutzen sein soll desto mehr Umgebungsvariablen müssen beachtet werden. Dies benötigt Zeit.  

- <span id="overlay"><a href="#44" title="Next" >&darr;</a>Soll die Automation von dritten Benutzt werden?</span><a id="43"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Dies ist ein wichtiger Faktor. Wenn nur der Autor selbst die Automation verwendet kann er seine vorhergehenden Aktionen auf die Bedürfnisse und Beschränkungen des Skriptes anpassen. Wenn jedoch eine unbedarfte oder schlimmer noch eine dem Skripten nicht mä(ö)chtige Person dieses Werkzeug nutzen soll müssen wie bereits oben erwähnt viele Umgebungsvariablen abgefragt oder selber bestimmt werden. Im Programmier-Slang sagt man: "Man muss vom DAU ausgehen." Dies ist nicht als Beleidigung gedacht. Es soll eher sagen dass alle Benutzerfehler die auftreten können auftreten werden. In diesem Fall bekommt ein Nicht des Programmierens Mächtiger wenn er Glück hat nur eine Fehlermeldung, wenn er Pech hat einen Programmabsturz. In beiden Fällen steigt die Hemmung des Nutzer ungemein das Skript noch einmal zu verwenden. Wenn also Dritte mit ins Spiel kommen erfordert es noch längere Test- und Debug-Phasen. <a href="#" class="show_hide" rel="#slidingDiv4">[?]</a><div id="slidingDiv4">DAU: Dümmster Anzunehmender User</div>  
  
- <span id="overlay"><a href="#04" title="Next" >&darr;</a>Ist der Prozess linear oder bedarf es einer Rückkopplung zum Benutzer?</span><a id="44"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Wenn dem so ist sollte der Prozess vielleicht in mehrere Skripte zerlegt werden. Für den Fall das Variablen von einem Skript an das nächste übergeben werden müssen kann dies die Komplexität weiter erhöhen. In diesem Fall gibt es die Möglichkeit eigene Textdateien vom Skript kreieren zu lassen in dem Werte abgelegt werden können, Eine "Script Panel" zu erzeugen oder eine eigene `#targetengine` zu erzeugen in der solange das Programm aktiv ist Daten gespeichert werden. Die letzten beiden sind jedoch fortgeschrittene Lösungen die ebenfalls viele Stolpersteine beherbergen können.  <a href="#" class="show_hide" rel="#slidingDiv5">[?]</a><div id="slidingDiv5"> Ein Script Panel ist eine Erweiterung der Grafischen Oberfläche die es erlaubt während das Skript läuft weiterhin mit dem Programm zu interagieren</div>   

###<span id="overlay"><a href="#05" title="Next" >&darr;</a></span><a id="04"></a>2.1 Das Beispiel targetengine <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span> 
Skript 1:
{% highlight js %}
	#targetengine "session01"
	var myValue = 0; // new value
	alert(myValue); // result is 0
	myValue++; // increment by 1
{% endhighlight %}
  
Skript 2:
{% highlight js %}
	#targetengine "session01"
	alert(myValue); // result is 1
{% endhighlight %}
  
Der Algorithmus lautet wie folgt  

{% highlight js %}
	Start  
	Sitzung 1
	definiere Variable meinWert und Speicher 0 in ihr
	zeige Wert von meinWert
	erhöhe meinWert im eins
	Stop  
  
	Start  
	Sitzung 1
	zeige Wert von meinWert
	Stop  
{% endhighlight %}
  
Dies bedeutet dass das Programm (nicht das Skript) sich den Wert für die Variable `myValue` gemerkt hat und ihn solange in `#targetengine "session01"` speichert bis es beendet wird. Hier liegt die Gefahr darin Variablen Namen doppelt zu vergeben. In vielen meiner Skripte speichere ich das aktive Dokument in der variable `doc`. Wenn diese nun in einer targetengine liegen wird das Programm immer auf das zuletzt `doc` gleichgesetzte Objekt zugreifen auch wenn dies vielleicht nicht gewünscht ist sondern vom Benutzer nicht beachtet wurde. Auch die Verwendung von Textdateien kann ihre Tücken haben. Auf unterschiedlichen Betriebsystemen werden Dateipfade unterschiedlich gehandhabt. Auch dies will abgefragt und getestet werden. "Last but not least" gibt es noch die Möglichkeit eigene Grafische Benutzeroberflächen zu erzeugen. Dies ist aber eine Variante für erfahrenere Autoren.   
  
Die Recherche-Arbeiten sollten bereits vor dem ersten Entwurf erledigt sein.

- <span id="overlay"><a href="#45" title="Next" >&darr;</a>Existieren bereits Automationen in dem Sektor und wenn ja lassen sich diese abwandeln?</span><a id="45"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

Wie bereits oben erwähnt sind viele Probleme bereits einmal aufgetreten am Ende dieser Arbeit ist eine Liste zu finden wo für welchen Zweck nach Informationen gesucht werden kann. Wenn das Problem nicht all zu speziell ist kann es gut sein, dass es bereits ein Skript gibt das entweder genau diese Funktion enthält und wenn nicht auf die eigenen Bedürfnisse angepasst werden kann oder was meist der Fall es mehrere Skripte gibt die Teilprozesse der eigenen Idee beinhalten und als Referenz benutzt werden können. In den seltensten Fällen entsteht ein Skript von Scratch*(aus einem blanken Textdokument). 
  
- <span id="overlay"><a href="#07" title="Next" >&darr;</a>Bietet die API direkten Zugriff auf die benötigten Funktionen oder bedarf es eines Workaround?</span><a id="46"></a><span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  

###<span id="overlay"><a href="#07" title="Next" >&darr;</a></span><a id="05"></a>2.2 Das Beispiel try char <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span> 
Um dies zu erläutern möchte ich mich eines Beispiels bedienen.  
InDesign kann nicht erfragen ob ein Zeichen in einer Schriftart enthalten ist. Es gibt kein Feld das so etwas `wie Font has Character` beinhaltet. Um dieses Abfrage zu simulieren hat Peter Kahreldie Funktion try_char geschrieben die hier in einer etwas abgewandelten Form folgt.   <a href="#" class="show_hide" rel="#slidingDiv6">[?]</a><div id="slidingDiv6"> Peter Kahrel ist einer der präsentesten InDesign Skripter und Autor von "InDesign mit JavaScript automatisieren" erschienen im O'Reilly Verlag</div>    
<br /> <a href="images/algorithmus_trychar.png"><img src="images/algorithmus_trychar.png" width="100%" alt="" /></a>
Um die folgende Funktion `try_char()` sinnvoll ausführen zu können benötigen sie ein InDesign Dokument mit einer Textbox auf der ersten Seite, in der Text in einer Schriftart enthalten ist die die Zeichen des Textes nicht enthält.  

{% highlight js %}
 	var tf = app.activeDocument.pages.item(0).textFrames.item(0);
 
 	for(var i = 0; i < tf.characters.length;i++){
     var theChar = tf.characters.item(i);
     try_char (theChar);
     };
 
 	// original function by Peter Kahrel 
 	// http://www.kahrel.plus.com/indesign/compose_cs3.jsx
 	// edited by fabiantheblind
 	function try_char (theChar){  
 	try {  
     	// save the character 
 		var storage = theChar.contents; 
     	// create outline  
     	theChar.createOutlines();  
     	// if we got here it worked, so delete the outline
     	// if not the next line will be within the catch block  
 		// if not it will cause an error  
     	theChar.remove();  
     	// insert the character (again)  
     	theChar.contents = storage;  
     	} catch(e){  
     	alert("The character "+ theChar.contents + 
     	" could not be converted into an Outline.\n"+
     	"That means he does not exist in the font:\n\""
     	+ theChar.appliedFont.name+"\"");
     	}  
     } 
 {% endhighlight %} 
<br /> <a href="images/try_char_id.png"><img src="images/try_char_id.png" width="100%" alt="" /></a>

Diese Funktion macht folgendes. Sie bekommt eine Zeichen als Parameter. Diesen speichert sie temporär in einer Variable. Dann wird das Zeichen genommen und InDesign versucht es in Pfade umzuwandeln. Dies kann nur passieren wenn das Zeichen in der Schrift auch existiert. Sollte dem so sein wird die neu kreierte Vektor-Form wieder verworfen und das Zeichen wird aus dem Zwischenspeicher wieder hergestellt. Wenn jedoch die Umwandlung einen Fehler erzeugt wird dieser aufgefangen. Dies passiert mit dem Konstrukt `try { } catch (e) { }` Sollte der Inhalt der ersten geschwungenen Klammer oder auch Block genannt einen Fehler erzeugen wird dieser abgebrochen und das Skript führt den Zweiten Block aus. Die Variable `e` ist in diesem Fall die Fehlermeldung. Probieren sie es  mit diesem kurzen Skript aus.  

{% highlight js %}
try{
    var no_no = nothing; // nothing does not exist
    // so this produces an error

}catch(e){
    // open a window and show the alert.
    // \n is just a breakline
    // \" is to show quotation marks in text
    alert("This is the error message \"e\":\n" + e);
	}
{% endhighlight %}
<br /> <a href="images/trycatchscript.png"><img src="images/trycatchscript.png" width="100%" alt="" /></a>

Das Programm wird sie warnen das die Variable `nothing` nicht existiert.  
Solche Lösungen setzen nicht nur ein kreativen Umgang mit Code voraus sondern auch ein tiefes Wissen über die Funktionsweise und Möglichkeiten innerhalb von, in diesem Falle, InDesign.  
Die obig genannten Hindernisse schrecken ab. Es klingt alles sehr komplex. Es ist jedoch alles sehr allgemein gehalten und manche Fragen stelle sich auch erst gar nicht. Bei Aufgaben die ein Normal Nutzer niemals manuell machen würde muss sogar ein Skript geschrieben werden wenn sie erledigt werden sollen.  
Auch wenn der Prozess des Skript-Schreibens eine Kreative Arbeit ist, ist das Ziel des Skriptes nicht der Kreative Output sondern die Optimierung der eigenen Arbeitsabläufe. Das Skript oder Programm kann niemals die Idee liefern. Es unterstützt den Prozess indem es sich wiederholende  Aufgaben erledigt die entweder niemals gemacht worden wären, oder aber vom eigentlichen Kreativem Prozess ablenken.   
<br />
##<span id="overlay"><a href="#08" title="Next" >&darr;</a></span><a id="07"></a>3 Szenarien <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Um besser zu verstehen was das Skript leisten kann soll hier ein Fall Beispiel aufgemacht werden vor dem jeder Layouter einmal stehen könnte. Stellen sie sich vor ihre Aufgabe ist folgende:  
<br>
Erzeugen Sie eine quadratische Bildmatrix in InDesign aus einer definierten Anzahl an quadratischen Bildern mit einer festen Grösse.
<br>
Das würde bedeuten das wir zum Beispiel 4×4 also 16 Bilder darstellen wollen.
Es folgt eine grafische Gegenüberstellung des automatisierten (links) und manuellen (rechts) Prozesses.
<br /> <a href="images/matrix_algorithmus_01.png"><img src="images/matrix_algorithmus_01.png" width="100%" alt="" /></a>
Wird ihnen bereits klar worauf ich hinaus will? Bei 16 Bildern kommen wir auf 38 Aktionen. Mit einem Skript haben wir 3 Aktionen. Wenn es eine 10×10 Matrix sein soll sind das 206 Aktionen im Skript sind es weiterhin 3. Der Kern der Aufgabe ist das errechnen des Layouts. Dies muss in der manuellen sowie in der automatisierten Variante passieren. Also kommt auch der Gestalter der sich für die manuelle entschieden hat auch nicht um etwas Mathematik herum. Da wir von Prozessen im Gestalter Alltag reden kann es gut vorkommen das ein Kunde eine solche Aufgabe an sie stellt.  
Verändern wir die Aufgabe noch ein wenig:  
Erzeugen Sie eine Bildmatrix in InDesign aus einer noch nicht definierten Anzahl an quadratischen Bildern mit einer festen Grösse.   
<br /> <a href="images/matrix_algorithmus_02.png"><img src="images/matrix_algorithmus_02.png" width="100%" alt="" /></a>  
Um dieser Anforderung gerecht zu werden müssen wir in der automatisierten Variante eine Kondition einführen. Wenn die gerundete Wurzel eine Fließkommazahl ist, ist die Seitenhöhe die Seitenbreite plus eine Bildbreit.  
<br />
###<span id="overlay"><a href="#33" title="Next" >&darr;</a></span><a id="08"></a>3.1 Der Einsatz - das Beispiel image matrix <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Die Fragen die sich jetzt stellen sind folgende: "Wie kommt dies zum Einsatz?", "Wie kann ich dies nutzen?".
Es folgt nun das InDesign Skript image_matrix.jsx mit etwas mehr als 40 Zeilen Code. Dieses Skript beinhaltet eine Benutzer Interaktion, Dateihandhabung, das Math Objekt, Konditionen, eine Schleife, Funktionen, Variablen und es hat einen generativen Charakter. Das Skript erledigt folgende Schritte. <a href="#" class="show_hide" rel="#slidingDiv7">[?]</a><div id="slidingDiv7"> Das Math Objekt ist ein ein bereits bestehender Teil von JavaScript. Es erledigt solche Aufgaben wie Rundung von Werten oder das Berechnen einer Quadratwurzel</div>  

- Frage den Benutzer nach einem Ordner mit jpg Dateien.  
- Erzeuge ein Quadratisches Dokument dessen Grösse auf der Quadratwurzel der Menge der Bilder basiert und alle Bilder fast.  
- Platziere alle Bilder.  

  
Kopieren sie den nachstehenden Code und bereiten sie einen Ordner mit einigen Jpg-Bildern vor. Das Skript das unten beschrieben wird verarbeitet NUR .jpg Dateien, Dateien die .jpeg oder .JPG heissen werden ignoriert. Es sollten um die 15 bis 30 sein damit die Ausführung des Skriptes nicht zuviel Zeit in Anspruch nimmt. Es kann jedoch auch 100, 1000 oder mehr Bildern verarbeiten. Die genau Menge ist irrelevant. Lesen sie nochmal den Abschnitt <a href="#21">7.08 Was ist Hello World?</a>  und führen sie das Skript aus. Wenn der Ordnerauswahl Dialog sich öffnet wähle sie den Ordner mit den Bildern.
Das gesamte Skript:  

{% highlight js %}
	{ // START SCRIPT
	main(); // you need a function to be able to cancel a script

	function main(){ // all is in here

	var w = 25; // the image sizes
	var allImages = loadFiles("*.jpg"); // opens a prompt and lets the user choose a folder
	if(allImages == null) return; // if that what the function returns null is - cancel

	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2); // this will hold the page width
	var ph = pw;

	if(Math.round(Math.sqrt(allImages.length)) != Math.sqrt(allImages.length)){
	        ph = pw + w;
	        }

	var doc = app.documents.add(); //build a basic document
	doc.documentPreferences.pageWidth = pw; // set the width
	doc.documentPreferences.pageHeight = ph; // set the height
	var page = doc.pages.item(0); // finally - get the first page

	var y = w; // the upper left corner
	var x = w; // the upper left corner

	for(var i = 0; i < allImages.length;i++){ // loop thru all images

	var rect = page.rectangles.add({geometricBounds:[y,x,y + w,x + w]}); // add a rectangle to the page
	rect.place(allImages[i] ); // place the image
    rect.fit(FitOptions.FILL_PROPORTIONALLY); // fit it to the frame
    rect.fit(FitOptions.CENTER_CONTENT); // fit it to the frame
    x +=w; // increase x by an image width

	if(x >= pw - (w)){ // if x is the width minus an image width
	        x = w; // reset x
	        y+= w; // and increment y by an image width
	        }; //end increase x and y conditional

	    };//close allImages loop

	};// end main function

	function loadFiles(type){ // the function that loads the files

	var theFolder = Folder.selectDialog ("Choose the Folder");// user select a folder

	if(!theFolder){ // if the folder is not a folder cancel the script
		return; // this cancels the whole function image_loadFiles
			}; // end folder check

	var allImages = theFolder.getFiles(type);// get the files by type
	if((allImages.length < 1)||(allImages == null) ){// again if check if there are images
		alert("There are no images of the type: " + type);// hm something went wrong? User error
		return null; // so we cancel the function
		   }else{
		return allImages; // give back the images. Success!
	        };// end all images check

		};// end function loadFiles
	} // END OF SCRIPT
{% endhighlight %}
<br>
####<span id="overlay"><a href="#09" title="Next" >&darr;</a></span><a id="33"></a>3.1.1 Ergebnisse - image matrix <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Alle 3 nachfolgenden Bilder sind mit ein und dem selbem Skript erzeugt.  
<br /> <a href="images/image_matrix_1.jpg"><img src="images/image_matrix_1.jpg" width="100%" style="max-width:500px;" alt="" /></a><br />
<br /> <a href="images/image_matrix_2.jpg"><img src="images/image_matrix_2.jpg" width="100%" style="max-width:500px;" alt="" /></a><br />
<br /> <a href="images/image_matrix_3.jpg"><img src="images/image_matrix_3.jpg" width="100%" style="max-width:500px;" alt="" /></a><br />


###<span id="overlay"><a href="#10" title="Next" >&darr;</a></span><a id="09"></a>3.2 image matrix - Schritt für Schritt. <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  
Ein Skript sollte immer in geschwungenen Klammern eingefasst sein. Dies ist nicht zwingend jedoch nützlich falls das Skript von einem anderem Skript evaluiert werden muss. Innerhalb dieser Klammern folgt der gesamte Quelltext.  

	{}

Als nächstes definieren wir eine Funktion die einmalig aufgerufen wird. Hierbei ist es irrelevant ob der Aufruf vor oder nach der Funktionsdefinition stattfindet. Aus Gründen der Übersichtlichkeit steht hier der Aufruf vor der Definition. Diese Funktion erhält keine Parameter. Später wird auch ein Funktion mit Parametern eingesetzt. Der Zweck den gesamten Code in einer Funktion zu kapseln ist folgender: Wenn es eine hierarchisch höhere Ebene gibt, unsere `{}` Klammern, kann eine Funktion mit dem Befehl `return;` beendet werden. Dies ist nützlich um bei Fehlern oder falscher Benutzer Eingabe die Ausführung zu stoppen. Mit dem Befehl `return` kann nicht nur ein Funktion beendet werden sondern auch ein Wert zurückgeliefert werden.  
Wenn wir also schreiben `return 1;` am Ende einer Funktion wäre das Ergebnis 1. `var myValue = main();` Wenn die Funktion main nun einen Wert zurückgeben würde, wäre `myValue` 1. In unserem Fall benötigt die `main()` keinen Rückgabewert.

{% highlight js %}
	main();
	function main(){
	}
{% endhighlight %}

Wir befinden uns nun in der Funktion `main();`.  
Es folgt die Deklaration der ersten Variable. Sie beinhaltet die Breite (und Höhe) unserer Bilder.

{% highlight js %}
	var w = 25;
{% endhighlight %}

Wie zu sehen ist entspricht die Variable `w`*(steht für width) nun 25. `w` wird im Verlauf des Skriptes mehrmals verwendet. Der Vorteil  daran Variablen zu verwenden anstatt immer 25 zu schreiben ist, dass wenn wir die Breite verändern wollen wir dies nur ein einziges mal an `w` erledigen müssen und alle weiteren Verwendungen von `w` werden angepasst.  
Als nächstes folgt bereits die nächste Subfunktion mit einem Parameter und einem Rückgabewert. In JavaScript werden alle Variablen mit `var` deklariert. Die Unterscheidung des Typus findet erst bei der Verwendung statt. Deshalb können wir schreiben.  

{% highlight js %}
	var allImages = loadFiles("*.jpg");
{% endhighlight %}

Damit die Funktion auch vorhanden ist fügen wir sie hinter `function main(){ }` an.
Unser Code sieht also wie folgt aus.  

{% highlight js %}
	{
	main();
		function main(){
			var w = 25;
			var allImages = loadFiles("*.jpg");
		}
		function loadFiles(type){
			return 0;
		}
	}
{% endhighlight %}

Den Rückgabewert werden wir noch verändern, denn wir wollen Bilder laden und nicht 0. Wie oben zu sehen ist erhält `loadFiles` den Parameter `type`. Dies ist der Dateityp der später geladen werden soll. `type` ist genau wie `w` und `allImages` eine Variable nur das wir im Parameter Block der Funktion das `var` weglassen können.  
Wenn wir `*.*` schreiben würden würde unsere Funktion jeden Dateityp laden. Der Einfachheit halber beschränken wir uns auf jpg da wir wissen das InDesign jpg-Dateien laden und platzieren kann.  
Als nächstes begeben wir uns in die Funktion `loadFiles` und betrachten die Dateihandhabung und eine Benutzerinteraktion. Basierend auf dem Ergebnis der Interaktion fällt das Skript eine Konditionale Entscheidung ob es weiter arbeiten soll oder ob es die Funktion `loadFiles` beendet.  

{% highlight js %}
	var theFolder = Folder.selectDialog ("Choose the Folder");
	if(!theFolder){ 
			return;
			};
{% endhighlight %}

Bisher waren alle Befehle JavaScript Befehle. Der Befehl `Folder.selectDialog ("Choose the Folder")` jedoch ist <a href="#31">ExtendScript</a>. das Objekt `Folder` hat eine eigene Funktion `selectDialog(parameter)`. Wir müssen diese Funktion nicht betrachten. Wir müssen nur wissen, dass sie ein Interface öffnet und dem Benutzer die Möglichkeit gibt einen beliebigen Ordner auszuwählen. Der Parameter ist der Text der auf dem Auswahldialog oben zu sehen ist. Der gewählte Ordner wird dann in der neuen Variable `theFolder` für eine spätere Referenzierung gespeichert. Dann folgt das Konstrukt der Konditionalen Abfrage.

{% highlight js %}
	if( Statement ){ Do Something }
{% endhighlight %}

Sie besagt, dass wenn die Aussage in der runden Klammer war ist die geschwungene Klammer ausgeführt wird. in unserem Fall wird durch das `!` die Aussage negiert. Ausgeschrieben könnte dort stehen `if(theFolder == false)` oder `if(theFolder != true)` die Schreibweise `if(!theFolder)` ist einfach nur verkürzt. Wenn wir  `if(theFolder)` schreiben würden würde das `if(theFolder==true)` entsprechen. Zu Beachten ist nicht `=` zu schreiben. Dies bedeutet "ist gleich", `==` bedeutet "entspricht". Gesprochen wäre unsere Aussage: "Wenn der Ordner nicht existiert - beende die Funktion".  
Als nächstes betrachten wir was das Laden der Dateien aus unserem Ordner.  

{% highlight js %}
	var allImages = theFolder.getFiles(type);
{% endhighlight %}

Ordner Objekte (Folder) haben eine weiter eingebaute Funktion: `getFiles(parameter)`. Diese hat auch einen Parameter. Den Dateityp. Hierbei wird nicht nur eine einzelne Datei zurückgegeben sondern eine Sammlung aller Dateien des angegebenen Typs. Dies ist ein Array. Ein Array sollte man sich als eine Liste vorstellen deren Positionen über einen Index aufgerufen werden können. Hierbei ist zu beachten das das erste Objekt in der Liste nicht mit 1 sondern mit 0 angesprochen wird. Also ist `allImages[0]` das erste Bild unserer Liste.  
Nun folgt ein weitere Sicherheitscheck ob wir Bilder gefunden haben und die Bestimmung des Rückgabewerts unserer Funktion. Ebenfalls wird der Nutzer wenn es keine Bilder gibt darauf hingewiesen.

{% highlight js %}
	if((allImages.length < 1) || (allImages == null) ){
		alert("There are no images of the type: " + type);
		return null;	   
	}else{
		return allImages;
	};
{% endhighlight %}

Wie wir oben sehen benutzen wir nochmals die Konditionale Entscheidung `if()`. jedoch mit einer Erweiterung dem `else`. Dies bedeutet das auf jeden Fall eine er beiden Blöcke ausgeführt wird. Um es im <a href="#18">Pseudocode</a> darzustellen:  

{% highlight js %}
Wenn die Aussage zutrifft mach dies ansonsten mach dass
{% endhighlight %}

Innerhalb unsere runden Aussage Klammer haben wir mehrere Aussagen verknüpft. wir haben also 2 Aussagen. Mit dem `||` sagen wir entweder oder. In unserem Fall ist das einmal der Check ob wir mindestens ein Bild haben `(allImages.length < 1)`. `length` ist eine Eigenschaft jedes Arrays und gibt wenn wir ein Bild haben 1 zurück. Wenn es einhundert sind 100. Wir fragen also ob die länge von unserer Liste kleiner als 1 ist. Diese Aussage verbinden wir mit `||` dies bedeutet "oder". Wenn also Aussage 1 oder Aussage 2 zutreffen führe den ersten Block aus. Wenn wir beide Aussagen Abfragen wollten müssten wir `&&` schreiben. Dies würde nur den ersten Block ausführen wenn beide Aussagen zutreffen. In unserem zweiten Aussage fragen wir nach `null`, dies ist etwas ähnliches wie nichts. Also wenn wir einen Fehler beim Laden der Bilder hatten oder `allImages` nicht existiert. Im ersten Block beenden wir nur die Funktion. Wenn keine der beiden Aussagen zutrifft sollten wir eine Liste von Bildern haben und diese geben wir mit `return allImages` an unsere Funktion `main` zurück.
  
Wir befinden uns wieder in der Funktion main und werden einen weiter Abfrage starten.

{% highlight js %}
if(allImages == null) return;
{% endhighlight %}

Wenn `loadImages` `null` zurückgibt bricht das Skript ab. Dies ist nötig da `loadImages` in der Funktion `main` stattfindet. Also führt ein `return` in `loadImages` nur zurück nach `main` und nicht zum beenden des Skripts. Hier ist ebenfalls eine verkürzte Schreibweise zu sehen. Wir können uns die geschwungenen Klammern sparen wenn wir nur einen einzigen Befehl haben. Das heisst:  

{% highlight js %}
	if(statement){doSomething;} 
{% endhighlight %}

entspricht:  

{% highlight js %}
	if(statement) doSomething
{% endhighlight %}

Ebenfalls könnte 

{% highlight js %}
	if(statement){doSomething;}else{doSomethingElse;}
{% endhighlight %}

als

{% highlight js %}
	if(statement) doSomething; else doSomethingElse;
{% endhighlight %}

abgekürzt werden. Dies geht jedoch nur bei jeweils einem Befehl nach der Aussage.  

Als nächstes folgt die Berechnung unserer Seitenbreite und Seitenhöhe. Die Höhe wird nochmals mit einer Kondition überprüft. Wenn die Menge an Bildern nicht in ein Matrix passt, also 3 mal 3 oder 4 mal 4 oder 100 mal 100 muss die Höhe nochmals um eine Zeile erweitert werden. Hier kommt das JavaScript Objekt `Math` zum Einsatz.   

{% highlight js %}
	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2);
	var ph = pw;
	if(Math.round(Math.sqrt(allImages.length)) != Math.sqrt(allImages.length)){
	        ph = pw + w;
	}
{% endhighlight %}

Dies wirkt kompliziert. Um es zu Verstehen lösen wir den ersten Satz einmal auf. Betrachten sie das Bild dabei.  

{% highlight js %}
 	a ist gleich 16. Die Menge an Bildern.  
 	b ist die Wurzel aus a. Wir wollen es rechteckig. Also 4.  
 	c ist b gerundet. Falls es eine Gleitkommazahl ist. Bleibt in diesem Fall 4, wenn a 16 ist.
 	d ist 25. Die Breite der Bilder.  
 	e ist c mal d. Wir staffeln die Bilder nach rechts. 4×25 also 100  
 	f ist d mal 2. Das ist Links und Rechts der Abstand zum Seitenrand.
 	Jeweils eine Bildbreite. Also 50 
 {% endhighlight %} 

<br /> <a href="images/matrix_think.png"><img src="images/matrix_think.png" width="100%" style="max-width:500px;" alt="" /></a><br />

Also ist unsere Seitenbreite 150  

Die Breite der Bilder mal der auf- oder abgerundeten Wurzel aus der Menge an Bildern plus eine Bildbreite links und eine rechts. (Lesen sie den vorherigen Satz nochmals und versuchen sie sich ein geistiges Bild von der Berechnung zu machen.)   

oder    
g = [√a] × d + (d × 2)  
oder  

{% highlight js %}
	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2);  
{% endhighlight %}

Danach setzen wir die Höhe der Seite der Breite gleich.
Für den Fall das b (oder `Math.sqrt(allImages.length)`) eine Fliesskommazahl ist und wir eine nicht rechteckige Matrix erzeugen müssen, also alle Bilder platziert werden sollen, müssen wir die Höhe der Seite um eine Zeile für Bilder erweitern. Deshalb vergleichen wir in dem `if(statement)` ob die gerundete Quadratwurzel kleiner als die Quadratwurzel ist.

{% highlight js %}
	(Math.round(Math.sqrt(allImages.length)) < Math.sqrt(allImages.length)
{% endhighlight %}

oder  
[√a] ≠ √a  
oder  
Wenn die Wurzel aus der Menge an Bilder nicht der gerundeten Wurzel aus der Menge an Bildern entspricht ist die Seitenhöhe die Seitenbreite plus eine Bildbreite. Wenn a also 17 ist wäre die Seite 150 breit und 175 hoch.  
  
ich vermeide hier um es nicht noch weiter zu verkomplizieren jede Art von Maßeinheit. Das lassen wir InDesign selber regeln. In der Standard-Einstellung sind es Millimeter. Dies könnten wir definieren müssen wir aber nicht da InDesign immer eine Grundeinstellung hat.  
Als nächstes folgen das erzeugen des Dokuments, das einstellen der Seite auf unsere errechneten Werte, das überführen der ersten Seite im Dokument in eine Variable und die Definition unseres Startpunktes.  

{% highlight js %}
	var doc = app.documents.add();
	    doc.documentPreferences.pageWidth = pw;
	    doc.documentPreferences.pageHeight = ph;
	var page = doc.pages.item(0);
	var y = w;
	var x = w;
{% endhighlight %}

Diese Zeilen sind fast selbst erklärend. Wir fügen der Sammlung an Dokumenten ein neues hinzu. Dabei ist irrelevant ob bereits ein Dokument existiert oder nicht. Dann stellen wir die Weite und Höhe der Seite ein. Dann nehmen wir aus der Sammlung an Seiten in dem neuem Dokument die Erste. Der Aufruf `item(0)` ist ebenfalls ein ExtendScript Befehl der nur in InDesign funktioniert. wir könnten auch `var page = doc.pages[0]` schreiben. Hier funktioniert beides gleich. Das ist jedoch nicht immer der Fall. Es gibt zum Beispiel die Möglichkeit `doc.pages.middleItem()` oder `doc.pages.lastItem()` abzufragen. Bei einem normalen Array wie unserem `allImages` würde `lastItem()` nicht funktionieren. Danach erzeugen wir die Startpunkt unseres ersten Bildes. x und y sind jeweils eine Bildbreite vom Rand der Seite entfernt.
Es gibt noch die Möglichkeit die ersten drei Zeilen abzukürzen. Dies ist eine komprimiert Schreibweise die uns noch öfter begegnen wird.  

{% highlight js %}
	var doc = app.documents.add({documentPreferences:{pageWidth:pw,pageHeight:ph}});
{% endhighlight %}

Aber zu dieser Schachtelung kommen wir noch. Wir sind bereits halb durch. Es folgt nochmals ein weiteres Konstrukt. die Schleife.  

{% highlight js %}
	for(var i = 0; i < allImages.length;i++){
	var rect = page.rectangles.add({geometricBounds:[y, x, y + w,x + w]});
	rect.place(allImages[i] );
	rect.fit(FitOptions.FILL_PROPORTIONALLY);// fit it to the frame
	rect.fit(FitOptions.CENTER_CONTENT);// fit it to the frame
	x +=w;
	}
{% endhighlight %}

Mit dieser Schleife würden wir nur Bilder nach rechts weiter setzen. Den "Zeilenumbruch" fügen wir später ein. Erst einmal die Aussage der Schleife ähnelt der Kondition `for(statment){doSomething}` nur mit `for` anstatt `if`. Es könnte als an _solange_ übersetzt werden. Solange du durch die Liste der Bilder zählen kannst. Die Aussage `for(var i = 0; i < allImages.length; i++ )` ist  eine verkürzte Schreibweise für `for(var i = 0; i < allImages.length; i = i + 1 )`. Es wäre  auch möglich `for(var i = 5; i < 100; i= i +5)` zu schreiben. Das Bedeutet. Zähler i ist 5. Solange i kleiner als 100 ist, erhöhe i um 5. Im ersten durchlauf ist i 5 im zweiten 10 im dritten 15. Wir würden dann nur das 5te ,10te und 15te Bild erhalten anstatt alle.  
Es folgt:  

{% highlight js %}
	var rect = page.rectangles.add({geometricBounds:[y, x, y + w,x + w]});
{% endhighlight %}

Wir erzeugen auf der ersten Seite eine Rechteck, ähnlich wie unser Dokument und stellen die Aussenkanten ein. Die `geometricBounds`. Wir könnten auch folgendes schreiben.  
  
{% highlight js %}
	var rect = page.rectangles.add();
	var y1 = y;
	var x1 = x;
	var y2 = y1 + w;
	var x2 = x1 + w;
	rect.geometricBounds = [y1, x1, y2, x2];
{% endhighlight %}
  
Die Eigenschaft `geometricBounds` erwartet immer ein Array mit 4 Stellen. Diese geben die Linke obere Ecke und die Rechte untere Ecke an. Immer von der Oberen beziehungsweise linken Kante der Seite gemessen. Hierbei steht die y Koordinate vor der x Koordinate. Zu beachten ist auch, dass innerhalb von `add()` ein Doppelpunkt anstatt eines Gleichheitszeichens bei der Zuweisung des Wertes verwendet werden muss.  
Es folgen drei einfache Befehle.  
  
{% highlight js %}
	rect.place(allImages[i] );
	rect.fit(FitOptions.FILL_PROPORTIONALLY);// fit it to the frame
	rect.fit(FitOptions.CENTER_CONTENT);// fit it to the frame
	x +=w;
{% endhighlight %}
  
Das Bild mit dem Index i wird in dem Rechteck platziert, der Inhalt wird an die Grösse des Rechteckes angepasst, zentriert und wir erhöhen den x Wert um eine Bildbreite. Hier könnte auch `x = x + w` stehen. Es gibt weiter verkürzte Schreibweisen wie:

{% highlight js %}
	x-=5; //  equivalent to x = x - 5;
	x*=5; //  equivalent to x = x * 5;
	x/=5; //  equivalent to x = x / 5;
{% endhighlight %}

Da wir in unserer Schleife sind passiert dies für die komplette Menge der Bilder unabhängig davon ob wir 5, 100 oder 10000 haben. Dies ist eine der großen Stärken von Skripten und Programmen. Die Iteration.  
Damit wir jedoch nicht nur Bilder nach Rechts platzieren sondern umbrechen wenn x (oder x1) größer oder gleich der Breite der Seite minus der Bildbreite (der Rand) ist müssen wir eine weitere Kondition hinzufügen.  

{% highlight js %}
	if(x >= pw - (w)){
 	x = w;
 	y+= w;
 	}
{% endhighlight %}

Wenn diese Kondition nicht da wäre würde das Skript die Bilder wie in der folgenden Grafik platzieren. Achtung! Wenn zuviel Bilder über die Arbeitsfläche hinaus gehen kann das InDesign zum Absturz bringen und oder das Dokument unwiderruflich zerstören.  
<br /> <a href="images/matrx_without_breakline.png"><img src="images/matrx_without_breakline.png" width="100%" alt="" /></a><br />
Die die es bis hier her geschafft haben sollten den obigen Code jetzt entschlüsseln können.  
Wenn x grösser gleich 150 - 25, um auf unser Beispiel mit der 16 als Menge der Bilder zurückzukommen, setze x zurück auf 25 und addiere auf y 25 auf. die Zahlenreihe ist dann:  

{% highlight js %}	
	i = 0
	x = 25
	y = 25  
{% endhighlight %}

dann

{% highlight js %}
	i = 1
	x = 50
	y = 25
{% endhighlight %}

Das passiert solange bis x 125 ist.  
Dort setzt die Kondition `if(x >= pw - (w))` an.  
x wird in der Kondition zurück auf 25 gesetzt und y wird auf 50 gesetzt.
Dann ist  

	{% highlight js %}
		i = 4.
	{% endhighlight %}

Wir fangen bei 0 an zu Zählen im Array also ist `allImages[4]` das fünfte Bild.
und so weiter und so weiter.  
Wir sind am Ende. Probieren sie den Code mit unterschiedliche vielen Jpg-Dateien aus. Verändern sie ihn bis er nicht mehr funktioniert und lesen sie die Fehlermeldungen. Dies ist ein weiterverbreitetes Problem. Computer und Programme würden viel an ihrer Mystik verlieren wenn einerseits die Nutzer die Meldungen lesen würde anstatt nur auf ok zu drücken und andererseits die Meldungen verständlich geschrieben wären.  
<br /> <a href="images/error.png"><img src="images/error.png" width="100%" alt="" /></a><br />  
###<span id="overlay"><a href="#12" title="Next" >&darr;</a></span><a id="10"></a>3.3 Das Beispiel great power <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Ein weiters Skript, _greatPower.jsx_, welches aus nur einer Befehlszeile besteht und dennoch mächtig und auch ein wenig gefährlich ist.  
Wenn bei der Entwicklung eines anderen Skripts immer wieder neue Dokumente erzeugt werden kann es schnell passieren, dass 10, 20, 50 Dokumente geöffnet sind. Die Oberfläche von InDesign bietet nicht die Möglichkeit alle geöffneten Dokumente zu schliessen ohne zu speichern. Das bedeutet das bei 50 Dokumenten 50 mal beim Schliessen entweder gespeichert oder das Dokument verworfen werden muss. Mit greatPower.jsx ist dies möglich. Um dies auszuprobieren erzeugen wir ein paar Dokumente mit dem Skript createDocuments.jsx. Dies is stark verkürzt in seiner Schreibweise und verwendet eine andere Art von Schleife. die `while` Schleife.   
<br /> <a href="images/algocreatedoc.png"><img src="images/algocreatedoc.png" width="100%" alt="" /></a><br />  

{% highlight js %}
	// createDocuments.jsx
	var counter = 0;
	var numberOfDocuments = 22;
	while(counter <= numberOfDocuments){
	app.documents.add({
	    documentPreferences:{
	        pageWidth:100,pageHeight:100
	        }
	    });
	var tf = app.activeDocument.pages.item(0).textFrames.add({
	    geometricBounds:[10,10,90,90],
	    contents:String(counter) + "Hello World"
	    });
	tf.characters.everyItem().properties = {
	    pointSize:42
	    };
	counter++;
	}
{% endhighlight %}

Um diese 23 Dokumente wieder zu schliessen benutzen sie "greatPower.jsx"
<br /> <a href="images/algogreatpower.png"><img src="images/algogreatpower.png" width="100%" alt="" /></a><br />  
{% highlight js %}
 	// Like Uncle Ben saz: "With great power comes great responsability!"
 	app.documents.everyItem().close(SaveOptions.NO);
{% endhighlight %} 
Wenn nun dem ein oder anderem der Gedanke kommt: "Das ist doch alles viel zu kompliziert!" Warum dies mehr Unwille den Unvermögen ist werde ich versuchen im nächsten Teil zu untersuchen.   

##<span id="overlay"><a href="#11" title="Next" >&darr;</a></span><a id="12"></a>4 Ein Werkzeug - AEMap<span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span> 
Wo bleibt die extra Zeit für Gestaltung die versprochen wurde? Wie bereits erwähnt braucht das lernen einer Sprache etwas Zeit. Die Grammatik und Rechtschreibung können aus einem Buch gelernt werden, die Nuancen und Umgangssprache kann jedoch nur durch das Sprechen geschult werden.  
Zum Glück sind wir hier nicht alleine. Es gibt bereits viele Werkzeuge die frei zur Verfügung stehen und zur Optimierung unserer Arbeitsprozesse genutzt werden können. In diesem Sinne habe ich das Skript AEMap.jsx für Adobe After Effects geschrieben.  
<br /> <a href="images/aemapuiv02a.png"><img src="images/aemapuiv02a.png" width="100%" alt="" /></a><br />  

Viele Motion Designer kommen irgendwann einmal an den Punkt an dem sie eine Weltkarte oder die Aussenkontur eines Landes benötigen. Bisher war es so das immer wieder eine Websuche begann nach benutzbaren Kartenmaterial. Hierbei entstehen einige Problem. Die Rechte an Kartenmaterial das "einfach so" aus dem Netz gezogen wurde sind oft ungeklärt. Manchmal sind es Vektor-Dateien wenn man Pech hat sind es Pixelbilder. Diese Quelldatei liegt dann innerhalb eines Projektes und wird mit diesem archiviert. Wenn sie wieder benötigt wird beginnt die Suche aufs neue. Was bei vielen absolvierten Projekten schnell zeitraubend werden kann. After Effects Projekte können schnell aus hunderten Quelldateien bestehen und sind gerne nach persönlichem Gusto sortiert. Was wenn dann nicht nur eine Weltkarte sondern zum Beispiel die Kontur von Ost-Timor und Papua Neu Guinea benötigt wird?  

<br /> <a href="images/ostimorpaua_01.jpg"><img src="images/ostimorpaua_01.jpg" width="100%" alt="" /></a><br />  

Selbst wenn eine vernünftige Vektor-Form einer Karte existiert und griffbereit ist wie könne die beiden Länder gefunden werden? Was ist wenn eine Grenzänderung stattfindet? Und und und. Um diesen Problemen zu entgehen kann AEMap.jsx eine Weltkarte in Rektangularprojektion erzeugen. Dabei entsteht eine After Effects Komposition in einer gewählten Skalierung (immer 2:1) in der 178 Prä-Kompositionen enthalten sind die 286 einzelne Polygon-Gruppen beinhalten.
<br /> <a href="images/aemapfullcomp.png"><img src="images/aemapfullcomp.png" width="100%" alt="" /></a><br />  
Der Nutzer kann zwischen verschiedenen Einstellungen wählen wie zum Beispiel die Karte mit Kontur zu zeichnen oder ohne oder ob alle Polygone auf eine Ebene gezeichnet werden sollen oder ob in die oben genannten Kompositionen gesplittet werden soll. Ebenfalls können 3D Einstellungen definiert werden und ähnliche mehr. Die Daten bestehen auf einem GeoJson Datensatz der zum freien Gebrauch ins Netz gestellt wurde. Der gesamten Funktionsumfang ist auf [dieser Webseite](http://fabiantheblind.github.com/AEMap/) dokumentiert. Dieses Skript spart nicht nur mir Zeit sondern auch anderen. Die Resonanz in der After Effects Community" ist gross. Daher hat das Skript seit seiner Veröffentlichung auf [AEScripts.com](http://aescripts.com/aemap/) am 10 April 2012 bereits über 400 Downloads gehabt (heute 24 April 2012). Das Tutorial und das Demo wurden bereits über 4000 mal auf Youtube geladen. Aber genug der Selbstbeweihräucherung. Der Vorteil an solchen und ähnlichen Werkzeugen die zum Beispiel auf AEScripts.com bereit gestellt werden ist, dass diese meist aus dem Zwang heraus entstanden sind einen Arbeitsablauf zu automatisieren um Zeit zu sparen. 

##<span id="overlay"><a href="#06" title="Next" >&darr;</a></span><a id="11"></a>5 Die Angst <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Wann immer ich gefragt werde über was ich schreibe oder womit ich mich beschäftige und ich antworte: "Programmieren", stosse ich auf die Aussage: "Das werde ich nie lernen." Woher kommt diese Annahme? 
Auf der TEDxVancouver im November 2011  beschreibt Jef Thorp eine Situation die gut unseren aktuellen Zustand beschreibt:
Wenn man vor 30 Jahren einem Programmierer gesagt hätte: "In 30 Jahren haben alle einen Computer aber keiner wird wissen wie man programmiert." Hätte dieser gesagt das ist nicht möglich.
Computer haben sich von den Rechenmaschienen der Spezialisten zu einem alltäglichen Ding entwickelt, das wir nutzen und akzeptieren dem wir aber nicht unter die Haube gucken möchten.
Oder anders.
> „Jede hinreichend fortschrittliche Technologie ist von Magie nicht zu unterscheiden.“
> Sir Arthur C. Clarke's Drittes Gesetz

Wir haben Computer und ihre Funktionsweise mystifizert ein "Klerus" die wir Programmiere nennen erzeugt Ohs und Ahs aber wie dieser Zauber wirkt wissen wir nicht. Da ich keinen Einblick in die derzeitige Situation an unseren Schulen habe kann ich das Folgende nur aus meiner eigenen Erfahrung beurteilen. Ein frühes Vertrautmachen mit Computern gab es in meiner schulischen Laufbahn nicht. Wer Interesse hatte konnte in die Computer-AG eintreten. Freiwillig. Bei einem eher musisch begabtem Menschen ruft die natürlich wenig Begeisterung hervor. Ich denke damit stehe ich nicht allein. Die Angst kommt vom Unbekannten. Um auf den Vergleich des Auslandsaufenthalts zurück zu kommen, natürlich haben wir ein unwohles Gefühl wenn wir uns dort aufhalten wo wir uns nicht auskennen. Wir werden weiterhin versuchen, so oft wir können, unsere eigene Sprache anstatt der Landessprache zu nutzen. Dies ist menschlich - und und ein wenig töricht.  
Mit dem erlernen einer Computersprache vollzieht sich ein Wandel. Es ist der Schritt vom Bediener eines von anderen gefertigten Werkzeugen zu einem Macher von Werkzeugen. Die Programme die wir als Grafiker nutzen sind nach der Idee eines Teams von Menschen geformt. Wir haben keinen Einfluss auf die Funktionsweise. Mit dem Schreiben von Programmen oder Skripten kann dies überwunden werden.  

##<span id="overlay"><a href="#13" title="Next" >&darr;</a></span><a id="06"></a>6 Fazit <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Programmieren ist nicht leicht, aber leichter als man denkt. Es gibt Stolpersteine. Gerade der Anfang hat eine flache Lernkurve. Ab einem gewissen Punkt ändert sich dies aber der muss erst erreicht werden. Der Idealfall zum erlernen von Computersprachen ist unter Zwang. Wenn sie vor einem Problem stehen das manuell nicht gelösst werden kann aber gelösst werden muss.  
Alle anderen müssen sich selbst überwinden. Es kann vieles mit einer Automation durch Programmierung gelöst werden. Sie ist nicht die Lösung unserer Arbeit sondern die Entschlackung unseres Arbeitsprozesses von geisttötenden Aufgaben. Sie schafft Raum für komplexe Visualisierungen und Zeit für das Konzept, wenn die eigenen Fertigkeiten gefesstigt sind. Das Lernen dieser Sprachen ist wie im Neuen Jahr mit dem Rauchen aufhören und regelmäßig Sport trieben. Man muss es einfach machen. Auch dies ist nicht leicht aber vielleicht besser für uns.  
Wichtig ist keine Dogmas zu erschaffen. Eine Aufgabe automatisiert zu lösen um der Automation willen kann genauso kontraproduktiv sein wie sich mit einem "Ich kann das nicht!" zufrieden zu geben.


****************************

##<span id="overlay"><a href="#14" title="Next" >&darr;</a></span><a id="13"></a>7 Die kleine Terminologie <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Dieser Abschnitt ist zur Erläuterung gedacht und um den Lesefluss nicht durch sekundär Informationen und Erklärungen von FAchbegriffen zu unterbrechen. 

###<span id="overlay"><a href="#15" title="Next" >&darr;</a></span><a id="14"></a>Was ist Code? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Als Code bezeichnen wir in der Regeln Informationen die verschlüsselt (encoding) werden um dann an einer weiteren Stelle wieder entschlüsselt zu werden (decoding). Zum Beispiel stellt Morse-Code Buchstaben dar indem ein einziges unmoduliertes Signal, zum Beispiel ein Ton, in kurze und lange Sequenzen unterteilt wird. Der Rezipient kann dann, wenn er des Systems mächtig ist, diese Informationen entschlüsseln und zu der originalen Nachricht wieder zusammensetzen. Ein weiters Bespiel ist der Abakus. Dieser erlaubt es wenn der Benutzer des Systems mächtig ist Rechenoperationen auszuführen. Und als drittes die Knotenschrift der Inkas die wie der Name bereits besagt aus einem System von Knoten auf einem Satz Schnüren bestand. Heutzutage findet das Wort "Code" im Computerbereich oft Verwendung als Kurzform des Ausdrucks "Source-Code" also Quelltext eines <a href="#15">Programms</a>.  
  
###<span id="overlay"><a href="#16" title="Next" >&darr;</a></span><a id="15"></a>Was ist ein Programm? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Das Bild das viele im Kopf haben wenn sie das Wort Programm hören ist stark durch Film beeinflusst. Wir sehen junge, meist übergewichtig und verpickelte Menschen vor uns die in abgedunkelten Räumen zwischen Monitoren, Kabeln und Pizzapackungen auf ewige grün leuchtende Zahlenkolonnen blicken die für uns keinerlei Sinn ergeben. Diese oder ähnliche Bilder sind inspiriert aus einer Zeit in der Computer nur einfarbige Pixel hatten und Grafische Benutzeroberflächen wie Windows noch aus der Kommandozeile gestartet wurde. Als Hommage an diese Vorstellung hat "Duiker101" das Programm [HackerTyper](http://hackertyper.net/) entworfen welches mit bereits vorgegebenem Text allein über Tastendruck den Bildschirm mit kompliziertem Quelltext füllt. Dabei ist es irrelevant welche Tasten der Benutzer drückt.
Verwerfen sie diese Vorstellung (Es ist nicht so das es dies nicht gibt dennoch entspricht es nicht der Regel). Ein Programm ist lt. [Duden](http://www.duden.de/rechtschreibung/Programm): "die nach einem Plan genau festgelegten Einzelheiten eines Vorhabens". Unter dieser Betrachtungsweise ist jede Bauanleitung zu Möbelstücken, eine Beschreibung des Weges von hier zum Bahnhof oder das Rezept für Sahnetörtchen ein Programm. Bloß das in letzterem Fall nicht ein Computer die Anweisungen ausführt sondern ein Mensch. Die Sprache in der dieses Programm geschrieben ist, ist Deutsch. Der grosse Unterschied zu einem Computersprache/-programm liegt hier ein der Möglichkeit der Interpretation. Die Ausführende "Maschine" (in diesem Fall der Mensch) kann solche Angaben wie "eine Priese Salz" oder "eine Messerspitze Meerrettich" verarbeiten. Ein Computer ist hierzu (noch) nicht fähig. Er bräuchte eine eindeutigere Angabe wie 50 Gramm. Das Programm sollte an dieser Stelle noch von dem Begriff des <a href="#16">Algorithmus</a> abgetrennt werden.  

###<span id="overlay"><a href="#17" title="Next" >&darr;</a></span><a id="16"></a>Was ist ein Algorithmus? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Auch wenn sich diese beiden Begriffe in ihrer Bedeutung teilweise überschneiden sollten sie auf folgende weise unterschieden werden. Der Algorithmus für Milch holen wäre in Pseudocode:  

	wenn (Aussage (kein Milch ist im Kühlschrank) wahr ist): hole neue Milch! wenn nicht: tue nichts!  

Das Programm für Milch holen würde voraussetzen das alle Schritte und Notwendigkeiten bis zum Übergang der Milch in das Eigentum der Holenden bekannt und definiert sind. Also so etwas wie:  

	Person fabian ist gleich neu Person;
	Kühlschrank Schrank ist gleich neuer Kühlschrank;
	Kühlschrank Menge Milch ist gleich 1;
	jeden morgen fabian trinke Milch aus Kühlschrank;
	Menge Milch reduziere um 0.2l;
	jeden morgen fabian beobachte Menge Milch;
	wenn Milch kleiner gleich 0.1 ist fabian hohle Milch im Supermarkt;

Und so weiter und so ähnlich. Diese Funktionsanweisungen könnten noch detaillierter ausgearbeitet werden. Hierbei sei zu beachten das solche Objekte wie Kühlschrank und Person bereits implementiert also bekannt sind. Das Programm im Vergleich zum Algorithmus muss alle eingesetzten Mittel kennen und oder selber beschreiben.  
  
###<span id="overlay"><a href="#18" title="Next" >&darr;</a></span><a id="17"></a>Was ist die Syntax? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Die Syntax ist die Form in der die Programmiersprache ausgestaltet ist. Die Syntax einer Programmiersprache besteht aus reservierten Worten wie zum Beispiel in Java `new, while, null , true,` Operatoren wie  `+,-,*,.` und Kontrollstrukturen wie `if(){}else{}` oder "`for(int i = 0; i < x;i++)`  
Lesen sie diese "Sätze" kurz. Wie würden sie es sprechen?  
  
Ausgesprochen wäre dies: ` For int i gleich 0, i kleiner x, i plus plus `

Es gibt in JavaScript eine Hand voll [reservierter Worte (Mozilla Developer Network)](https://developer.mozilla.org/en/JavaScript/Reference/Reserved_Words) die beim schreiben nicht verwendet werden dürfen.
{% highlight js %}
break, case, catch, continue, debugger, default, delete, do, else, finally, 
for, function, if, in, instanceof, new, return, switch, this, throw, try, typeof, 
var, void, while, with, null, false, true 
{% endhighlight %}
Noch einmal. Diese Worte dürfen nur für bestimmte Aufgaben verwendet werden! Wenn also ein Programmierer seine Variable `null` nennet, wird das Programm beim ausführen eine Fehler auswerfen. Die obig genannten Strukturen, Operatoren und reservierten Worte müssen erlernt werden. Eine vollständige Beschreibung aller würde jedoch den Rahmen dieser Arbeit sprengen.  
Weiterhin ist beim schreiben von Programmen auch auf die Groß- und Kleinschreibung zu achten. Eine Variable die mit dem Namen `myValue` initiiert wird muss auch mit diesem Namen aufgerufen werden. Bei einer falschen Schreibweise `MyValue` oder `myvalue` würde das Programm warnen, dass die aufgerufene Variable nicht existiert.  

{% highlight js %}
	var myValue = 5; // define a variable
	myvalue++; //edit it but written wrong
{% endhighlight %}

<br /> <a href="images/error_myvalue.png"> <img src="images/error_myvalue.png" width="100%" style="max-width:800px;" alt="" /></a>

Es gibt Sprachen die versuchen ihre Syntax so weit wie möglich an unseren Sprachen zu orientieren, zum Beispiel Applescript:

{% highlight applescript %}
	tell application "Safari" to activate
{% endhighlight %}

und wieder andere wie die esoterische Programmiersprache* "Brainfuck" die mit ihren acht Zeichen  

{% highlight bf %}
	+ - < > [ ] , .
{% endhighlight %}

voll funktionsfähig, aber nicht für das schreiben von Programmen gedacht ist sondern eher ein Gedankenmodell darstellt.
Das Brainfuck Hello World ([aus wiki](http://en.wikipedia.org/wiki/Brainfuck)):  

{% highlight bf %}
 	+++++ +++++             initialize counter (cell #0) to 10
 	[                       use loop to set the next four cells to 70/100/30/10
 	    > +++++ ++              add  7 to cell #1
 	    > +++++ +++++           add 10 to cell #2 
 	    > +++                   add  3 to cell #3
 	    > +                     add  1 to cell #4
 	    <<<< -                  decrement counter (cell #0)
 	]                   
 	> ++ .                  print 'H'
 	> + .                   print 'e'
 	+++++ ++ .              print 'l'
 	.                       print 'l'
 	+++ .                   print 'o'
 	> ++ .                  print ' '
 	<< +++++ +++++ +++++ .  print 'W'
 	> .                     print 'o'
 	+++ .                   print 'r'
 	----- - .               print 'l'
 	----- --- .             print 'd'
 	> + .                   print '!'
 	> .                     print '\n' 
 {% endhighlight %} 

Wie bereits oben in der Beschreibung des Milchalgorithmus zu sehen ist verwendet selbst Pseudocode ein nicht genau definierte Syntax lehnt sich jedoch mit Konstruktionen wie "ist gleich" an die Mathematik und Programmierung an. Andere Sprachen mit denen wir uns noch später Auseinandersetzen wie C++, Processing oder JavaScript sind zwischen diesen Extrema angesiedelt und vereinen in einer für das geübte Auge lesbaren und dennoch kompakte Art die Befehlsaufrufe.
  
###<span id="overlay"><a href="#19" title="Next" >&darr;</a></span><a id="18"></a>Was ist Pseudocode? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Im Verlaufe dieser Arbeit werde ich immer wieder auf die Darstellung von Algorithmen in "Pseudocode" zurückgreifen. Pseudocode besteht nicht aus einer bereits definierten Syntax und kann auch nicht von einem <a href="#19">Compiler</a> übersetzt werden sondern dient nur zur Darstellung eines logischen Ablaufs. Wie bereits in dem Milchalgorithmus zu sehen war versucht Pseudocode einen Programmablauf in menschenlesbarer Form darzustellen.  
  
###<span id="overlay"><a href="#20" title="Next" >&darr;</a></span><a id="19"></a>Was ist ein Compiler? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Der Vollständigkeit halber soll dieser hier erklärt werden auch wenn er uns kaum mehr im weiteren Verlauf der Arbeit begegnen wird. Der Compiler ist ebenfalls ein Programm das aus menschenlesbaren Hochsprachen wie zum Beispiel C++ maschinenlesbaren Quelltext erzeugt (Assemblercode). Diesen Prozess bezeichnet man auch als Kompilierung.  
  
###<span id="overlay"><a href="#21" title="Next" >&darr;</a></span><a id="20"></a>Was ist eine IDE (Integrated Development Envoirement)? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Um Quelltext zu schreiben bedarf es nicht viel. Ein einfacher Texteditor reicht aus um komplette Programme zu schreiben. Im Laufe der Zeit wurde jedoch viel Software programmiert um das schreiben von Quelltext zu erleichtern. Dies geht los bei einfachem Syntax-Highlighting bis hinzu kompletten Entwicklungsumgebungen die noch vor dem Kompilieren beziehungsweise während des Schreibens die Syntax auf ihre Validität prüfen und gegebenenfalls Vorschläge machen was gemeint sein könnte oder bei nicht verwendeten Programmteilen warnen das diese derzeit unnütz sind. In unserem Fall-Beispiel werden wir noch mit diesen Programmen zu tuen kriegen. Es sei jedoch bereits gesagt das wir die einfachste Möglichkeit nutzen werden die sich uns bietet und die auf beiden Plattformen (Windows und Mac OS X) zur Verfügung steht. Das ExtendScript Toolkit.  

###<span id="overlay"><a href="#22" title="Next" >&darr;</a></span><a id="21"></a>Was ist Hello World? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span> 
Das "Hello World" Programm hat sich als Standard Beispiel etabliert um die Syntax einer Sprache zu erklären. Exerzieren wir das einmal kurz durch. Um für Adobe InDesign, After Effects, Illustrator, Photoshop, Photoshop Elements, Photoshop Elements Organizer, Bridge, Audition, Media Encoder und Premiere Pro Skripte zu schreiben liefert Adobe eine eigene <a href="#20">IDE, eine Integrierte Entwicklung Umgebung</a>, mit.  
<br /> <a href="images/estk.png"> <img src="images/estk.png" width="100%" alt="" /></a>
Das ExtendScript Toolkit. Dies ist nicht der schönste Editor. Er hat jedoch einige Vorteile die die Entwicklung von Skripten sehr einfach macht. Die wichtigste Eigenschaft ist dabei folgende. Es kann ein Skript ohne es zu speichern ausführen. Das Toolkit wird bei der Installation von Adobe Produkten direkt mit geliefert. Suchen sie es in ihren Dienstprogrammen dort sollten sie fündig werden. Wenn nicht gehen sie zu dieser Webseite [http://www.adobe.com/devnet/scripting.html](http://www.adobe.com/devnet/scripting.html), laden und installieren sie es.  
Wenn es dann installiert ist geben sie folgende Text ein:  

{% highlight js %}
	alert("Hello World");
{% endhighlight %}

und drücken sie auf den "Play/Run" Knopf oben rechts oder drücken sie CMD-r oder CTRL-r, abhängig von ihrer Platform.  
<br /> <a href="images/hello_world.png"> <img src="images/hello_world.png" width="100%" alt="" /></a>

Herzlichen Glückwunsch. Ihr erstes JavaScript.  
Um dieses Skript in InDesign oder Photoshop auszuführen muss die Ziel Applikation aus dem PullDown Menü auf der oberen Leiste gewählt werden. Beim öffnen ist es auf ExtendScript Toolkit gestellt. Wählen sie dort InDesign aus. Das Toolkit wird sofort fragen ob InDesign auch gestartet werden soll. Bestätigen sie das und führen sie das Skript noch einmal aus. Sie werden sehen, dass der Computer zu InDesign überwechselt und den gleichen Hinweis gibt.  
Probieren sie weiter Skripte und Kalkulationen aus. Zum Beispiel  

{% highlight js %}
 	var h = "Hello";
 	var w = "World";
 	var calc = (10*50)/23 - 1;
 	alert(h + " " + w +"! Your result is: "+ calc ); 
 {% endhighlight %} 
  


  
###<span id="overlay"><a href="#23" title="Next" >&darr;</a></span><a id="22"></a>Was ist Syntax-Highlighting? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
<br /> <a href="images/syntax_highlite.png"><img src="images/syntax_highlite.png" width="100%" alt="" /></a>

Syntax-Highlighting ist eine Hilfestellung für Programmierer um ihren Quelltext übersichtlicher zu gestalten. Hierbei werden bestimmte Teile wie Operatoren, Kommentare, Funktionsdeklarationen oder Reservierte Worte farblich hervorgehoben beziehungsweise zurückgenommen um das Lesen zu erleichtern.  
  
###<span id="overlay"><a href="#24" title="Next" >&darr;</a></span><a id="23"></a>Was ist eine API (Application Programming Interface)? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Dies ist die Schnittstelle die ein Programm bietet um auf sein Funktionen zugreifen zu können. Dies wird beim Schreiben von Programmen wie InDesign von den Programmierern definiert. Diese Schnittstelle ist wie ein Baum mit Querverweisen aufgebaut. Um in InDesign einem bestehendem Dokument auf der ersten Seite eine Textbox hinzuzufügen muss durch diesen Baum manövriert werden.  

	app.activeDocument.pages.item(0).textFrames.add();

Diese Zeile erzeugt in der linken oberen Ecken eine Textkiste.  
All diese Befehle und Eigenschaften müssen nicht auswendig gelernt werden sondern können nachgeschlagen werden. Im ExtendScript Toolkit kann unter Hilfe / ObjektModell Viewer ein Hilfsprogramm aufgerufen werden das alle Befehle mit einer kurzen Erklärung enthält. Oder es kann auf der Seite von jongware eine .chm Datei heruntergeladen werden die die gleichen Informationen enthält und mit einem .chm Viewer durchsucht werden kann. [http://www.jongware.com/idjshelp.html](http://www.jongware.com/idjshelp.html)  
  
###<span id="overlay"><a href="#25" title="Next" >&darr;</a></span><a id="24"></a>Was ist Objektorientierung? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Als Objektorientierung (ach als OO abgekürzt) versteht man ein bestimmte Art wie Programme aufgebaut sind. Ein Objekt ist ein gekapselter Teil des Programmcodes der Schnittstellen und Methoden bietet und seine Eigenschaften an weiter Objekte vererben kann. Um dies besser zu verstehen möchte ein hervorragendes Beispiel aus "Processing: A Programming Handbook for Visual Designers and Artists" von Casey Reas and Ben Fry bemühen.  
####Klammer auf!
	{  

Der Proto-Apfel hat bestimmte Eigenschaften wie Gewicht und Farbe. Hinzu kommen bestimmte Methoden wie Fallen, Wachsen und Verrotten die durch die Eigenschaften beeinflusste werden können. <a href="#" class="show_hide" rel="#slidingDiv10">[?]</a><div id="slidingDiv10">Der Proto-Apfel existiert eigentlich nicht. Unsere Sprache lässt solche Ungenauigkeiten zu. Es gibt einen Apfel und einen Anderen. Aber nicht "DEN" Apfel.</div>  
<br /> <a href="images/object_orientation_classes-1.png"><img src="images/object_orientation_classes-1.png" width="100%" alt="" /></a>
 Wenn nun ein Baum wächst und Äpfel produziert erzeugt er nach dem Bauplan des Proto-Apfels neue Äpfel und jedem werden bestimmte Werte übergeben.  
<br /> <a href="images/object_orientation_classes-2.png"><img src="images/object_orientation_classes-2.png" width="100%" alt="" /></a>
Der Baum erzeugt den Apfel und ruft kontinuierlich die Methode Wachsen auf. Hierbei wird der Wert des Gewichtes inkrementiert. Sind die Früchte dann reif wird abhängig vom Gewicht des einzelnen Apfels die Methode Fallen ausgelöst. Wenn der Apfel dann auf dem Boden liegt und die Methode Fallen beendet ist beginnt die Methode Verrotten ihre Arbeit. Die Farbe des Apfels verändert sich und das Gewicht wird wieder verringert.
Das bedeutet der Proto-Apfel selber wird nicht angerührt sondern Instanzen von diesem. Um dies noch auf die Spitze zu treiben haben wir nicht nur eine Art Apfel sondern verschieden Sorten. Also ist die Klasse Granny Smith und ein "Kind"-Klasse der Basisklasse Apfel. Granny Smith erbt alle Eigenschaften der Klasse Apfel ohne das sie neu implementiert werden müssen und bekommt noch eine weitere Eigenschaft: den Namen.

	} // Klammer zu.  
Dieses Konstruktionsweise spiegelt sich in nicht nur in der Programmierung wieder. Die Benutzung einiger Komponenten in unseren Werkzeugen ist genau nach diesem Prinzip organisiert.
####Eine weiter Klammer auf   

	{

In InDesign hat der Benutzer die Möglichkeit Absatz- und Zeichenformate anzulegen ohne die das setzen eines Buches eine wirklich Zeitraubende Angelegenheit wäre. Eine einfache Gruppe von Absatzformaten kann wie folgt aufgebaut sein.  
- [Einfacher Absatz]  
- TextKörper  
- Überschrift 1  
- Überschrift 2  
- Überschrift 3  
- Bild Unterschrift  
- Pagina  
In dem Format "[Einfacher Absatz]" wird eine Schriftart und eine Schriftgrösse definiert. Dieses Format ist das Proto-Format von dem sich alle weiteren Formate ableiten. Sie erben also alle die Eigenschaften Schrift (appliedFont) und die Schriftgrösse (pointSize). Das Format "Überschrift 1" (Ü1) bekommt dann eine eigene Schriftgrösse und einen fetten Schnitt der Schriftart. Im dem Format "Überschrift 2" (Ü2) wird dann festgelegt das nicht mehr das "[Einfacher Absatz]" Format als Basis Klasse benutzt wird sondern Ü1. Damit erbt Ü2 alle Eigenschaften von Ü1. In Ü2 wird dann nur noch eine neue Schriftgrösse festgelegt. Das gleiche kann dann mit "Überschrift 3" (Ü3) passieren. Ü3 basiert auf Ü2 und bekommt ebenfalls eine eigene Schriftgrösse. Jetzt basiert Ü3 auf Ü2, das auf Ü1 und das auf "[Einfacher Absatz]". Ähnlich verfahren wir mit den weiteren Formaten. "Textkörper" basiert auf "[Einfacher Absatz]", "Bildunterschrift" auf "Textkörper" nur kleiner und "Pagina" auf "Bildunterschrift" aber mit 70% Deckkraft. Wenn der Gestalter nun entscheidet dass eine andere Schriftart von Nöten ist, ändert er sie nur in "[Einfacher Absatz]" und alle Kinder werden entsprechend angepasst. Dies ist ebenfalls Objektorientiert.  
<br /> <a href="images/id_formate.png"><img src="images/id_formate.png" width="100%" alt="" /></a>

	} // Klammer zu
  
###<span id="overlay"><a href="#26" title="Next" >&darr;</a></span><a id="25"></a>Was sind Funktionen/Methoden? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Eine Funktion oder eine Methode sind gekapselte Programmteile and die Parameter übergeben werden können und die an den gegebenen Parametern eine Kalkulation durchführen. Sie können dann Werte zurückgeben. Dies ist nützlich wenn bestimmte Tätigkeiten an unterschiedlichen Positionen eins Programms oder Skripts mehrmals aufgerufen werden müssen.     
###<span id="overlay"><a href="#27" title="Next" >&darr;</a></span><a id="26"></a>Was ist ein Bug? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Ein Bug ist ein Fehler der das Programm von seiner einwandfreien Ausführung abhält. Dies kann nur ein Rechenfehler sein oder ein Fehler der das gesamte Programm zum Absturz bringt.  
  
###<span id="overlay"><a href="#28" title="Next" >&darr;</a></span><a id="27"></a>Was ist Debugging? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Dies ist der Prozess des Finden und korrigieren von Fehlern.  

###<span id="overlay"><a href="#29" title="Next" >&darr;</a></span><a id="28"></a>Was ist ein Workaround? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  
Ein Workaround ist eine kreative Lösung um ein Problem zu umgehen. Wenn zum Beispiel eine API ein bestimmte Funktion nicht anbietet muss ein Weg um dieses Problem drumherum gefunden werden. 
  
###<span id="overlay"><a href="#30" title="Next" >&darr;</a></span><a id="29"></a>Welche Konventionen gibt es? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
Neben den Bestimmungen der Syntax gibt es verschiedene Konventionen die das lesen von Skripten einfacher machen sollen. Zum Beispiel ist es gang und gebe dass die Funktionsweise am Beginn eines Skripts in einem Kommentar erklärt wird. Oder die Verwendung der Variable i (für Iterator) als Zähler in Schleifen.

###<span id="overlay"><a href="#31" title="Next" >&darr;</a></span><a id="30"></a>Herkunft von JavaScript <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
JavaScript orientiert sich in seiner Syntax an C und C++. 
Zur Veranschaulichung was dies bedeutet hier ein Programm das folgende Aufgaben erledigt.  

- Zwei Zahlen  in Variablen definieren
- Ein Objekt mit folgenden 3 Eigenschaften erzeugen  
- Einem Namen  
- Einer Funktion die 2 Zahlen mit einander vergleicht und feststellt welche die grössere von beiden ist.  
- Eine Ergebnis zurück geben  
- Einen Satz aus allen Variablen zusammenstellen
- Diesen Satz darstellen
  
Dieses Programm liegt hier in verschiedenen Sprachen vor.  
Ich werde hier kurz auf kleine Unterschiede eingehen und versuchen an diesen 3 Beispielen zu erläutern warum JavaScript eine einfach und mächtige Sprache ist. An dieser Stelle ist es nicht zwingend den Programmcode komplett zu verstehen. Beachten sie nur die syntaktischen Unterschiede. Vergleichen sie die Funktion oder Methode `int Object::compare(int a, int b)` in C++ mit `int compare(int a, int b)` in C und betrachten sie danach die Funktion / Objekt `compare : function(a,b){if(a>b){return a;}else{return b;}` in JavaScript. Es gibt kleine Unterschiede aber die gemeinsame Herkunft ist unübersehbar. Eine tiefere Erklärung des Quelltextes findet sich in den Kommentaren der einzelnen Programme und des Skriptes.  

####Assembler (anObject.s)
Dies ist die Variante die die Maschine versteht. Es wurde jedoch nicht von mir geschrieben sondern ist das Ergebnis des Kompilierungs-Prozesses des C++ Programms. Näher wäre nur noch Nullen und Einsen zu schrieben. Ich drucke dies hier der Vollständigkeit halber ab. Ja - es gibt auch diesen Aspekt der Programmierung der genau dem entspricht was Menschen davon abhält sich mit ihr auseinander zu setzen. Um dort an zu gelangen ist es ein weiter Weg den wenige gehen und auch wir nicht beschreiten werden in dieser Arbeit. Aus Platzgründen werde ich hier nur die ersten 29 Zeilen zeigen. Das gesamte Programm in Assembler Code ist über 700 Zeilen lang und ist im Download Packet enthalten.  

{% highlight cpp-objdump %}
		.section	__TEXT,__text,regular,pure_instructions
		.globl	__ZN6Object7compareEii
		.align	1, 0x90
	__ZN6Object7compareEii:
	Leh_func_begin1:
		pushq	%rbp
	Ltmp0:
		movq	%rsp, %rbp
	Ltmp1:
		movq	%rdi, -8(%rbp)
		movl	%esi, -12(%rbp)
		movl	%edx, -16(%rbp)
		movl	-12(%rbp), %eax
		movl	-16(%rbp), %ecx
		cmpl	%ecx, %eax
		jle	LBB1_2
		movl	-12(%rbp), %eax
		movl	%eax, -24(%rbp)
		jmp	LBB1_3
	LBB1_2:
		movl	-16(%rbp), %eax
		movl	%eax, -24(%rbp)
	LBB1_3:
		movl	-24(%rbp), %eax
		movl	%eax, -20(%rbp)
		movl	-20(%rbp), %eax
		popq	%rbp
		ret
	Leh_func_end1:
{% endhighlight %}
(…)  

Gruselig oder nicht? Zu unserem Glück müssen wir so etwas weder schreiben noch lesen können. Von 1969 bis 1973 würde die Sprache C von Dennis Ritchie ( Quelle The C Programming Language von Brian W. Kernighan & Dennis Ritchie) im "Bell Labs Computing Sciences Research Center" entwickelt. Diese Sprache wird beim Kompilieren in Assembler Code übersetzt. Der Vorteil dabei ist eine viel einfachere Syntax die es erlaubt den Schwerpunkt der Aufmerksamkeit auf das Konzept des Programms zu richten.   

####ANSI C noObject.c  
Im Unterschied zu C++ und JavaScript ist die Sprache C nicht für eine Objektorientierung ausgelegt. Deshalb hier einmal das Beispiel noObject.c welches die gestellte Aufgabe des Vergleich löst aber kein Objekt erzeugt. Die Syntax ähnelt hier sehr der von JavaScript. Sobald jedoch Pointer hinzukommen wird es schwer kompliziert.

Aber ich schweife ab. Keine Sorge mit Problemen wie: "In welchem Speicher lege ich meine Variable ab" und "Habe ich auch den Müll rausgetragen" (Das löschen eines unbenutzten Objekts wird "Garbadge Collection" also "Müll sammeln" genannt), werden wir in JavaScript nicht konfrontiert. All diese Funktionalität wird von der Maschine im Hintergrund erledigt. Somit bleibt Zeit sich mit der Funktionsweise und Konzept zu beschäftigen. Stellen sie es sich vor wie es wäre entweder das Auto vor dem Fahren zusammen zu bauen oder einfach in das fertige Auto einzusteigen und loszufahren." Um die Abstammung von JavaScript verstehen zu können habe ich die Vergleichs-Funktion in C geschrieben.
{% highlight c %}
// include the io lib
#include<stdio.h>
// the compare function takes integer as arguments 
int compare(int a, int b){
	if(a>b){return a;}else{return b;}
}
// the main function
int main(void){
	char name[11] = "Hello World"; // our string
	int a = 23,b = 5; // the values to compare
	// now print all that stuff
	// with %s you insert string arguments
	// with %d digits 
	printf("The Object named: %s\nCompared: %d with %d.\n%d is bigger!",name,a,b,compare(a,b));

	return 0;// everything went fine return 0
}
{% endhighlight %}  

<br /> <a href="images/terminal_c_cpp.png"><img src="images/terminal_c_cpp.png" width="100%" alt="" /></a>
####C++ (anObject.cpp)  
Basierend auf C wurde Ende der Siebziger Anfang der Achtziger Jahre des letzten Jahrtausends die Sprache C++ von Bjarne Stroustrup in den AT&T Labs entwickelt (Quelle: Bjarne\_Stroustrup\_-\_The\_C++\_Programming\_Language\_3rd\_Ed [online](http://www.ib.cnea.gov.ar/~oop/biblio/Bjarne_Stroustrup_-_The_C++_Programming_Language_3rd_Ed.pdf)). Diese Sprache ist nach dem Konzept der Objektorientierung (OO) aufgebaut. In diesem Beispiel ist bereits zu sehen, dass die Menge an Code die geschrieben werden muss geringer wird (im Vergleich zum Assembler Code). Wobei hier wie auch im C Beispiel bedacht werden muss, dass bereits vorhandene Programmteile mit weiteren hunderten oder tausenden Zeilen Code hinzugefügt werden. <a href="#" class="show_hide" rel="#slidingDiv8">[?]</a><div id="slidingDiv8"> OO hat den Vorteil des Versteckens beziehungsweise Kapseln von Daten. Es kommt die Klasse hinzu. Sie erlaubt ganze Programmteile auszulagern und nur einen Schnittstille für ihre Benutzung zu liefern. Für genauere Erklärungen lesen sie den Abschnitt <a href="#24">7.11 Was ist Objektorientierung?</a></div>  

{% highlight cpp %}
#include <iostream>
#include <string> 
 {% endhighlight %} 
  
Mit den obigen 2 Zeilen werden fertige Klassen eingebunden. "iostream" um die Ein- und Ausgabe des Programms zu handhaben und "string" um Zeichenketten zu verarbeiten. Der Unterschied ist enorm. Während in C eine Zeichenkette noch eine Liste einzelner Zeichen ist wird in C++ ein Zeichenkette als ein einziges Objekt gehandhabt und bringt viele Funktionen mit zur Verarbeitung dieser.  

{% highlight cpp %}

// the string and io classes
#include <iostream>
#include <string>

//using namespace std; // if you use this you can remove all "std::"
class Object{ /* our object*/
public:
	std::string name; // its name

	Object(){}// basis constructor
	Object(std::string in){name = in;}// another constructor
	int compare(int a, int b);//Prototype for comparsion
	void setName(std::string in){name = in;} // to set the name
};

int Object::compare(int a, int b){/* the compare function*/
	if(a>b){return a;}else{return b;}
}

int main(){ /* now the main program*/
	Object* myObject = new Object("Hello World CPP");// make a new object

	int a = 23,b = 5;// declare some values
	// now the output directly with comparsion
	std::cout << "The Object named: "<< 
	myObject->name << "\nCompared: "
	<< a << " with "
	<< b << "\n" 
	<< myObject->compare(a,b) <<" is bigger\n" 
	<< std::endl;
	/* code */
	delete myObject; // remove the object from memory
	return 0; // everything went fine return 0
}
{% endhighlight %}
<br />
####JavaScript (anObject.js)  
Im Jahre 1995 wurde die Sprache LiveScript zusammen mit der 2.0 Version von Netscape (ein WEb-Browser) veröffentlicht und bald in JavaScript umbenannt (Quelle: JavaScript das Umfassende Handbuch). Wie in jedem Buch das sich mit JavaScript auseinandersetzt möchte auch ich hier sagen und es dabei belassen:  
######Java is to JavaScript like ham to hamster  
Mit JavaScript gehen wir einen Schritt weiter als in C++. Hier sind das Objekt, die Ein-/Ausgabe, der String bereits existent und müssen nicht neu implementiert noch eingebunden werden. Genau genommen ist in JavaScript fast alles ein Objekt. Der massgebende Unterschied ist dass die vorherigen Programme wirklich vollwertige Programme sind die nach dem Kompilieren aus der Kommandozeile ausgeführt werden können. Die JavaScript Variante benötigt ein Programm in dem es ausgeführt wird. Es ist also alleine nicht lauffähig. Dennoch - was wir in C++ in 8 Zeilen schreiben hat in JavaScript nur noch 4 Zeilen.

{% highlight js %}
main(); // call the main function

function main(){ /* here wee go */

    var obj = buildNewObject("Hello JS"); // create a new Object
    var a = 23, b = 5; // define the values
    obj.compare(a,b); // let the object compare the values
    // and make the message
    alert("The Script named: "+ obj.name + 
          "\nCompared: "+ a +" with "+ b +"\n" 
          + obj.result + " is bigger\n");
    obj = null; // delete the object
    return 0; // everything went fine return 0
};

function buildNewObject(n){/* this is our object builder*/
    var obj = { /* create a json object*/
    name:n, /* its name is the incoming value*/
    result:0, /* this will be set by the compare object*/
    compare : function(a,b){if(a>b){this.result = a;}else if(a<b){this.result = b;}}
    };
    return obj; // return the new object
};
{% endhighlight %}
<br /> <a href="images/estk_anobjectjs.png"><img src="images/estk_anobjectjs.png" width="100%" alt="" /></a>
Werfen sie einen Blick auf die Funktion `buildNewObject(n)`.
Dies ist eine kleine Abwandlung der `compare` Funktion die wir in der C++ Variante sehen. Die verbesserte Funktion kann die gegebenen Variablen vergleichen und in sich selber mit `this.result` das Ergebnis festlegen. Um eine solche Funktionalität in einer C++ zu erzeugen bedürfte es einiger Zeilen mehr.
Ohne diese Erweiterung und ohne das Objekt würde das JavaScript es wieder der C Variante ähneln.

{% highlight js %}
main();  
function main(){
   	var a = 23, b = 5;
   	var name = "Hello JS";
   	var result = compare(a,b);
       	alert("The Script named: "+ name +"\nCompared: "
       		  + a +" with "+ b +"\n" + result + " is bigger\n");
   	}
function compare (a,b){
   	if(a>b){
       	return  a;
       	}else{
       	return  b;
   	};
};
{% endhighlight %}
<br /> <a href="images/estk_noobjectjs.png"><img src="images/estk_noobjectjs.png" width="100%" alt="" /></a>


###<span id="overlay"><a href="#32" title="Next" >&darr;</a></span><a id="31"></a>Was ist der Unterschied zwischen JavaScript und ExtendScript? <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
JavaScript oder EcmaScript ist das was uns täglich in Webbrowsern solche Dinge bescherte wie Scrollen auf Knopfdruck oder Warnhinweise und ähnliches. ExtendScript ist ein Dialekt von JavaScript der von Adobe entwickelt wurde. Das bedeutet InDesign versteht JavaScript und ExtendScript aber ein Browser kann mit ExtendScript Befehlen nichts anfangen.  

###<span id="overlay"><a href="#34" title="Next" >&darr;</a></span><a id="32"></a>Was sind Pointer <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>  
Ein Pointer ist der Verwies auf die Adresse unter der eine Variable abgelegt. Dies verweist auf von der Variable okkupierten Speicher. Das kann dann so aussehen:
{% highlight c %}
double *dp, atof(char *);
{% endhighlight %}

>says that in an expression *dp and atof(s) have values of double, and that the argument of atof is a pointer to char.  

> aus The C programming Language By Brian W. Kernighan and Dennis M. Ritchie. Published by Prentice-Hall in 1988
([online]( http://net.pku.edu.cn/~course/cs101/2008/resource/The_C_Programming_Language.pdf))

<br>
##<span id="overlay"><a href="#35" title="Next" >&darr;</a></span><a id="34">8 Refenrenzen</a> <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
<br>
##<span id="overlay"><a href="#36" title="Next" >&darr;</a></span><a id="35">9 Weblinks</a> <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>
<br>
##<a id="#36">10 Quellen</a> <span id="overlay"><a href="#top" title="Back to Index" >&uarr;</a></span>