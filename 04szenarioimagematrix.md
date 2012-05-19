---
layout: twitterbootstraped
title: Szenario image matrix
bodyid: usage
---

<a name="08"></a>
###3.1 Der Einsatz - das Beispiel image matrix

Die Fragen, die sich jetzt stellen, sind folgende: "Wie kommt dies zum Einsatz?", "Wie kann ich das nutzen?".
Es folgt nun das InDesign-Skript "image_matrix.jsx" mit etwas mehr als 40 Zeilen Quelltext. Dieses Skript beinhaltet eine Benutzerinteraktion, Dateihandhabung, das Math Objekt <a data-toggle="modal" href="#myModal1" ><i class="icon-asterisk"></i></a>, Konditionen, eine Schleife, Funktionen, Variablen und es hat einen generativen Charakter. Das Skript erledigt folgende Schritte.
<div class="modal fade" id="myModal1">
    <script type="text/javascript">$(this).modal('hide');</script>
  <div class="modal-header">
    <button class="close" data-dismiss="modal">×</button>
    <h3>Anmerkung</h3>
  </div>
  <div class="modal-body">
    <p>Das <a href="http://www.w3schools.com/js/js_obj_math.asp" target="blank" >Math Objekt</a> ist ein bereits bestehender Teil von JavaScript. Es erledigt solche Aufgaben wie Rundung von Werten oder das Berechnen einer Quadratwurzel.</p>
  </div>
</div>
- Frage den Benutzer nach einem Ordner mit .jpg Dateien.  
- Erzeuge ein quadratisches Dokument dessen Grösse auf der Quadratwurzel der Menge der Bilder basiert und alle Bilder fasst.  
- Platziere alle Bilder.  

  
Kopieren sie den nachstehenden Code und bereiten sie einen Ordner mit einigen Jpg-Bildern vor. Das Skript, das unten beschrieben wird, verarbeitet nur Dateien mit der Endung .jpg . Dateien mit .jpeg oder .JPG als Endung werden ignoriert. Es sollten um die 15 bis 30 sein, damit die Ausführung des Skriptes nicht zuviel Zeit in Anspruch nimmt. Es kann jedoch auch 100, 1000 oder mehr Bilder verarbeiten. Die genaue Menge ist irrelevant. Lesen sie nochmal den Abschnitt [7.08 Was ist Hello World?](10terminologie.html#21) und führen sie das Skript aus. Wenn der Ordnerauswahl-Dialog sich öffnet, wählen sie den Ordner mit den Bildern.
Das gesamte Skript:  

<script src="https://gist.github.com/2651660.js"> </script>
{% comment %}
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
{% endcomment %}

<a name="33"></a>
####3.1.1 Ergebnisse - image matrix
Alle 3 nachfolgenden Bilder sind mit demselbem Skript erzeugt.  
[![matrix 1](images/image_matrix_1_thumb.jpg)](images/image_matrix_1.jpg)  
[![matrix 2](images/image_matrix_2_thumb.jpg)](images/image_matrix_2.jpg)  
[![matrix 3](images/image_matrix_3_thumb.jpg)](images/image_matrix_3.jpg)  

{% comment %}
[^math]: Das Math Objekt ist ein bereits bestehender Teil von JavaScript. Es erledigt solche Aufgaben wie Rundung von Werten oder das Berechnen einer Quadratwurzel.  
{% endcomment %}
