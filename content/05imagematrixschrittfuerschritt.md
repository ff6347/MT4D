---
layout: twbsoffline
title: Image Matrix Schritt fuer Schritt
bodyid: usage
---

<a name="09"></a>
###3.2 image matrix - Schritt für Schritt.  
Ein Skript sollte immer in geschwungenen Klammern eingefasst sein. Dies ist nicht zwingend notwendig, jedoch nützlich, falls das Skript von einem anderem Skript evaluiert werden muss. Innerhalb dieser Klammern folgt der gesamte Quelltext.  

	{}

Als nächstes definieren wir eine Funktion, die einmalig aufgerufen wird. Hierbei ist es irrelevant, ob der Aufruf vor oder nach der Funktionsdefinition stattfindet. Aus Gründen der Übersichtlichkeit steht hier der Aufruf vor der Definition. Diese Funktion erhält keine Parameter. Später wird auch eine Funktion mit Parametern eingesetzt. Der Zweck, den gesamten Code in einer Funktion zu kapseln, ist folgender: Wenn es eine hierarchisch höhere Ebene gibt, unsere Klammern `{}`, kann eine Funktion mit dem Befehl `return;` beendet werden. Dies ist nützlich, um bei Fehlern oder falscher Benutzereingabe die Ausführung zu stoppen. Mit dem Befehl `return` kann nicht nur eine Funktion beendet werden, sondern auch ein Wert zurückgeliefert werden.
Wenn wir am Ende einer Funktion `return 1;` schreiben, wäre das Ergebnis 1. `var myValue = main();` Wenn die Funktion `main` nun diesen Wert zurückgeben würde, wäre `myValue` 1. In unserem Fall benötigt die `main()` keinen Rückgabewert.

{% highlight js %}
{
main();
function main(){
	}
}
{% endhighlight %}

Wir befinden uns nun in der Funktion `main();`.  
Es folgt die Deklaration der ersten Variable. Sie beinhaltet die Breite (und Höhe) unserer Bilder.

{% highlight js %}
var w = 25;
{% endhighlight %}

Wie zu sehen ist, entspricht die Variable `w` (steht für width) nun 25. `w` wird im Verlauf des Skriptes mehrmals verwendet. Der Vorteil daran, Variablen zu verwenden, anstatt immer 25 zu schreiben ist, dass wenn wir die Breite verändern wollen, wir dies nur ein einziges mal an `w` erledigen müssen. Alle weiteren Verwendungen von `w` werden angepasst.  
Als nächstes folgt eine Subfunktion mit einem Parameter und einem Rückgabewert. In JavaScript werden alle Variablen mit `var` deklariert. Die Unterscheidung des Typus findet erst bei der Verwendung statt. Deshalb können wir schreiben:  

{% highlight js %}
var allImages = loadFiles("*.jpg");
{% endhighlight %}

Damit die Funktion auch vorhanden ist, fügen wir sie hinter `function main(){}` an. Unser Code sieht also wie folgt aus.  

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

Den Rückgabewert werden wir noch verändern, denn wir wollen Bilder laden und nicht `0`. Wie oben zu sehen ist, erhält `loadFiles` den Parameter `type`. Dies ist der Dateityp, der später geladen werden soll. `type` ist genau wie `w` und `allImages` eine Variable, nur dass wir im Parameterblock der Funktion das `var` weglassen können. Wenn wir `*.*` schreiben, würde unsere Funktion jeden Dateityp laden. Der Einfachheit halber beschränken wir uns auf .jpg, da wir wissen, dass InDesign .jpg-Dateien laden und platzieren kann.  
Als nächstes begeben wir uns in die Funktion `loadFiles` und betrachten die Dateihandhabung und eine Benutzerinteraktion. Basierend auf dem Ergebnis der Interaktion fällt das Skript eine konditionale Entscheidung, ob es weiter arbeiten soll oder ob es die Funktion `loadFiles` beendet.  

	{% highlight js %}
	var theFolder = Folder.selectDialog ("Choose the Folder");
	if(!theFolder){ 
			return;
			};
	{% endhighlight %}

Bisher waren alle Befehle JavaScript Befehle. Der Befehl `Folder.selectDialog ("Choose the Folder")` jedoch ist [ExtendScript](10terminologie.html#31). Das Objekt `Folder` hat eine eigene Funktion `selectDialog(parameter)`. Wir müssen diese Funktion nicht betrachten. Wir müssen nur wissen, dass sie ein Interface öffnet und dem Benutzer die Möglichkeit gibt, einen beliebigen Ordner auszuwählen. Der Parameter ist der Text, der auf dem Auswahldialog oben zu sehen ist. Der gewählte Ordner wird dann in der neuen Variable `theFolder` für eine spätere Referenzierung gespeichert. Dann folgt das Konstrukt der konditionalen Abfrage.

	{% highlight js %}
	if( Statement ){ doSomething }
	{% endhighlight %}

Sie besagt, dass, wenn die Aussage in der runden Klammer wahr ist, die geschwungene Klammer ausgeführt wird. In unserem Fall wird durch das `!` die Aussage negiert. Ausgeschrieben könnte dort stehen `if(theFolder == false)` oder `if(theFolder != true)`. Die Schreibweise `if(!theFolder)` ist lediglich verkürzt. Wenn wir `if(theFolder)` schreiben, würde das `if(theFolder==true)` entsprechen. Zu beachten ist nicht `=` zu schreiben. Dies bedeutet "wird zu", `==` bedeutet "entspricht". `=` ist eine Zuweisung von Werten, `==` ist ein Vergleich. Der Vollständigkeit halber soll noch erwähnt werden, dass es noch eine weitere Form gibt. Der typsichere Vergleich mit `===`, den wir jedoch nicht weiter betrachten wollen. Gesprochen wäre die obere Aussage: "Wenn der Ordner nicht existiert - beende die Funktion".  
Als nächstes betrachten wir was das Laden der Dateien aus unserem Ordner.  

	{% highlight js %}
	var allImages = theFolder.getFiles(type);
	{% endhighlight %}

Ordnerobjekte (`Folder`) haben eine weiter eingebaute Funktion: `getFiles(parameter)`. Diese hat auch einen Parameter: den Dateityp. Hierbei wird nicht nur eine einzelne Datei zurückgegeben, sondern eine Sammlung aller Dateien des angegebenen Typs. Dies ist ein Array. Ein Array sollte man sich als eine Liste vorstellen, deren Positionen über einen Index aufgerufen werden können. An dieser Stelle ist zu beachten, dass das erste Objekt in der Liste nicht mit 1 sondern mit 0 angesprochen wird. Also ist `allImages[0]` das erste Bild unserer Liste.  
Nun folgt ein weiterer Sicherheitscheck, ob wir Bilder gefunden haben und die Bestimmung des Rückgabewerts unserer Funktion. Ebenfalls wird der Nutzer, wenn es keine Bilder, gibt darauf hingewiesen.

	{% highlight js %}
	if((allImages.length < 1) || (allImages == null) ){
		alert("There are no images of the type: " + type);
		return null;	   
	}else{
		return allImages;
	};
	{% endhighlight %}

Wie wir oben sehen, benutzen wir nochmals die konditionale Entscheidung `if()`, jedoch mit einer Erweiterung, dem `else`. Dies bedeutet, dass auf jeden Fall einer der beiden Blöcke ausgeführt wird. Um es im <a href="10terminologie.html#18">Pseudocode</a> darzustellen:  

	{% highlight text %}
	Wenn die Aussage zutrifft mach dies ansonsten mach dass
	{% endhighlight %}

Innerhalb unsere runden Aussageklammer haben wir mehrere Bedinungen verknüpft. Wir haben also zwei Aussagen. Mit dem `||` werden mehrere Aussagen geprüft. In unserem Fall ist das einmal der Check, ob wir mindestens ein Bild haben `(allImages.length < 1)`. `length` ist eine Eigenschaft jedes Arrays und gibt, wenn wir ein Bild haben 1 zurück. Wir fragen, ob die Länge von unserer Liste kleiner als 1 ist. Diese Aussage verbinden wir mit `||`, dies bedeutet "oder". Wenn Aussage 1 oder Aussage 2 zutrifft, führe den ersten Block aus. Wenn beide Aussagen wahr sein müssen, schreiben wir dafür `&&`. Dies würde nur den ersten Block ausführen, wenn beide Aussagen zutreffen. In unserer zweiten Aussage fragen wir nach `null`, dies entspricht "nichts". Wenn wir einen Fehler beim Laden der Bilder hatten oder `allImages` nicht existiert, dann brich die Ausführung ab. Im ersten Block wird die Funktion beendet. Wenn eine der beiden Aussagen zutrifft, wird mit `return allImages` eine Liste mit Bildreferenzen an die Funktion `main` zurückgegeben.  
  
Wir befinden uns wieder in der Funktion `main` und werden eine weitere Abfrage starten.

	{% highlight js %}
	if(allImages == null) return;
	{% endhighlight %}

Wenn `loadImages` `null` zurück gibt, bricht das Skript ab. Dies ist nötig, da `loadImages` in der Funktion `main` stattfindet. Also führt ein `return` in `loadImages` nur zurück nach `main` und nicht zum Beenden des Skripts. Hier ist ebenfalls eine verkürzte Schreibweise zu sehen. Die geschwungenen Klammern können bei nur einem einzigen Folgebefehl weggelassen werden. Das heißt:  

	{% highlight js %}
	if(statement){doSomething;} 
	{% endhighlight %}

entspricht:  

	{% highlight js %}
	if(statement) doSomething;
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

Als nächstes folgt die Berechnung unserer Seitenbreite und Seitenhöhe. Die Höhe wird nochmals mit einer Kondition überprüft. Wenn die Menge an Bildern nicht in eine Matrix passt, also nicht 3 × 3, 4 × 4 oder 100 × 100 ist, muss die Höhe nochmals um eine Zeile erweitert werden. Hier kommt das JavaScript Objekt `Math` zum Einsatz.   

	{% highlight js %}
	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2);
	var ph = pw;
	if(Math.round(Math.sqrt(allImages.length)) != Math.sqrt(allImages.length)){
	        ph = pw + w;
	}
	{% endhighlight %}

Dies wirkt kompliziert. Um es zu verstehen, lösen wir den ersten Satz einmal auf. Betrachten sie dabei das Bild.  

[![matrix 4 mal 4](images/matrix_think_thumb.jpg)](images/matrix_think.jpg)  

{% highlight text %}
a ist gleich 16. Die Menge an Bildern.  
b ist die Wurzel aus a. Wir wollen es rechteckig. Also 4.  
c ist b gerundet. Falls es eine Fließkommazahl ist.
c bleibt in diesem Fall 4, wenn a 16 ist.
d ist 25. Die Breite der Bilder.  
e ist c mal d.
Wir staffeln die Bilder nach rechts. 4 × 25 also 100.  
f ist d mal 2. Das ist der linke und rechte Abstand zum Seitenrand. Jeweils eine Bildbreite. Also 50.
{% endhighlight %} 

Daraus ergibt sich eine Seitenbreite von 150.  

Die Breite der Bilder multipliziert mit der auf- oder abgerundeten Wurzel aus der Menge an Bildern plus eine Bildbreite links und eine rechts. (Lesen sie den vorherigen Satz nochmals und versuchen sie sich ein geistiges Bild von der Berechnung zu machen.)  

oder  

	{% highlight text %}
	g = [√a] × d + (d × 2) 
	{% endhighlight %} 

oder  

	{% highlight js %}
	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2);  
	{% endhighlight %}

Danach setzen wir mit `var ph = pw;` die Höhe der Seite der Breite gleich. Für den Fall, dass `b` (oder `Math.sqrt(allImages.length)`) eine Fließkommazahl ist und wir eine nicht quadratische Matrix erzeugen, also alle Bilder platziert werden sollen, müssen wir die Höhe der Seite um eine Zeile für Bilder erweitern. Deshalb wird in dem `if(statement)` verglichen, ob die gerundete Quadratwurzel nicht der Quadratwurzel entspricht.  

	{% highlight js %}
	(Math.round(Math.sqrt(allImages.length)) != Math.sqrt(allImages.length)
	{% endhighlight %}

oder  

	{% highlight text %}
	[√a] ≠ √a  
	{% endhighlight %}

oder  
<br>  
Wenn die Wurzel aus der Menge an Bildern nicht der gerundeten Wurzel aus der Menge an Bildern entspricht, ist die Seitenhöhe die Seitenbreite plus eine Bildbreite. Wenn a also 17 ist wäre die Seite 150 breit und 175 hoch.  
  
Ich vermeide hier, um es nicht noch weiter zu verkomplizieren, jede Art von Maßeinheit. In der Standard-Einstellung in InDesign sind es Millimeter. Dies könnten wir definieren, müssen wir aber nicht, da InDesign immer eine Grundeinstellung hat.  
Als nächstes folgen das Erzeugen des Dokuments, das Einstellen der Seite auf unsere errechneten Werte, das Überführen der ersten Seite im Dokument in eine Variable und die Definition unseres Startpunktes `(x,y)`.  

	{% highlight js %}
	var doc = app.documents.add();
	    doc.documentPreferences.pageWidth = pw;
	    doc.documentPreferences.pageHeight = ph;
	var page = doc.pages.item(0);
	var y = w;
	var x = w;
	{% endhighlight %}

An dieser Stelle wird der Sammlung an Dokumenten ein neues hinzugefügt. Dabei ist irrelevant, ob bereits ein Dokument existiert. Dann stellen wir die Weite und Höhe der Seite ein. Danach nehmen wir aus der Sammlung an Seiten in dem neuem Dokument die Erste. Der Aufruf `item(0)` ist ebenfalls ein ExtendScript Befehl, der nur in InDesign funktioniert. Wir könnten auch `var page = doc.pages[0]` schreiben. Hier funktioniert beides gleich. Das ist jedoch nicht immer der Fall. Es gibt die Möglichkeit, `doc.pages.middleItem()` oder `doc.pages.lastItem()` abzufragen. Bei einem normalen Array wie unserem `allImages` würde `lastItem()` oder auch `item() nicht funktionieren. Danach erzeugen wir den linken, obere Koordinate unseres ersten Bildes. x und y sind jeweils eine Bildbreite vom Rand der Seite entfernt. Es gibt noch die Möglichkeit, die ersten drei Zeilen abzukürzen. Dies ist eine komprimiert Schreibweise, die uns noch öfter begegnen wird.  

	{% highlight js %}
	var doc = app.documents.add({documentPreferences:{pageWidth:pw,pageHeight:ph}});
	{% endhighlight %}

Aber zu dieser Schachtelung kommen wir noch. Wir sind bereits halb durch. Es folgt nochmals ein weiteres Konstrukt: die Schleife.  

	{% highlight js %}
	for(var i = 0; i < allImages.length;i++){
	var rect = page.rectangles.add({geometricBounds:[y, x, y + w,x + w]});
	rect.place(allImages[i] );
	rect.fit(FitOptions.FILL_PROPORTIONALLY);// fit it to the frame
	rect.fit(FitOptions.CENTER_CONTENT);// fit it to the frame
	x +=w;
	}
	{% endhighlight %}

Mit dieser Schleife würden wir nur Bilder weiter nach rechts setzen. Den "Zeilenumbruch" fügen wir später ein. Die Aussage der Schleife ähnelt der Kondition `for(statment){doSomething}` nur mit `for` anstatt `if`. Es könnte als an _solange_ übersetzt werden. Solange der Zähler kleiner als die Menge an Bildern in der Liste ist, führe etwas aus.  
Die Aussage `for(var i = 0; i < allImages.length; i++ )` ist  eine verkürzte Schreibweise für `for(var i = 0; i < allImages.length; i = i + 1 )`. Es wäre  auch möglich, `for(var i = 5; i < 100; i= i +5)` zu schreiben. Das bedeutet:   Zähler i ist 5. Solange i kleiner als 100 ist, erhöhe i um 5. Im ersten Durchlauf ist i 5, im zweiten 10, im dritten 15. Wir würden dann lediglich das 5te ,10te und 15te Bild erhalten.  
Es folgt:  

	{% highlight js %}
	var rect = page.rectangles.add({geometricBounds:[y, x, y + w,x + w]});
	{% endhighlight %}

Wir erzeugen auf der ersten Seite ein Rechteck, ähnlich wie bei unserem Dokument, und stellen die Außenkanten ein. Die `geometricBounds`. Wir könnten auch folgendes schreiben.  
  
	{% highlight js %}
	var rect = page.rectangles.add();
	var y1 = y;
	var x1 = x;
	var y2 = y1 + w;
	var x2 = x1 + w;
	rect.geometricBounds = [y1, x1, y2, x2];
	{% endhighlight %}
  
Die Eigenschaft `geometricBounds` erwartet immer ein Array mit 4 Stellen. Diese geben die linke, obere Ecke und die rechte, untere Ecke an. Immer von der oberen beziehungsweise linken Kante der Seite gemessen. Hierbei steht die y Koordinate vor der x Koordinate. Zu beachten ist auch, dass innerhalb von `add()` ein Doppelpunkt anstatt eines Gleichheitszeichens bei der Zuweisung des Wertes verwendet werden muss.  
Es folgen drei, einfache Befehle.  
  
	{% highlight js %}
	rect.place(allImages[i] );
	rect.fit(FitOptions.FILL_PROPORTIONALLY);// fit it to the frame
	rect.fit(FitOptions.CENTER_CONTENT);// fit it to the frame
	x +=w;
	{% endhighlight %}
  
Das Bild mit dem Index `i` wird in dem Rechteck platziert. Der Inhalt wird an die größe des Rechteckes angepasst, zentriert und wir erhöhen den x Wert um eine Bildbreite. Hier könnte auch `x = x + w` stehen. Es gibt weiter verkürzte Schreibweisen wie:

	{% highlight js %}
	x-=5; //  equivalent to x = x - 5;
	x*=5; //  equivalent to x = x * 5;
	x/=5; //  equivalent to x = x / 5;
	{% endhighlight %}

Da wir in unserer Schleife sind, geschieht dies für die komplette Menge der Bilder, unabhängig davon, ob 5, 100 oder 10000 vorhanden sind. Dies ist eine der großen Stärken von Skripten und Programmen. Die Iteration.  
Damit die Bilder nicht nur nach rechts platziert werden, sondern auch umbrechen, wenn x (oder x1) größer oder gleich der Breite der Seite minus der Bildbreite (der Rand) ist, müssen wir eine weitere Kondition hinzufügen.  

	{% highlight js %}
	if(x >= pw - (w)){
	x = w;
	y+= w;
	}
	{% endhighlight %}

Wenn diese Kondition nicht da wäre, würde das Skript die Bilder wie in der folgenden Grafik platzieren. Achtung! Wenn zuviele Bilder über die Arbeitsfläche hinaus gehen, kann das InDesign zum Absturz bringen und/oder das Dokument unwiderruflich zerstören.  

[![matrix onhe linebreak](images/matrx_without_breakline_thumb.jpg)](images/matrx_without_breakline.jpg)  

Die, die es bis hierher geschafft haben, sollten den vorherigen Code jetzt entschlüsseln können.  
Wenn x grösser gleich 150 - 25 ist, um auf unser Beispiel mit der 16 als Menge der Bilder zurückzukommen, setze x zurück auf 25 und addiere auf y 25. Die Zahlenreihe ist dann:  

	{% highlight text %}	
	i = 0
	x = 25
	y = 25  
	{% endhighlight %}

dann

	{% highlight text %}
	i = 1
	x = 50
	y = 25
	{% endhighlight %}

Das passiert solange bis x 125 ist. Dort setzt die Kondition `if(x >= pw - (w))` an. `x` wird in der Kondition zurück auf 25 gesetzt und y wird auf 50 gesetzt. Dann ist `i 4`.
Wir fangen bei 0 an zu zählen im Array also ist `allImages[4]` das fünfte Bild. Und so weiter und so weiter.  
Wir sind am Ende. Probieren sie den Code mit unterschiedliche vielen `.jpg` Dateien aus. Verändern sie ihn, bis er nicht mehr funktioniert und lesen sie die Fehlermeldungen. Dies ist ein weiterverbreitetes Problem. Computer und Programme würden viel an ihrer Mystik verlieren, wenn einerseits die Nutzer die Meldungen lesen würden, anstatt nur auf "ok" zu drücken und andererseits die Meldungen verständlich geschrieben wären.  

[![error](images/error_thumb.jpg)](images/error.jpg)  