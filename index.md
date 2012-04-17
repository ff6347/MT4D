---
layout: default
title: Mehr Zeit für Gestaltung
---
#BA von Fabian Morón Zirfas  
##Mehr Zeit für Gestaltung  
  
#Einleitung
Diese Arbeit setzt sich mit der Automation von Design-Prozessen auseinander. Sie ist keinen komplette Anleitung zum Erlernen von Programmier-Grundkenntissen, diese können für viele verschieden Sprachen im "World Wide Web" gefunden werden, sondern eine Auseinandersetzung was Automation durch Programmierung für Designer leisten kann und welche Bereiche sie nicht abdeckt. Dies wird durch einige kurze aber mächtige Beispiele illustriert.
Sie, die Arbeit, ist der versuch die Mystik und nebulösen Vorstellungen die sich um Computerprogramme ranken zu brechen und den die Schnitstellen die aktuelle Grafikprogramme bieten auf zu zeigen.  
Im ersten Teil soll dem Leser ein Verständnis für die Herkunft und Unterschiede von Computersprachen und den in ihrem Kontext verwendeten Vokablen vermittelt werden. Dadurch lassen sich die im zweiten Teil betrachteten Anwendungsgebiete unterschiedlicher Sprachen besser verstehen.  Hier wird auch aufgezeigt wo Grenzen liegen und wann es sinnig, unnötig und unerlässlich ist. Im dritten Teil werden dann die Einsatzmöglichkeiten innerhalb von Grafiksoftware beleuchtet und anhand von einfachen und dennoch mächtigen Automationen der Nutzen dargestellt den sie liefern. Im vierten Teil soll dann ergründet werden wo die Abwehrhaltung her rührt wenn das Thema auf das Erlernen von Programmiersprachen fällt und warum diese unbegründet sind beziehungsweise sogar schädlich sein können.  
Der fünfte Teil versucht dann an einem komplexerem Beispiel den Aufbau eines solchen Werkzeuges zu durchdringen die Methodik die dahinter steht zu erläutern.  
Abschliessend soll im Fazit der Erkenntniszuwachs aus alledem nochmals zusammengefasst werden.  
  
##Teil 1 Herkunft, Unterschiede und kleine Terminologie
[NOCH NICHT GESCHRIEBEN]  
###Herkunft von Computersprachen
[NOCH NICHT GESCHRIEBEN]    
###(Einige) Unterschiede von Computersprachen
[NOCH NICHT GESCHRIEBEN]  
###Was ist Code?
Als Code bezeichen wir in der Regelin Informationen die verschlüsselt (encoding) werden um dann an einer weiteren Stelle wieder entschlüsselt zu werden (decoding). Zum Beispiel stellt Morse-Code Buchstaben dar indem ein einziges unmoduliertes Signal, zum Beispiel ein Ton, in kurze und lange Sequenzen unterteilt wird. Der Rezipient kann dann, wenn er des Systems machtig ist, diese Informationen entschlüsseln und zu der originalen Nachricht wieder zusammensetzen. Ein weiters Bespiel ist der Abakus. Dieser erlaubt es wenn der Benutzer des Systems machtig ist Rechenoperationen auszuführen. Und als drittes die Knotenschrift der Inkas die wie der Name bereits besagt aus einem System von Knoten auf einem Satz Schnüren bestand. Heutzutage findet das Wort "Code" im Computerbereich oft Verwendung als Kurzform des Ausdrucks "Source-Code" also Quellkode eines Programms.  
  
###Was ist ein Programm?
Das Bild das wir im Kopf haben wenn wir das Wort Programm hören ist stark durch Film beeinflusst. Wir sehen junge, meist übergewichtig und verpickelte Menschen vor uns die in abgedunkelten Räumen zwischen Monitoren, Kabeln und Pizzapackungen auf ewige grün leuchtende Zahlenkolonnen blicken die für uns keinerlei Sinn ergeben. Diese oder ähnliche Bilder sind inspiriert aus einer Zeit in der Computer nur einfarbige Pixel hatten und Grafische Benutzeroberflächen wie Windows noch aus der Kommandozeile gestartet wurde. Als Hommage an diese Vorstellung hat "Duiker101" das Programm [HackerTyper](http://hackertyper.net/) entworfen welches mit bereits vorgegebenem Text allein über Tastendruck den Bildschirm mit kompliziertem Quellkode füllt. Dabei ist es irrelevant welche Tasten der Benutzer drückt.
Verwerfen sie diese Vorstellung (Es ist nicht so das es dies nicht gibt dennoch entspricht es nicht der Regel). Ein Programm ist lt. [Duden](http://www.duden.de/rechtschreibung/Programm): "die nach einem Plan genau festgelegten Einzelheiten eines Vorhabens"*. Unter dieser Betrachtungsweise ist jede Bauanleitung zu Möbelstücken, eine Beschreibung des Weges von hier zum Bahnhof oder das Rezept für Sahnetörtchen ein Programm. Bloß das in letzterem Fall nicht ein Computer die Anweisungen ausführt sondern ein Mensch. Die Sprache in der dieses Programm geschrieben ist, ist Deutsch. Der grosse Unterschied zu einem Computersprache/-programm liegt hier ein der Möglichkeit der Interpretation. Die Ausführende "Maschiene" (in diesem Fall der Mensch) kann solche Angaben wie "eine Priese Salz" oder "eine Messerspitze Merrettich" verarbeiten. Ein Computer ist hierzu (noch) nicht fähig. Er bräuchte eine eindeutigere Angabe wie 50 Gramm.  
Das Programm muss an dieser Stelle noch von dem Begriff des Algorithmus abgetrennt werden.  

###Was ist ein Algorithmus?
Auch wenn sich diese beiden Begriffe in ihrer Bedeutung teilweise überschneiden sollten diese auf folgende weise unterschieden werden. Der Algorithmus für Milch holen wäre in Pseudocode:  
`wenn (Aussage (kein Milch ist im Kühlschrank) wahr ist): hole neue Milch! wenn nicht: tue nichts!`  
Das Programm für Milch holen würde vorraussetzen das alle Schritte und Notwendigkeiten bis zum Übergang der Milch in das Eigentum der Holenden bekannt und definiert sind. Also so etwas wie:  
	Person fabian ist gleich neu Person;
	Kühlschrank schrank ist gleich neuer Kühlschrank;
	Kühlschrank Menge Milch ist gleich 1;
	jeden morgen fabian trinke Milch aus Kühlschrank, Menge 0.2;
	jeden morgen fabian beobachte Menge Milch;
	wenn Milch kleiner gleich 0.1 ist fabian hohle Milch im Supermarkt;
Und so weiter und so weiter. Diese Funktionsanweisungen könnten noch detailierter ausgearbeitet werden. Hierbei sei zu beachten das solche Objekte wie Kühlschrank und Person bereits implemetiert also bekannt sind. Das Programm im Vergleich zum Algorithmus muss alle eingesetzten Mittel kennen und oder selber beschreiben.  
  
###Was ist die Syntax?
Die Syntax ist die Form in der die Programmiersprache ausgestalltet ist. Die Syntax einer Programmiersprache besteht aus reservierten Worten wie zum Beispiel in Java `"new","while","null","true"`, Operatoren wie `"+","-","*","."` und Kontrollstrukturen wie `"if(){}else{}"` oder `"for(int i = 0; i < x;i++)"`. Diese Konstrukte dürfen nur für bestimmte Aufgaben verwendet werden. Wenn also ein Programmierer seine Variable `"null" nennet, wird das Programm beim ausführen eine Fehler auswerfen. Die obig genannten Strukturen, Operatoren und reservierten Worte müssen erlernt werden. Eine vollständige Beschreibung aller würde jedoch den Rahmen dieser Arbeit sprengen. Weiterhin ist beim schreiben von Programmen auch auf die Groß- und Kleinschreibung zu achten. Eine Variable die mit dem Namen "myValue" initiert wird muss auch mit diesem Namen aufgerufen werden. Bei einer falschen schreibweise "MyValue" oder "myvalue" würde das Programm warnen das die gewünschte Variable nicht existiert. Es gibt Sprachen die versuchen ihre Syntax so weit wie möglich an unseren Sprachen zu orientieren, zum Beispiel Applescript:
	tell application "Safari" to activate
und wieder andere wie die esoterische Programmiersprache*** "Brainfuck" die mit ihren acht Zeichen `+-<>[],.` voll funktionsfähig, aber nicht für das schreiben von Programmen gedacht ist sondern eher ein Gedankenmodell darstellt.
Das Brainfuck Hello World (aus wiki [http://en.wikipedia.org/wiki/Brainfuck](http://en.wikipedia.org/wiki/Brainfuck)):  
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
Wie bereits oben in der Beschreibung des Milchalgorithmus zu sehen ist verwendet selbst Pseudocode ein nicht genau definierte Syntax lehnt sich jedoch mit konstruktionen wie "ist gleich" an die Mathematik an. Andere Sprachen mit denen wir uns noch später Auseinandersetzen wie C++, Processing oder JavaScript sind zwischen diesen Extrema angesiedelt und vereinen in einer für das geübte Auge lesbaren und dennoch kompakte Art die Befehlsufrufe.
  
###Was ist Hello World? 
Das "Hello World" Programm hat sich als standard Beispiel etabliert um die Syntax einer Sprache zu erklären. Exerzieren wir das einmal kurz durch. Um für Adobe InDesign, After Effects, Illustrator, Photoshop, Photoshop Elements, Photoshop Elements Organizer, Bridge, Audition, Media Encoder und Premiere Pro Skripte zu schreiben liefert Adobe eine eigene IDE, eine Integrierte Entwicklungs Umgebung, mit. Das ExtendScript Toolkit. Dies ist nicht der schönste Editor. Er hat jedoch einige Vorteile die die Entwicklung von Skripten sehr einfach macht. Die wichtigste Eigenschaft ist dabei folgende. Es kann ein Skript ohne es zu speichern ausführen. Probier es aus. Das Toolkit wird bei der Installation von Adobe Produkten direkt mit  geliefert. Suche es in deinen Dienstprogrammen dort solltest du fündig werden. Wenn nicht gehe zu diesem Webseite [http://www.adobe.com/devnet/scripting.html](http://www.adobe.com/devnet/scripting.html) und lade und installiere es.  
Wenn es dann installiert ist gib folgende Text ein:  

	alert("Hello World")

und drücke auf den "Play/Run" Knopf oben rechts oder drücke CMD-r oder CTRL-r, abhängig von deiner Platform. Herzlichen Glückwunsch. Dein erstes Javascript.  
Um dieses Skript in InDesign oder Photoshop auszuführen muss die Ziel Applikation aus dem PullDown Menü auf der oberen Leiste gewählt werden. Beim öffenen ist es auf ExtendScript Toolkit gestellt. Wähle InDesign aus. Das Toolkit wird sofort fragen ob InDesign auch gestartet werden soll. Bestätige das und führe das Skript noch einmal aus. Du wirst sehen das der Computer zu InDesign überwechselt und den gleichen Hinweis gibt.  
Probiere weiter Skripte und Kalkulationen aus. Zum Beispiel  

	var h = "Hello";
	var w = "World";
	var calc = (10*50)/23 - 1;
	alert(h + " " + w +"! Your result is: "+ clac );  
  

      
###Was ist Pseudocode?
Im Verlaufe dieser Arbeit werde ich immer wieder auf die Darstellung von Alogrithmen in "Pseudocode" zurückgreifen. Pseudocode besteht nicht aus einer bereits definierten Syntax und kann auch nicht von einem Compiler übersetzt werden sondern dient nur zur Darstellung eines logischen Ablaufs. Wie bereits in dem Milchalgorithmus zu sehen war versucht Pseudocode einen Programmablauf in menschenlesbarer Form darzustellen.  
  
###Was ist ein Compiler?
Der Vollständigkeit halber soll dieser hier erklärt werden auch wenn er uns kaum mehr im weiteren Verlauf der Arbeit begegen wird. Der Compiler ist ebenfalls ein Programm das aus menschenlesbaren Hochsprachen wie zum Beispiel C++ maschienenlesbaren Quellkode erzeugt (Assemblercode). Diesen Prozess bezeichnet man auch als Kompilierung.  
  
###Was ist eine IDE (Integrated Development Envoirement)?
Um Quellkode zu schreiben bedarf es nicht viel. Ein einfacher Texteditor reicht aus um komplette Programme zu schreiben. Im Laufe der Zeit wurde jedoch viel Software programmiert um das schreiben von Quelltext zu erleichtern. Dies geht los bei einfachem Syntax-Highlighting bis hinzu kompletten Entwicklungsumgebungen die noch vor dem Kompilieren beziehungweise während des schreibens die Syntax auf ihre Validität prüfen und gegebenfalls Vorschläge machen was gemeint sein könnte oder bei nicht verwendeten Programmteilen warnen das diese derzeit unnütz sind. In unserem Fallbeispieln werden wir noch mit diesen Programmen zu tuen kriegen. Es sei jedoch bereits gesagt das wir die einfachste Möglichkeit nutzen werden die sich uns bietet und die auf beiden Platformen (Windows und Mac OS X) zur Verfügung steht. Das ExtendScript Toolkit (Mehr dazu ist im Abschnitt: Was ist Hello World? zu finden).  
  
#Was ist Syntax-Highlighting?
Syntax Highlighting ist eine Hilfestellung für Programmierer um ihren Quellkode übersichtlicher zu gestalten. Hierbei werden bestimmte Teile wie Operatoren,Kommentare, Funktionsdeklarationen oder Reservierte Worte farblich hervorgehoben beziehungsweise zurückgenommen um das Lesen zu erleichtern.  
  
###Was ist eine API (Application Programming Interface)?
Dies ist die Schnittstelle die ein Programm bietet um auf sein Funktionen zugreifen zu können. Dies wird beim Schreiben von Programmen wie InDesign von den Programmierern definiert. Diese Schnittstelle ist wie ein Baum mit Querverweisen aufgebaut. Um in InDesign einem bestehendem Dokument auf der ersten Seite eine Textbox hinzuzufügen muss durch diesen Baum manövriert werden.  
	app.activeDocument.pages.item(0).textFrames.add();
Diese Zeile erzeugt in der linken oberen Ecken eine Textkiste.  
All diese Befehle und Eigenschaften müssen nicht auswendig gelernt werden sondern können nachgeschlagen werden. Im ExtendScript Toolkit kann unter Hilfe / ObjektModell Viewer ein Hilfsprogramm aufgerufen werden das alle Befehle mit einer kurzen Erklärung enthält. Oder es kann auf der Seite von jongware eine .chm Datei heruntergeladen werden die die gleichen Informationen enthält und mit einem .chm Viewer durchsucht werden kann. [http://www.jongware.com/idjshelp.html](http://www.jongware.com/idjshelp.html)
  
###Was ist Objektorientierung?
Als Objektorientierung (ach als OO abgekürzt) versteht man ein bestimmte Art wie Programme aufgebaut sind. Ein Objekt ist ein gekapselter Teil des Programmcodes der Schnittstellen und Methoden bietet und seine Eigenschaften an weiter Objekte vererben kann. Um dies besser zu verstehen möchte ein hervorragendes Beispiel aus "Processing: A Programming Handbook for Visual Designers and Artists" von Casey Reas and Ben Fry bemühen.  
####Klammer auf!
{
Der Proto-Apfel (Der Proto-Apfel existiert eingentlich nicht. Unsere Sprache lässt solche Ungenauigkeiten zu. Es gibt einen Apfel und einen Anderen. Aber nicht "DEN" Apfel. ) hat bestimmte Eigenschaften wie Gewicht und Farbe. Hinzu kommen bestimmte Methoden wie Fallen, Wachsen und Verrotten die durch die Eigenschaften beeinflusste werden können.  
(Abb 01)  
 Wenn nun ein Baum wächst und Äpfel produziert erzeugt er nach dem Bauplan des Proto-Apfels neue Äpfel und jedem werden bestimmte Werte übergeben.  
(Abb 02)  
Der Baum erzeugt den Apfel und ruft kontinuierlich die Methode Wachsen auf. Hierbei wird der Wert des Gewichtes inkrementiert. Sind die Früchte dann reif wird abhängig vom Gewicht des einzelnen Apfels die Methode Fallen ausgelösst. Wenn der Apfel dann auf dem Boden liegt und die Methode Fallen beendet ist beginnt die Methode Verroten ihre Arbeit. Die Farbe des Apfels verändert sich und das Gewicht wird wieder verringert.
Das bedeutet der Proto-Apfel selber wird nicht angerührt sondern Instanzen von diesem. Um dies noch auf die Spitze zu treiben haben wir nicht nur eine Art Apfel sondern verschieden Sorten. Also ist die Klasse Granny Smith und ein "Kind"-Klasse der Basisklasse Apfel. Granny Smith erbt alle Eigenschaften der Klasse Apfel ohne das sie neu implemntiert werden müssen und bekommt noch eine weitere Eigenschaft: den Namen.
}  
####Klammer zu.  
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
In dem Format "[Einfacher Absatz]" wird eine Schriftart und eine Schriftgrösse definiert. Dieses Format ist das Proto-Format von dem sich alle weiteren Formate ableiten. Sie erben also alle die Eigenschaften Schrift (appliedFont) und die Schriftgrösse (pointSize). Das Format "Überschrift 1" (Ü1) bekommt dann eine eigene Schriftgrösse und einen fetten Schnitt der Schriftart. Im dem Format "Überschrift 2" (Ü2) wird dann festgelegt das nicht mehr das "[Einfacher Absatz]" Format als Basis Klasse benutzt wird sondern Ü1. Damit erbt Ü2 alle Eigenschaften von Ü1. In Ü2 wird dann nurnoch eine neue Schriftgrösse festgelegt. Das gleiche kann dann mit "Überschrift 3" (Ü3) passieren. Ü3 basiert auf Ü2 und bekommt ebenfalls eine eigene Schriftgrösse. Jetzt basiert Ü3 auf Ü2, das auf Ü1 und das auf "[Einfacher Absatz]". Ähnlich verfahren wir mit den weiteren Formaten. "Textkörper" basiert auf "[Einfacher Absatz]", "Bildunterschrift" auf "Textkörper" nur kleiner und "Pagina" auf "Bildunterschrift" aber mit 70% Deckkraft. Wenn der Gestalter nun entscheidet dass eine andere Schriftart von Nöten ist, ändert er sie nur in "[Einfacher Absatz]" und alle Kinder werden entsprechend angepasst. Dies ist ebenfalls Objektorientiert.  
}  
####Klammer zu
  
###Was sind Funktionen/Methoden?
Eine Funktion oder eine Methode sind gekapselte Programmteile and die Parameter übergeben werden können und die aus den gegebenen Parametern eine Kalkulation durchführen. Sie können dann Werte zurückgeben. Dies ist nützlich wenn bestimmte Tätigkeiten an unterschiedlichen Positionen eins Programms oder Skripts mehr mals aufgerufen werden müssen.     
###Was ist ein Bug?
Ein Bug ist ein Fehler der das Programm von seiner einwandfreien Ausführung abhält. Dies kann nur ein Rechenfehler sein oder ein Fehler der das gesamte Programm zum Absturz bringt.  
  
###Was ist Debugging?
Dies ist der Prozess des Findens und korrigeren von Fehlern.  

###Was ist ein Workaround?  
Ein Workaround ist eine kreative Lösung um ein Problem zu umgehen. Wenn zum Beispiel eine API ein bestimmte Funktion nicht anbietet muss ein Weg um dieses Problem drumherum gefunden werden. 
  
###Welche Konventionen gibt es?
Neben den Bestimmungen der Syntax gibt es verschiedene Konventionen die das lesen von Skripten einfacher machen sollen. Zum Beispiel ist es gang und gebe dass die Funktionsweise am Beginn eines Skripts in einem Kommentar erklärt wird. Oder die Verwendung der Variable i (für Iterator) als Zähler in Schleifen.
  
#Was ist Scripting?
> Scripting languages assume that there already exists a collection of useful components written in other languages. Scripting languages aren't intended for writing applications from scratch; they are intended primarily for plugging together components  
> Scripting: Higher Level Programming
for the 21st Century by John K. Ousterhout
   

###Was ist der Unterschied zwischen Javascript und ExtendScript?
JavaScript oder EcmaScript ist das was uns täglich in Webbrowsern solche Dinge bescherte wie Scrollen auf Knopfdruck oder Warnhinweise und ähnliches. ExtendScript ist ein Dialekt von JavaScript der von Adobe entwickelt wurde. Das bedeutet InDesign versteht JavaScript und ExtendScript aber ein Browser kann mit ExtendScript Befehlen nichts anfangen.  
  
##Teil 2 Anwendungsgebiete
Auch wenn Aufgaben auf unterschiedliche Weise mit verschiedenen Programmiersprachen gelöst werden können haben sich spezielle Anwendungsgebiete für die einzelnen Sprachen ergeben. Ganz unabhängig davon, dass sich in unserem Fall Adobe Anwendungen nur mit AppleScript, VisualBasic oder JavaScript ansprechen lassen macht es Sinn eine Scriptsprache zu verwenden um die bereits in höheren Sprachen implemetierten Funktionen zu verbinden.  
  
Zur Veranschaulichung was das in der Anwendung bedeutet zur hier ein Programm das folgende Aufgaben erledigt.
Ein Objekt erzeugen mit folgenden Eigenschaften  
- Einem Namen  
- Einer Funktion die 2 Zahlen mit einander vergleicht und feststellt welche die grössere von beiden ist.
Dann gibt das Programm eine Meldung mit dem Ergebnis zurück.  
  
Dieses Programm liegt hier in verschiedenen Sprachen vor.  
Ich werde hier kurz auf die Unterschiede eingehen. Eine tiefere Erklärung des Quellcodes findet sich in den Kommentaren der einzelnen Programme.  
####Assembler (anObject.s)  
Aus Platzgründen werde ich hier nur die ersten 29 Zeilen zeigen. Das gesamte Programm in Assembler Code ist über 700 Zeilen lang.  

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

Dies ist die Variente die die Maschiene versteht. Es wurde jedoch nicht von mir geschrieben sondern ist das Ergebnis des Kompilierungsprozesses des C++ Programms. Näher wäre nur noch Nullen und Einsen zu schrieben.
####ANSI C anObject.c  
  
	//based on Phil's guide to object-oriented ANSI C
	// http://www.bolthole.com/OO-C-programming.html
	// and some stackoverflow.com questions about Object orientation in ANSI C
	
	#include <stdio.h>
	#include <stdlib.h>
	
	// this is something like the class
	typedef struct OBJECT {
	  int res; // the object knows it result
	  char *name; // the char array for the name
	} OBJECT
	
	typedef OBJECT* Object;
	 // ------------ now the methods of the "class" ------------ 
	
	//Create a new objact based on struct OBJECT
	Object obj_create() {
	  Object s;
	  s = (Object) malloc(sizeof(OBJECT));
	  // set the fields to inital values
	  s->res = 0;
	  s->name = "undefined";
	
	  return(s);// gibe back the object
	}
	// need to remove this object again
	void obj_destroy(Object s) { free(s); }
	// this is the compare method
	int obj_compare(Object s, int a, int b){
			if(a>b){
				s->res = a;
			}else if (b>a){
				s->res = b;
			}else if(b == a){
			s->res = 0;
		}
		return s->res;
	}
	
	void obj_set_name(Object s, char *n){
	s->name = n;
	}
	
	
	int main(void) {
	  Object s = obj_create();
	
	    s.compare_ptr = compare;
	
	  obj_set_name(s,"Hello ANSI C");
	  int a = 23, b = 5;
	
	  printf("The Object named \"%s\" compared %d with %d. The result is %d \n",s->name, a,b, obj_compare(s, a, b));
	obj_destroy(s);
	  return 0;
	}

####ANSI C anObject.c  

	#include<stdio.h>

	compare(int a, int b){
		if(a>b){return a;}else{return b;}
		}
	
	int main(void){
		char name[11] = "Hello World";
		int a = 23,b = 5;
		printf("The Object named: %s\nCompared: %d with %d.\n%d is bigger!\n",name,a,b,compare(a,b));
	
		return 0;
	}

Für die C Implementation gibt es zwei Beispiele. Im Unterschied zu C++ und JS ist die Sprache C von grundsätzlich nicht für eine Objektorientierung ausgelegt. Deshalb hier einmal das Beispiel noObject.c welches ebnfalls die gestellte Aufgabe des Vergleich lösst aber kein Objekt erzeugt und die Variante anObject.c. In Diesem Beispiel wird ein Objekt erzeugt. Im Vergleich zu der C++ Version anObject.cpp ist in diesem Objekt das Objekt Orientierungs Paradigma Vererbung nicht enthalten.  
####C++ (anObject.cpp)  
  
	#include <iostream>
	#include <string>
	
	// using namespace std; // if you use this you can remove all "std::"
	class Object{
		
	public:
		std::string name;
		Object(){}// basis constructor
		Object(std::string in){name = in;}// another constructor
		int compare(int a, int b);//Prototype
		void setName(std::string in){name = in;}
	};
	
	int Object::compare(int a, int b){
		if(a>b){return a;}else{return b;}
	}
	
	int main(){
		Object* myObject = new Object("Hello World");
	
		int a = 23,b = 5;
	
		std::cout << "The Object named: "<< 
		myObject->name << "\nCompared: "
		<< a << " with "
		<< b << "\n" 
		<< myObject->compare(a,b) <<" is bigger\n" 
		<< std::endl;
		/* code */
		delete myObject;
		return 0;
	}
  
In diesem Beispiel ist bereits zu sehen, dass die Menge an Code die geschrieben werden muss geringer wird. Wobei hier wie auch im C Beispiel bedacht werden muss dass, bereits vorhandene Programmteile eingebunden werden. Mit der Aussage:  
	#include <iostream>
	#include <string>
werden fertige Klassen und Methoden eingebunden. "iostream" um die Ein- und Ausgabe des Programms zu handhaben und "string" um Zeichenketten zu verarbeiten. Der Unterschied ist enorm. Während in C eine Zeichenkette noch eine Liste einzelner Zeichen ist wird in C++ ein Zeichenkette als ein einziges Objekt gehandhabt und bringt viele Funktionen mit zur Verarbeitung dieser.  
####JavaScript (anObject.js)  
  
	main();
	
	function main(){
	
		var obj = build_new_object("Hello Javascript");
		var a = 23, b = 5;
		obj.compare(a,b);
		alert("The Object named: "+ obj.name +"\nCompared: "+ a +" with "+ b +"\n" + obj.result + " is bigger\n");
		obj = null;
		return 0;
	}
	
	function build_new_object(n){
	    var obj = {
		name:n,
	    result:0,
		compare : function(a,b){if(a>b){return a;}else{return b;}}
	    };
	    return obj;
	}
  
Mit JavaScript gehen wir noch einen Schritt weiter. Hier sind das Objekt, die Ein-/Ausgabe, der String bereits existent und müssen nicht neu implementiert noch eingebunden werden. Der massgebende  Unterschied ist dass, die vorherigen Programme wirklich vollwertige Programme sind die nach dem Kompilieren aus der Kommandozeile ausgeführt werden können. Die JavaScript Variante benötigit ein Programm in dem es ausgeführt wird. Es ist also alleine nicht lauffähig.  
  
Dies ist der Punkt wo wir als Gestalter ansetzen können. Wir müssen das Rad nicht neu erfinden. Wir können jedoch unseren Arbeitsablauf durch gezielte Befehlsketten von repetitive Aufgaben befreien. Ich bin mir sicher dass ein grossteil aller Gestalter die vorgefertigte Software für ihre Arbeit verwenden schon einmal an den Punkt kamen wo sie sich dachten: "Warum kann mein Programm DAS nicht," (DAS steht hier für eine gewünschte Funktionsweise)  "es ist doch alles da. Der Knopf und danach Knopf!". Scripting erlaubt es uns diese beiden Knöpfe mit eineander zu verbinden. Das bedeutet dann das wir unsere Arbeit um einen "Klick" reduziert haben. Wir haben zwei Knöpfe durch Verkettung auf einen neuen Knopf gelegt. Natürlich klingt die Reduktion um einen Klick vernachlässigbar. Wenn Jedoch diese zwei Klicks 100 mal ausgeführt werden müssen und wir durch logische Anweisung diese ebenfalls auf nur einen Knopf zusammenführen können ist der Zeitgewinn enorm. Ebenfalls muss hier erwähnt werden das viele der Probleme die in einem Gestlatungsprozess auftreten nicht zum erstenmal bei eben dieser Person auftreten. Für den Bereich Scripting von Adobe Anwendungen gibt es im Netz viele Seiten und Foren die sich mit diesem Thema befassen. Im Bereich JavaScript gibt es noch viele mehr, da JavaScript auch verwendet wird beziehungsweise entwichelt wurde um Browser zu steuern. Dementsprechend ist die Dokumentation für JavaScript mehr als ausgiebig. Es Bedarf nur einiger Übung um die gefundenen Beispiele auf die eigene Problemstellung zu abstrahieren.  
####Hierbei sei zu beachten!  
Scripting kann keine Entscheidungen fällen. Es existiert kein Algorithmus der Ästhetik simuliert. Um eine spannende Komposition zu schaffen braucht der Gestalter "nur" drei geometrische Grundformen zu erzeugen und diese im richtigen Verhältnis zu einander anzuordnen. Um dies programmatisch zu lösen müsste ein Skript mehrere hundert mal ausgeführt werden. Jedesmal mit einer kleinen Veränderung der Koordinaten der obig genannten drei Objekte. Daher sollte bevor der Author in die Tiefen von JavaScript abtaucht endschieden werden:  
  
- Wie komplex sind die Operationen?
- Wie ist das Zeitfenster und wann muss das Produkt fertig sein?
- Wie oft muss diese Tätigkeit ausgeführt werden?
- Lässt sich die Automation auch auf andere ähnliche Bereiche anwenden bzw mit geringen Aufwand abstrahieren?
- Wie sehr ist sie von Umgebungsvariablen abhängig?  
- Soll die Automation von dritten Benutzt werden?
- Ist der Prozess linear oder bedarf es einer Rückkopplung zum Benutzer?

Und einige Punkte die sich hauptsächlich durch Recherche abarbeiten lassen  

- Existieren bereits Automationen in dem Sektor und wenn ja lassen sich diese abwandeln?
- Bietet die API direkten Zugriff auf die benötigten Funktionen oder bedarf es eines Workarounds? 

Diese Analyse kann keine genauen Angaben über Zeit und Aufwand machen da dies immer auch vom Erfindungsreichtum des Authors abhängig ist. Der Kreative kommt hier schneller zum Ziel.

- Wie komplex sind die Operationen?  

Wenn eine fülle von unterschiedlichen Operationen ausgeführt werden soll, müssen auch ensprechend viele Anweisungen an das Programm erfolgen und der Author muss sich auf eine längere Entwicklungszeit einstellen. Wenn es im Gegensatz darum geht eine Hand voll Operationen sagen wir 1000 mal auszuführen kann es sein das sich der Kern des Skriptes auf ca 10 Zeile reduziert. Das bedeutet auch das die Zeit für Entwicklung und Debugging relativ gering sein können und sich der Zeitaufwand lohnen kann. 
  
- Wie ist das Zeitfenster und wann muss das Produkt fertig sein?  

Auch hier muss abhängig von der Komplexität des Skriptes und dem eigenem Vermögen geurteilt werden ob dies in dem gegebenen Zeitraum Recherchiert, Entworfen, Geschrieben und Debugged werden kann. Hinzukommt das das Ergebnis meist nur ein Teilergebnis ist und noch weiterverabeitet werden muss. Es ist davon auszugehen das etwaige tiefere Fehler erst während des vollem Einsatzes auftreten. Wenn dies in dem entsprechendem Zeitraum nicht zu bewerkstelligen ist sollte von einer Entwicklung abgesehen werden.

- Wie oft muss diese Tätigkeit ausgeführt werden?  

Wenn das Skript nur ein einziges mal ausgeführt werden soll ist sollte man sich fragen wo darin der Nutzen liegt. Es kann natürlich sein das dies Sinn und Zweck hat und sollte nur bedingt ausschlaggebend sein. Hierbei gilt es zu Unterscheiden das einmalig 1000 mal einen Knopf drücken bereits eine Hilfe sein kann. Einmalig 1000 mal unterschiedliche Knöpfe drücken ist eine Aufgabe die doch besser manuell geschieht.  

- Lässt sich die Automation auch auf andere ähnliche Bereiche anwenden bzw mit geringen Aufwand abstrahieren?  

Wenn dies der Fall ist steigt der Nutzen der Arbeit. Der einmalige Aufwand ein Programm oder Skript für eine immer wieder kehrende beziehungsweise ähnliche Aufgabe zu schreiben reduziert sich im "nachhinein" durch jede Ausführung. Dies soll heissen: Durch das schreiben des Programms das ich immer wieder verwende spare ich Zeit in der Zukunft. 

- Wie sehr ist sie (Die Aufgabe) von Umgebungsvariablen abhängig?  

(Das selbstgeschriebene Programm ist in diesem Fall aussen vor. Wie bereits oben erwähnt setzt das Programm alle Möglichkeiten vorraus. Das Skript hingegen greift auf bestehende Komponenten zu.) Kann das Skript unabhängig von allen Variablen die der Benutzer setzen kann ausgeführt werden vereinfacht das den Aufwand. Bei einer Abhängigkeit Bedarf es immer erst einer Abfrage des ist Status und einer Evaluierung. In Illustrator oder InDesign wird die aktuelle Auswahl des aktiven Dokuments in einer Liste genannt "selection" geführt.
	app.activeDocument.selection;
In dieser Liste liegen Einzelne Objekte die Text sein können oder eine Vektorform oder ein Bild. All diese haben gemeinsame Eigenschaften aber auch spezielle. Es muss also befor eine Eigenschaft genutzt oder verändert werden kann eine Abfrage stattfinden welche Art von Objekt einthalten ist.  
	var firstListItem = app.activeDocument.selection[0]; // first object in selection 
		if(firstListItem instanceof TextFrame){ /* check the type */
		alert("I am a " + firstListItem.typename);    // and name it
	}  
Viele solcher Abfrage können ein Skript schnell komplex werden lassen. Oder anders ausgedrückt je universeller der Nutzen sein soll desto mehr Umgebungsvariablen müssen beachtet werden. Dies bedarf natülich Zeit.  

- Soll die Automation von dritten Benutzt werden?  

Dies ist ein wichtiger Faktor. Wenn nur der Author selber die Automation verwendet kann er seine vorhergehenden Aktionen auf die Bedürfnisse und Beschränkungen des Skriptes anpassen. Wenn jedoch eine unbedarfte oder schlimmer noch eine dem Skripten nicht mä(ö)chtige Person dieses Werkzeug nutzen soll müssen wie bereits oben erwähnt viele Umgebungsvariablen abgefragt oder selber bestimmt werden. Im Programmier-Slang sagt man: "Man muss vom DAU* ausgehen." (Dümmster Anzunehmender User). Dies ist nicht als Beleidigung gedacht. Es soll eher sagen dass alle Benutzerfehler die auftreten können auftreten werden. In diesem Fall bekommt ein Nicht des Programmierens Mächtiger wenn er Glück hat nur eine Fehlermeldung, wenn er Pech hat einen Programmabsturz. In beiden Fällen steigt die Hemmung des Nutzer ungemein das Skript noch einmal zu verwenden. Wenn also Dritte mit ins Spiel kommen bedarf es noch längerer Test- und Debug-Phasen.  
  
- Ist der Prozess linear oder bedarf es einer Rückkopplung zum Benutzer?  

Wenn dem so ist sollte der Prozess vielleicht in mehrere Skripte zerlegt werden. Für den Fall das Variablen von einem Skript an das nächste übergeben werden müssen kann dies die Komplexität weiter erhöhen. In diesem Fall gibt es die Möglichkeit eigene Textdateien vom Skript kreieren zu lassen in dem Werte abgelegt werden können, Eine Script Panel zu erzeugen oder eine eigene #targetengine zu erzeugen in der solange das Programm aktiv ist Daten gespeichert werden. Die letzten bieden sind jedoch bereits eine sehr forgeschrittene Methode die ebenfalls viele Stolpersteine beherbergen kann.  
####Das Beispiel targetengine 
Skript 1:
	#targetengine "session01"
	var myValue = 0; // new value
	alert(myValue); // result is 0
	myValue++; // increment by 1
  
Skript 2:
	#targetengine "session01"
	alert(myValue); // result is 1
  
Der Algorithmus is wie folgt  

	Start  
	Sitzung 1
	definiere Variable meinWert und speicher 0 in ihr
	zeige Wert von meinWert
	erhöhe meinWert im eins
	Stop  
  
	Start  
	Sitzung 1
	zeige Wert von meinWert
	Stop  
  
Dies bedeutet dass das Programm (nicht das Skript) sich den Wert für die Variable myValue gemerkt hat und ihn solange in targetengine "session01" speichert bis es beendet wird. Hier liegt die Gefahr darin Variablen Namen doppelt zu vergeben. In vielen meiner Skripte speichere ich das aktive Dokument in der variable doc. Wenn diese nun in einer targetengine liegen wird das Programm immer auf das zuletzt "doc" gleichgesetzte Objekt zugreifen auch wenn dies vielleicht nicht gewünscht ist sondern vom Benutzer nicht beachtet wurde. Auch die Verwendung von Textdateien kann ihre Tücken haben. Auf unterschiedlichen Betriebsystemen werden Dateipfade unterschiedlich gehandhabt. Wenn das Skript von dritten verwendet werde soll kommen wir wieder zum vorherigen Punkt zurück. Auch dies will abgefragt und getestet werden. "Last but not least" gibt es noch die Möglichkeit eigene Grafische Benutzeroberflächen zu erzeugen. Dies ist ebenfalls eine Variante für erfahrenere Authoren.   
  
Die Recherchearbeiten sollten bereits vor dem ersten Entwurf erledigt sein.

- Existieren bereits Automationen in dem Sektor und wenn ja lassen sich diese abwandeln?  

Wie bereits oben erwähnt sind viele Probleme bereits einmal aufgetreten am Ende dieser Arbeit ist eine Liste zu finden wo für welchen Zweck nach Informationen gesucht werden kann. Wenn das Problem nicht all zu speziell ist kann es gut sein, dass es bereits ein Skript gibt das entweder genau diese Funktion enthält und wenn nicht auf die eigenen Bedürfnisse angepasst werden kann oder was meist der Fall es mehrere Skripte gibt die Teilprozesse der eigenen Idee beinhalten und als Referenz benutzt werden können. In den seltesten Fällen entsteht ein Skript von Scratch*(aus einem blanken Textdokument). 
  
- Bietet die API direkten Zugriff auf die benötigten Funktionen oder bedarf es eines Workarounds?  

Dies Bedarf eines Beispiels. InDesign kann nicht erfragen ob ein Zeichen in einer Schriftart enthalten ist. Es gibt als kein Feld das so etwas wie "Font has Character" beinhaltet. Um dieses Abfrage zu simulieren hat Peter Kahrel für InDesign die Funktion  try_char geschrieben die hier in einer etwas abgewandelten Form folgt.  
  
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
		alert("The character "+theChar + "could not be converted into an Outline");
        }  
    }  

Solche Lösungen setzen nicht nur ein kreativen Umgang mit Code vorraus sondern auch ein tiefes Wissen über die Funktionsweise und Möglichkeiten innerhalb von, in diesem Falle, InDesign.  
  
Die obig genannten Hindernisse schrecken ab. Es klingt alles sehr komplex. Es ist jedoch alles sehr allgemein gehalten und manche Fragen stelle sich auch erst gar nicht. Bei Aufgaben die ein Normal Nutzer niemals manuell machen würde muss sogar ein Skript geschrieben werden wenn sie erledigt werden soll.  
Auch wenn der Prozess des Skript schriebens eine Kreative Arbeit ist, ist das Ziel des Skriptes nicht der Kreative Output sondern die Optimierung der eigenen Arbeitsabläufe. Das Skript oder Programm kann niemals die Idee liefern. Es unterstützt den Prozess indem es repetitive Aufgaben erledigt die entweder niemals gemacht worden wären oder aber vom eigentlichen Kreativem Prozess ablenken.   
  
##Teil 3 Der Einsatz
Die Fragen die sich jetzt stellen sind folgende: "Wie kommt dies zum Einsaz?", "Wie kann ich dies nutzen?".
Es folgt nun das InDesign Skript image_matrix.jsx mit etwas mehr als 40 Zeilen Code. Dieses Skript beinhaltet eine Benutzer Interaktion, Dateihandhabung, das Math Objekt*(ein bereits bestehnder Teil von Javascript. Es erledigt solche Aufgaben wie Rundung von Werten oder das Berechnen einer Quadratwurzel), Conditionen, eine Schleife, Funktionen, Variablen und es hat einen Generativen Character. Das Skript erledigt folgende Schritte (in Pseudocode).
Frage den Benutzer nach einem Ordner mit jpg Dateien.  
Erzeuge ein Quadratisches Dokument dessen Grösse auf der Quadratwurzel der Menge der Bilder bassiert und alle Bilder fast.  
Platziere alle Bilder.  
  
Kopiere den nachstehenden Code. Bereite dir einen Ordner mit einigen Jpg-Bildern vor. Es sollten um die 15 bis 30 sein. Die genau Menge ist irelevant. Lies nochmal den Abschnitt Hello World und wie Skripte ausgeführt werden können und führe das Skript aus. Wenn der Ordnerauswahl Dialog sich öffnet wähle deinen Ordner mit den Bildern an.
Das gesamte Skript:  

	{// START SCRIPT
	main(); // you need a function to be able to cancel a script

	function main(){// all is in here

	var w = 25; // the image sizes
	var allImages = loadFiles("*.jpg");// opens a prompt and lets the user choose a folder
	if(allImages == null) return; // if that what the function returns null is - cancel

	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2); // this will hold the page width
	var ph = pw;

	if(Math.round(Math.sqrt(allImages.length)) != Math.sqrt(allImages.length)){
	        ph = pw + w;
	        }

	var doc = app.documents.add(); //build a basic document
	doc.documentPreferences.pageWidth = pw;// set the width
	doc.documentPreferences.pageHeight = ph; // set the height
	var page = doc.pages.item(0);// finally - get the first page

	var y = w; // the upper left corner
	var x = w; // the upper left corner

	for(var i in allImages){// loop thru all images

	var rect = page.rectangles.add({geometricBounds:[y,x,y + w,x + w]});// add a rectangle to the page
	rect.place(allImages[i] );// place the image
	rect.fit(FitOptions.CONTENT_TO_FRAME);// fit it to the frame
	x +=w; // increase x by an image width

	if(x >= pw - (w)){ // if x is the width minus an image width
	        x = w; // reset x
	        y+= w; // and increment y by an image width
	        };//end increase x and y conditional

	    };//close allImages loop

	};// end main function

	function loadFiles(type){// the function that loads the files

	var theFolder = Folder.selectDialog ("Choose the FOLDER");// user select a folder

	if(!theFolder){// if the folder is not a folder cancel the script
		return;// this cancels the whole function image_loadFiles
			}; // end foldr check

	var allImages = theFolder.getFiles(type);// get the files by type
	if((allImages.length < 1)||(allImages == null) ){// again if check if there are images
		alert("There are no images");// hm something went wrong? User error
		return null;// so we cancel the function
		   }else{
		return allImages;// give back the images. Success!
	        };// end all images check

		};// end function loadFiles
	} // END OF SCRIPT
  
###Das Skript Schritt für Schritt.  
Ein Skript sollte immer in geschwungenen Klammern engefasst sein. Dies ist nicht zwingend jedoch nützlich falls das Skript von einem anderem Skript evaluiert werden muss. Innerhalb dieser Klammern folgt der gesamte Quellcode.
	{}
Als nächstes definieren wir eine Funktion die einmalig aufgerufen wird. Hierbei ist es irrelevant ob der Aufruf vor oder nach der Funktionsdefinition stattfindet. Aus Gründen der Übersichtlicheit steht hier der Aufruf vor der definition. Diese Funktion erhält keine Parameter. Später wird auch ein Funktion mit Parametern eingesetzt. Der Zweck den gesamten Code in einer Funktion zu kapseln ist folgender: Wenn es eine hirarchisch höhere Ebene gibt, unsere `{}` Klammern, kann eine Funktion mit dem Befehl `return;` beendet werden. Dies ist nützlich um bei Fehlern oder falscher Benutzer Eingabe die Ausführung zu stoppen. Mit diesem Befehl kann nicht nur ein Funktion beendet werden sondern auch ein Wert zurückgegben werden. Wenn wir also schreiben `return 1;` am Ende einer Funktion wäre das Ergebniss 1. `var myValue = main();` Wenn die Funktion main nun einen Wert zurückgeben würde, wäre `myValue` 1. In unserem Fall benötigt die `main()` keinen Rückgabewert.

	main();
	function main(){
	}

Wir befinden uns nun in der Funktion `main();`.  
Es folgt die deklaration der ersten Variable. Sie beinhaltet die  Breite (und Höhe) unserer Bilder.

	var w = 25;

Wie zu sehen ist entspricht die Variable `w`*(steht für width) nun 25. `w` wird im Verlauf des Skriptes mehrmals verwendet. Der Vorteil  daran Variablen zu verwenden anstatt immer 25 zu schreiben ist, dass wenn wir die Breite verändern wollen wir dies nur ein einziges mal an `w` erledigen müssen und alle weiteren Verwendungen von `w` werden angepasst.  
Als nächstes folgt bereits die nächste Subfunktion mit einem Parameter und einem Rückgabewert. In Javascript werden alle Variablen mit `var` deklariert. Die Unterscheidung des Types findet erst bei der Verwendung statt. Deshalb können wir schreiben.  

	var allImages = loadFiles("*.jpg");

Damit die Funktion auch vorhanden ist fügen wir sie hinter `main()` an.
Unser Code sieht also wie folgt aus.  

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

Den Rückgabewert werden wir noch verändern, denn wir wollen Bilder laden und nicht 0. Wie oben zu sehen ist erhält `loadFiles` den Parameter `type`. Dies ist der Dateityp der später geladen werden soll. `type` is genau wie `w` und `allImages` eine Variable nur das wir im Parameter Block der Funktion das `var` weglassen können.  
Wenn wir `*.*` schreiben würden würde unsere Funktion jeden Dateityp laden. Der Einfachheit halber beschränken wir uns auf jpg da wir wissen das InDesign jpg-Dateien laden und platzieren kann.  
Als nächstes begeben wir uns in die Funktion `loadFiles` und betrachten die Dateihandhabung und eine Benutzerinteraktion. Basierend auf dem Ergebnis der Interaktion fällt das Skript eine konditionale Entscheidung ob es weiter arbeiten soll oder ob es die Funktion `loadFiles` beendet.  

	var theFolder = Folder.selectDialog ("Choose the FOLDER");
	if(!theFolder){ 
			return;
			};

Bisher waren alle Befehle JavaScript Befehle. Der Befehl `Folder.selectDialog ("Choose the FOLDER")` jedoch ist ExtendScript. das Objekt `Folder` hat eine eigene Funktion `selectDialog(parameter)`. Wir müssen diese Funktion nicht betrachten. Wir müssen nur wissen, dass sie ein Interface öffnet und dem Benutzer die Möglichkeit gibt einen beliebigen Ordner auszuwählen. Der Parameter ist der Text der auf dem Auswahldialog oben zu sehen ist. Der gewählte Ordner wird dann in der neuen Variable `theFolder` für eine spätere Referenzierung gespeichert. Dann folgt das Konstrukt der Konditionalen Abfrage `if(Statment){Do Something}`. Sie besagt, dass wenn die Aussage in der runden Klammer war ist die geschwungene Klammer ausgeführt wird. in unserem Fall wird durch das `!` die Aussage negiert. Ausgeschrieben könnte dort stehen `if(theFolder == false)` oder `if(theFolder != true)` die Schreibweise `if(!theFolder)` ist einfach nur verkürzt. Wenn wir  `if(theFolder)` schreiben würden würde das `if(theFolder==true)` entsprechen. Zu Beachten ist nicht `=` zu schreiben. Dies bedeutet "ist gleich", `==` bedeutet "entspricht". Gesprochen wäre unsere Aussage: "Wenn der Ordner nicht wahr ist beende die Funktion".  
Als nächstes betrachten wir was das Laden der Dateien aus unserem Ordner.  

	var allImages = theFolder.getFiles(type);

Ordner Objekte (Folder) haben eine weiter enigebaute Funktion: `getFiles(parameter)`. Diese hat auch einen Parameter den Dateityp. Hierbei wird nicht nur eine einzelne Datei zurückgegebn sondern eine Sammlung aller Dateien des angegebenen Typs. Dies ist ein Array. Ein Array sollte man sich als eine Liste vorstellen deren Positionen über einen Index aufgerufen werden können. Hierbei ist zu beachten das das erste Objekt in der Liste nicht mit 1 sondern mit 0 angesprochen wird. Also ist `allImages[0]` das erste Bild unserer Liste.
Nun folgt ein weitere Sicherheitscheck ob wir Bilder gefunden haben und die Bestimmung des Rückgabewerts unsere Funktion. Ebenfalls wird der Nutzer wenn es keine Bilder gibt darauf hingewiesen.

	if((allImages.length < 1) || (allImages == null) ){		alert("There are no images");
	return null;	   
	}else{
	return allImages;
	};

Wie wir oben sehen benutzen wir nochmals die Konditionale Entscheidung `if()`. jedoch mit einer Erweiterung dem `else`. Dies bedeutet das auf jeden Fall eine er beiden geschwungene Blöcke ausgeführt wird. Um es im Pseudocode darszustellen: "Wenn Aussage zutrifft mach dies ansonsten mach dass". Innerhalb unsere runden Aussage Klammer haben wir mehrere Aussagen verknüpft. wir haben also 2 Aussagen. Mit dem `||` sagen wir entweder oder. In unserem Fall ist das einmal der Check ob wir mindestens ein Bild haben `(allImages.length < 1)`. `length` ist eine Eigenschaft jedes Arrays und gibt wenn wir ein Bild haben 1 zurück. Wenn es einhundert sind 100. Wir fragen also ob die länge von unserer Liste kleiner als 1 ist. Diese Aussage verbinden wir mit `||` dies bedeutet "oder". Wenn also Aussage 1 oder Aussage 2 zutreffen führe den ersten Block aus. Wenn wir beide Aussagen Abfragen wollten müssten wir `&&` schreiben. Dies würde nur den ersten Block ausführen wenn beide Aussagen zutreffen. In unserem zweiten Aussage fragen wir nach `null`, dies ist etwas ähnliches wie nichts. Also wenn wir einen Fehler beim Laden der Bilder hatten oder `allImages` nicht existiert. Im ersten Block beenden wir nur die Funktion. Wenn keine der beiden Aussagen zutrifft sollten wir eine Liste von Bildern haben und diese geben wir mit `return allImages` an unsere Funktion `main` zurück.
  
Wir befinden uns wieder in der Funktion main und werden einen weiter Abfrage starten.

	if(allImages == null) return;

Wenn `loadImages` `null` zurückgibt brich das Skript ab. Dies ist nötig da `loadImages` in der Funktion `main` statfindet. Also führt ein `return` in `loadImages` nur zurück nach `main` und nicht zum beenden des Skripts. Hier ist ebenfalls eine verkürzte schreibweise zu sehen. Wir können uns die geschwungenen Klammern sparen wenn wir nur einen einzigen Befehl haben. Das heisst `if(statement){doSomething;}` enspricht `if(statement) doSomething`. Ebenfalls könnte `if(statement){doSomething;}else{doSomethingElse;}` als `if(statement) doSomething; else doSomethingElse;` abgekürzt werden. Dies geht jedoch nur bei jeweils einem Befehl nach der Aussage.  
Als nächstes folgt die Berechnung unserer Seiten Weite und Seiten Höhe. Die Höhe wird nochmals mit einer Kondition überprüft. Wenn die Menge an Bildern nicht in ein Matrix passt, also 3 mal 3 oder 4 mal 4 oder 100 mal 100 müss die Höhe nochmals um eine Zeile erweitert werden. Hier kommt das JavaScript Objekt `Math` zum Einsatz.   

	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2);
	var ph = pw;
	if(Math.round(Math.sqrt(allImages.length)) != Math.sqrt(allImages.length)){
	        ph = pw + w;
	}

Dies wirkt komplizert. Um es zu Verstehen lösen wir den ersten Satz einmal auf.
a ist gleich 16. Die Menge an Bildern.  
b ist die Wurzel aus a. Wir wollen es rechteckig. Also 4.  
c ist b gerundet. Falls es eine Kommazahl ist. Bleibt in diesem Fall 4, wenn a 16 ist.  
d ist 25. Die Breite der Bilder.  
e ist c mal d. Wir staffeln die Bilder nach rechts. 4×25 also 100  
f ist d mal 2. Das ist Links und Rechts der Abstand zum Seitenrand.Jeweils eine Bildbreite. Also 50  

Also ist unsere Seitenweite 150  
Die Breite der Bilder mal der auf- oder abgerundeten Wurzel aus der Menge an Bildern plus eine Bildbreite links und eine rechts.  
oder    
g = [√a] × d + (d × 2)  
oder  

	var pw = Math.round(Math.sqrt(allImages.length)) * w + (w*2);  

Danach setzen wir die Höhe der Seite gleich der Breite.
Für den Fall das b eine Fliesskommazahl ist und wir eine nicht rechteckige Matrix erzeugen wollen, also alle Bilder platziert werden sollen, müssen wir die Höhe der Seite um eine Zeile Bilder erweitern. Deshalb vergleichen wir in dem `if(statement)` ob die gerundete Quadratwurzel kleiner als die Quadratwurzel ist. `(Math.round(Math.sqrt(allImages.length)) < Math.sqrt(allImages.length)`  
oder  
[√a] ≠ √a  
oder  
Wenn die Wurzel aus der Menge an Bilder nicht der gerundeten Wurzel aus der Menge an Bildern entspricht ist die Seitenhöhe die Seitenbreite plus eine Bildbreite. Wenn a also 17 ist wäre die Seite 150 breit und 175 hoch.  
  
ich vermeide hier um es nicht noch weiter zu verkomplizieren jede Art von Maßeinheit. Das lassen wir InDesign selber regeln. In der Standarteinstellung sind es Millimeter. Dies könnten wir defineren müssen wir aber nicht. Da InDesign immer eine Grundeinstellung hat.  
Als nächstes folgen das erzeugen des Dokuments, das einstellen der Seite auf unsere errechneten Werte und das überführen der ersten Seite im Dokument in eine Variable.  

	var doc = app.documents.add();
	    doc.documentPreferences.pageWidth = pw;
	    doc.documentPreferences.pageHeight = ph;
	var page = doc.pages.item(0);
	var y = w;
	var x = w;

Diese Zeilen sind fast selbst erklärend. Wir fügen der Sammlung an Dokumenten ein neues hinzu. Dabei ist irrelevant ob bereits ein Dokument existiert oder nicht. Dann stellen wir die Weite und Höhe der Seite ein. Dann nehmen wir aus der Sammlung and Seiten in dem neuem Dokument die Erste. Der Aufruf `item(0)` ist ebenfalls ein ExtendScript Befehl der nur in InDesign funktioniert. wir könnten auch `var page = doc.pages[0]` schreiben. Hier funktioniert beides gleich. Das ist jedoch nicht immer der Fall. Es gibt zum Beispiel die Möglichkeit `doc.pages.middleItem()` oder `doc.pages.lastItem()` abzufragen. Bei einem normalen Array wie unserem `allImages` würde `lastItem()` nicht funktionieren. Danach erzeugen wir die Startpunkt unseres ersten Bildes. x und y sind jeweils eine Bildbreite.
Ebenfalls gäbe es noch die Möglichkeit die ersten drei Zeilen abzukürzen.  
`var doc = app.documents.add({documentPreferences:{pageWidth:pw,pageHeight:ph}});`
Aber zu dieser Schachtelung kommen wir noch. Wir sind bereits halb durch. Es folgt nochmals ein Weiteres Konstrukt. die Schleife.  

	for(var i in allImages){
	var rect = page.rectangles.add({geometricBounds:[y, x, y + w,x + w]});
	rect.place(allImages[i] );
	rect.fit(FitOptions.CONTENT_TO_FRAME);
	x +=w;
	}

Mit dieser Schleife würden wir nur Bilder nach rechts weiter setzen. Den "Zeilenumbruch" fügen wir später ein. Ersteinmal die Aussage der Schleife ähnelt der Kondition `for(statment){doSomething}` nur mit `for` anstatt `if`. Es könnte als an solange übersetzt werden. Solange du durch die Liste der Bilder zählen kannst.Die Aussage `for(var i in allImages)` ist  eine verkürzte schreibweise für `for(var i = 0; i < allImages.length; i = i + 1 )` oder `for(var i = 0; i < allImages.length; i++ )`. Der Große Unterschied ist nur das mit der von mir verwendeten Variante wir die Möglichkeit einbüßen das wir zum Beispiel nicht bei 0 starten sondern bei 5 und wir grössere schritte machen könnten. Es wäre also auch möglich `for(var i = 5; i < 100; i= i +5)` zu schreiben. Das Bedeutet. Zähler i ist 5. Solange i kleiner als 100 ist, erhöhe i um 5. Im ersten durchlauf ist i 5 im zweiten 10 im dritten 15. Wir würden dann nur das 5te ,10te und 15te Bild erhalten anstatt alle. Unsere Variante ist ein bisschen schmucker. *FEHLER*
Es folgt:  

	var rect = page.rectangles.add({geometricBounds:[y, x, y + w,x + w]});

Wir erzeugen auf der ersten Seite eine Rechteck, ähnlich wie unser Dokument und stellen die Aussenkanten ein. Die `geometricBounds`. Wir könnten auch folgendes schreiben.  
  
	var rect = page.rectangles.add();
	var y1 = y;
	var x1 = x;
	var y2 = y1 + w;
	var x2 = x1 + w;
	rect.geometricBounds = [y1, x1, y2, x2];
  
Die Eigenschaft `geometricBounds` erwartet immer ein Array mit 4 Stellen. Diese geben die Linke obere Ecke und die Rechte untere Ecke an. Immer von der Oberen beziehungswiese linken Kante der Seite gemessen. Hierbei steht die y Koordinate vor der x Koordinate. Zu beachten ist auch das innerhalb von `add()` ein Doppelpunkt anstatt eines Gleichheitszeihens bei der Zuweisung des Wertes verwendet werden muss.  
Es folgen drei einfache Befehle.  
  
	rect.place(allImages[i] );
	rect.fit(FitOptions.CONTENT_TO_FRAME);
	x +=w;
  
Das Bild mit dem Index i wird in dem Rechteck platziert, der Inhalt wird an die Grösse des Rechteckes angepasst und wir erhöhen den x Wert um eine Bildbreite.Hier könnte auch `x = x + w` stehen. Da wir in unserer Schleife sind passiert dies für die komplette Menge der Bilder unabhängig davon ob wir 5, 100 oder 10000 haben. Dies ist eine der großen Stärken von Skripten und Programmen. Die Iteration.  
Damit wir jedoch nicht nur Bilder nach Rechts platzieren sondern umbrechen wenn x (oder x1) größer oder gleich der Breite der Seite minus der Bildbeite*(der Rand) ist müssen wir eine weitere Kondition hinzufügen.  
  
	if(x >= pw - (w)){
	x = w;
	y+= w;
	}
  
Die die es bis hier her geschafft haben sollten diesen Code jetzt entschlüsseln können. Wenn x grösser gleich 150 - 25, um auf unser Beispiel mit der 16 als Menge der Bilder zurückzukommen, setze x zurück auf 25 und addiere auf y 25 auf. die Zahlen reihe ist dann:  
	i = 0
	x = 25
	y = 25  
dann
	i = 1
	x = 50
	y = 25
Das passiert solange bis x 125 ist.  
Dort setzt die Kondition `if(x >= pw - (w))` an.  
x wird in der Kondition zurück auf 25 gesetzt und y wird auf 50 gesetzt.
Dann ist  
	i = 4.
Wir fangen bei 0 an zu Zählen im Array also ist `allImages[4]` das fünfte Bild.
und so weiter und so weiter.  
Wir sind am Ende. Probiere den Code mit unterschiedliche vielen Jpg-Dateien aus verändere ihn mach ihn kaputt und liess die Fehlermeldungen. Dies ist ein weitverbreitetes Problem. Computer und Programme würden viel an ihrer Mystik verlieren wenn einerseits die Nutzer die Meldungen lesen würde anstatt nur auf ok zu drücken und andererseits die Meldungen verständlich geschrieben wären.  
   
Ein weiters Skript _greatPower.jsx_. Dies besteht aus nur einer Zeile und ist doch mächtig und auch ein wenig gefährlich. Wenn bei der Entwicklung eines anderen Skripts immer wieder neue Dokumente erzeugt werden kann es schnell passieren, dass 10, 20, 50 Dokumente geöffnet sind. Die Oberfläche von InDesign bietet nicht die Möglichkeit alle geöffneten Dokumente zu schliessen ohne zu speichern. Das bedeutet das bei 50 Dokumenten 50 mal beim Schliessen entweder gespeichert oder das Dokument verworfen werden muss. Mit greatPower.jsx ist dies möglich. Um dies auszuprobieren erzeugen wir ein paar Dokumente mit dem Skript createDocuments.jsx. Dies is stark verkürzt in seiner schreibweise und verwendet eine andere Art von Schleife. die `while` Schleife.   

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

Um diese Dokumente wieder zu schliessen benutze greatPower.jsx

	// Like Uncle Ben saz: "With great power comes great responsability!"
	app.documents.everyItem().close(SaveOptions.NO);
  
Wenn nun dem ein oder anderem der Gedanke kommt: "Das ist doch alles viel zu kompliziert!" Warum dies mehr Unwille den Unvermögen ist  werde ich versuchen im nächsten Teil zu untersuchen 

##Teil 4 Die Angst
##Teil 5 Ein Werkzeug, Schritt für Schritt
##Fazit 

*HackerTyper: 
**Duden: 
***esoterische Programmiersprachen
****Pseudocode

