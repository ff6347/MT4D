---
layout: twitterbootstraped
title: Werkzeuge
---
<a name="12"></a>
##4Werkzeuge
Wo bleibt die extra Zeit für Gestaltung, die versprochen wurde? Wie bereits erwähnt, braucht das Lernen einer Sprache etwas Zeit. Die Grammatik und Rechtschreibung können aus einem Buch gelernt werden, die Nuancen und Umgangssprache kann jedoch nur durch das Sprechen geschult werden. Zum Glück sind wir dabei nicht alleine. Es gibt bereits viele Werkzeuge, die frei zur Verfügung stehen und zur Optimierung unserer Arbeitsprozesse genutzt werden können. Dies kann von kleinen Helfern wie "greatPower.jsx" bis zu voll ausgearbeiteten Systemen mit eigenen Grafischen Benutzeroberflächen gehen.  
<a name="99"></a>
###4.1 AEMap.jsx & AEMap Utilites.jsx
In diesem Sinne habe ich die Skripte AEMap.jsx und AEMap Utilities.jsx für Adobe After Effects geschrieben, und unter einer Open Source Lizenz ins Netz gestellt.  

[![AEMap](images/aemapuis_thumb.jpg)](images/aemapuis.jpg)
[![AEMap Utilities](images/aemaputilities_thumb.jpg)](images/aemaputilities.jpg)  

Viele Motion-Designer kommen irgendwann einmal an den Punkt, an dem sie eine Weltkarte oder die Aussenkontur eines Landes benötigen. Bisher war es so, dass immer wieder eine Websuche begann nach benutzbaren Kartenmaterial. Hierbei entstehen einige Probleme. Die Rechte an Kartenmaterial, das "einfach so" aus dem Netz gezogen wurde, sind oft ungeklärt. Manchmal sind es Vektor-Dateien, wenn man Pech, hat sind es Pixelbilder. Diese Quelldatei liegt dann innerhalb eines Projektes und wird mit diesem archiviert. Wenn sie wieder benötigt wird, beginnt die Suche aufs Neue, was bei vielen absolvierten Projekten schnell zeitraubend werden kann. After Effects Projekte können schnell aus hunderten Quelldateien bestehen und sind gerne nach persönlichem Gusto sortiert. Was, wenn nicht nur eine Weltkarte benötigt wird, sondern zum Beispiel die Kontur von Ost-Timor und Papua Neu Guinea?  

[![osttimor papua neu ginea](images/ostimorpaua_01_thumb.jpg)](images/ostimorpaua_01.jpg)  

Selbst wenn eine vernünftige Vektor-Form einer Karte existiert und griffbereit isnt wie können die beiden Länder darin gefunden werden? Was ist wenn eine Grenzänderung stattfindet? Und und und. Um diesen Problemen zu entgehen, kann AEMap.jsx eine Weltkarte in Rektangularprojektion erzeugen. Dabei entsteht eine After Effects Komposition in einer gewählten Skalierung (immer 2:1) in der 178 Prä-Kompositionen enthalten sind, die 286 einzelne Polygon-Formen beinhalten.  

[![AEMap Full Composition](images/aemapfullcomp_thumb.jpg)](images/aemapfullcomp.jpg)  

Der Nutzer kann zwischen verschiedenen Einstellungen wählen, zum Beispiel die Karte mit Kontur oder ohne zu zeichnen. Er kann entscheiden, ob alle Polygone auf eine Ebene gezeichnet werden sollen oder ob in die oben genannten Kompositionen gesplittet werden soll. Ebenfalls können 3D-Einstellungen definiert werden und ähnliches mehr. Die Daten bestehen auf einem GeoJson Datensatz, der zum freien Gebrauch ins Netz gestellt wurde. Der gesamte Funktionsumfang ist auf [dieser Webseite](http://fabiantheblind.github.com/AEMap/) dokumentiert. Dieses Skript spart nicht nur mir Zeit, sondern auch anderen. Die Resonanz in der After Effects Community" ist groß. Daher hat das Skript seit seiner Veröffentlichung auf [AEScripts.com](http://aescripts.com/aemap/) am 10 April 2012 bereits über 550 Downloads gehabt (heute 4 Mai 2012). Das Tutorial und das Demo wurden bereits über 5000 mal auf Youtube geladen. Aber genug der Selbstbeweihräucherung. Der Vorteil an solchen und ähnlichen Werkzeugen, die zum Beispiel auf AEScripts.com bereit gestellt werden, ist, dass diese meist aus dem Zwang heraus entstanden, sind einen Arbeitsablauf zu automatisieren, um Zeit zu sparen.  
<a name="98"></a>
###4.2 createBook

Ein weiteres Werkzeug zum Multipublishing, das ich noch nicht umgesetzt habe und auch vielleicht niemals umsetzen werde, wäre folgendes. Zum Schreiben dieser Arbeit benutze ich eine Auszeichnungssprache genannt [Markdown](http://daringfireball.net/projects/markdown/), in einem Editor genannt [iAWriter](http://www.iawriter.com/). <a data-toggle="modal" href="#myModal1" ><i class="icon-asterisk"></i></a>
<div class="modal fade" id="myModal1">
    <script type="text/javascript">$(this).modal('hide');</script>
  <div class="modal-header">
    <button class="close" data-dismiss="modal">×</button>
    <h3>Anmerkung</h3>
  </div>
  <div class="modal-body">
    <p>Die Auszeichnungssprache Markdown wurde von <a href="http://daringfireball.net/">John Gruber</a> entwickelt und erlaubt es in reinen Textdokumenten, Auszeichnungen wie Überschrift 1 oder Zitat zu verwenden, ohne dass der Lesefluss maßgeblich beeinträchtigt wird.</p>
  </div>
</div>
{% highlight text %}  
#Überschrift 1
##Überschrift 2
**Fett** oder __Fett__  
*Italic* oder _Italic_  
{% endhighlight %}  

Der obere Text wird nach dem Übersetzen, durch mein [CSS (Cascading Style Sheets)](http://www.w3schools.com/css/css_intro.asp) gesteuert, so dargestellt:

#Überschrift 1
##Überschrift 2
**Fett** oder __Fett__  
*Italic* oder _Italic_  

Mit iA Writer habe ich einen weissen Bildschirm und bin frei von jedweder Ablenkung. Mit diesem Set (Markdown + iA Writer) bin ich voll auf das Schreiben konzentriert und lasse mich nicht von Layoutaufgaben stören. Um diese Texte in ein lesbare und mit CSS gestaltbare Form zu bringen, benutze ich [Jekyll](http://jekyllrb.com/). Jekyll ist ein in Ruby geschriebener Markup-Übersetzer, der statische .html Dokumente exportiert. Mit einem in Ruby geschriebenem Jekyll Plugin **könnte**, neben dem .html, auch eine für InDesign verständliche Datei erzeugt werden ein: .idml (InDesign Markup Language). Ebenfalls könnte ein .epub (Electronic Publication) oder ein [RSS-Feed (Rich Site Summary)](http://www.whatisrss.com/) erzeugt werden. Alle drei sind offene Standards und basieren auf der [.xml( EXtensible Markup Language)](http://www.w3schools.com/xml/xml_whatis.asp) Formatdefinition.
Diese Pipeline kann mit unterschiedlichen Templates für verschiedenste Formate gesteuert werden. Auch hier gilt, die erzeugten Ergebnisse der Automation sind nicht das Endergebnis, sondern müssen noch weiterverabeitet werden. Es würde jedoch die Datenübertragung erleichtern und mit einer Anweisung in der Kommandozeile `jekyll --server` Rohdaten für verschiedenste Medien erzeugen. <a data-toggle="modal" href="#myModal2" ><i class="icon-asterisk"></i></a>  Diese müssten dann widerum einen Gestaltungsprozess durchlaufen. Leider ist dies nur eine Idee. Um es umzusetzen, müsste ich Ruby, das idml Schema, das epub Schema, mehr über xml, dtd, xslt, xPath, mehr über html und css und wie ich Plugins für Jekyll schreibe, lernen. Bis zum Ende dieser Arbeit ist das nicht zu bewerkstelligen. Aber toll wäre es.  
<div class="modal fade" id="myModal2">
    <script type="text/javascript">$(this).modal('hide');</script>
  <div class="modal-header">
    <button class="close" data-dismiss="modal">×</button>
    <h3>Anmerkung</h3>
  </div>
  <div class="modal-body">
    <p>Mit 4 Befehlen könnte dies schon auf einem Webserver bereitgestellt werden.  

  {% highlight sh %}
  jekyll --server
  git add --all
  git commit -m "This is the message describing the commit"
  git push origin master
  {% endhighlight %}

Damit sind die Daten im Netz verfügbar und können eingesehen werden. Hier könnte ein online Korrektursystem mit differenzierten Nutzerrechten eingebunden werden und und und…</p>
  </div>
</div>

[![pipeline](/images/pipeline_thumb.jpg)](/images/pipeline.jpg)  

Der aktuelle Prozess orientiert sich an dieser Idee, ist jedoch nicht komplett automatisert. Die Markdown Dateien werden mit einem Skript zu einem InDesign Buch zusammengeführt und die Auszeichnungen werden in Absatzformate übersetzt. Alle referenzierten Bilder werden auf den entsprechenden Seiten platziert. Ab diesem Punkt wird der "Feinschliff" des Layouts manuell durchgeführt. Das Übersetzen der Auszeichnung wird durch "Suchen und Ersetzen"-Routinen bewerkstelligt. Dies ist eine rohe Art der Transformation. Es wäre sinnvoller, die Übersetzung nicht mit einem Workaround zu erledigen. Wie bereits oben erwähnt, fehlt jedoch dafür die Zeit.  

<script src="https://gist.github.com/2659939.js?file=createBook.jsx"></script><br>

{% comment %}
[^markdown]: Die Auszeichnungssprache Markdown wurde von [John Gruber](http://daringfireball.net/) entwickelt und erlaubt es in reinem Textdokumenten Auszeichnungen wie Überschrift 1 oder Zitat zu verwenden ohne dass der Lesefluß maßgeblich beeinträchtigt wird.  

[^jekyll]: ?]Mit 4 Befehlen könnte dies schon auf einem Webserver bereitgestellt werden.  

	{% highlight sh %}
	jekyll --server
	git add --all
	git commit -m "This is the message describing the commit"
	git push origin master
	{% endhighlight %}

Damit sind die Daten im Netz verfügbar und können eingesehen werden. Hier könnte ein online Korrektursystem mit differenzierten Nutzerrechten eingebunden werden und und und...  
{% endcomment %}
