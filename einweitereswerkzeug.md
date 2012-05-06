Ein weiteres Werkzeug zum Multipublishing, das ich noch nicht umgesetzt habe und auch vielleicht niemals umsetzen werde wäre folgendes. Zum schreiben dieser Arbeit Benutze ich eine Auszeichnungssprache genannt Markdown in einem Editor genannt iAWriter. Diese wurde von John Gruber entwickelt und erlaubt es in reinem Textdokumenten Auszeichnungen wie Überschrift 1 oder Zitat zu verwenden ohne , dass der Leseflu? maßgeblich beeinträchtigt wird. Beispiel
{% highlite js %}
\#Überschrift 1
\#\#Überschrift 2
\*\*Fett\*\* oder \_\_Fett\_\_
\*Italic\* \_Italic\_
{% endhighlite %}
Hiermit bin ich voll auf Text konzentriert und lasse mich nicht von Layoutaufgaben stören. Um diese Texte in ein lesbare und mit CSS gestaltbare Form zu bringen benutze ich Jekyll. Jekyll ist eine in Ruby geschriebener Markdown-Übersetzer der statische .html Dokumente exportiert. Mit einem in Ruby geschriebenem Plugin **könnte** neben dem .html auch eine für InDesign verständliche Datei erzeugt werden ein .idml (InDesign Markup Language). Ebenfalls könnte ein .epub ( electronic publication) erzeugt werden. Beide basieren auf dem .xml Format.  
Diese Pipeline kann mit unterschiedlichen Templates für verschiedenste Formate gesteuert werden. Leider ist dies nur eine Idee. Um es umzusetzen müsste ich Ruby lernen, Das .idml Schema lernen, das .epub Schema lernen und lernen wie ich Plugins für Jekyll schreibe. Dies ist in bis zum Ende dieser Arbeit nicht zu bewerkstelligen. 
Aber toll wäre es.  
