---
layout: post
permalink: what-the-foto-api-dokumentation
title: 'What The Foto: API-Dokumentation'
excerpt: "<a href=\"http://www.flickr.com/photos/tacker/sets/72157626379556132/\"><img
  class=\"alignright\" src=\"http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg\"
  alt=\"What The Foto?\" /></a>Ein nicht unerheblicher Teil meiner Arbeit am Projekt
  ist in die Erstellung einer übersichtlichen API-Dokumentation geflossen.\r\n"
date: '2011-07-19 17:36:06 +0200'
tags:
- SoftwareTechnik
- WhatTheFoto
- python
---
<p><a href="http://www.flickr.com/photos/tacker/sets/72157626379556132/"><img class="alignright" src="http://farm6.static.flickr.com/5236/5814600568_a78deedb78_m.jpg" alt="What The Foto?" /></a>Ein nicht unerheblicher Teil meiner Arbeit am Projekt ist in die Erstellung einer übersichtlichen API-Dokumentation geflossen.<br />
<br />
Wichtig war mir dabei, dass beide Teams einen guten Überblick darüber bekommen, welche Schnittstellen es gibt, und welche bereits implementiert sind &mdash; gerade letztere Information war für das Frontend-Team wichtig, damit sie wissen, welche Funktionen serverseitig schon unterstützt werden und mit welcher Funktion man dann dementsprechend im Frontend weiter machen kann.</p>
<h3 class="textimage">XML als Basis</h3>
<p>Ich hatte bereits aus früheren Projekten mit der Dokumentation von APIs zu tun, und habe mich daher als Basis für eine <a href="{{ '/svn/WTF/apidocs/schnittstellen.xml' | prepend: site.baseurl | prepend: site.url }}">XML-Datei</a> entschieden.</p>
<p>Zum Einen kann diese manuell leicht gepflegt werden, und mit einer passenden <a href="{{ '/svn/WTF/apidocs/schnittstellen.xsd' | prepend: site.baseurl | prepend: site.url }}">XSD</a> bekommen Entwickler in einer IDE wie Eclipse auch direkt Fehlermeldungen angezeigt, wenn Sie Angaben eintragen, die nicht korrekt sind.</p>
<p>Zum Anderen &mdash; und dazu ist es leider nicht gekommen &mdash; kann die XML-Datei auch mittels Reflection aus bestehendem Quellcode generiert werden. Im <em>Idealfall</em> hat man im Verlaufe eines Projektes ein sauber dokumentiertes API-Package, dessen JavaDoc in das in der XML verwendete Format transformiert werden kann. Zeitlich sind wir leider nicht soweit gekommen, und so haben die Teams die XML-Datei manuell gepflegt.</p>
<h3 class="textimage">Aufbau der XML-Datei</h3>
<p>Ziel war es, die Schnittstellen-Kommunikation vollständig zu beschreiben, somit werden im ersten Abschnitt der XML-Datei Datentypen definiert. </p>
<p>Zuerst werden <strong>einfache Datentypen</strong> definiert.</p>

    <simpletype name="String">
      <description>Repräsentiert ein String</description>
      <example>Lorem ipsum</example>
    </simpletype>
    <simpletype name="DateTime">
      <description>Repräsentiert ein Datum mit Uhrzeit. Das Format ist YYYY-MM-DDTHH:MM:SS+ZZZZ</description>
      <example>2011-03-28T17:58:23+0001</example>
    </simpletype>

<p>Gefolgt von <strong>Enums</strong>, die in unserem Fall aus jedem der definierten einfachen Datentypen bestehen dürfen.</p>

    <enum name="Sex">
      <description>Repräsentiert das Geschlecht einer Person</description>
      <example>M</example>
      <items>
        <item value="M">
          <description>männlich</description>
        </item>
        <item value="F">
          <description>weiblich</description>
        </item>
      </items>
    </enum>

Anschließend folgen die <strong>komplexen Datentypen</strong>, die in der jeweiligen Implementierung ValueObjects oder Models entsprechen.<br />

    <complextype name="Lightbox" type="Object">
      <description>Repräsentiert eine Lightbox</description></p>
    <property name="id" type="Integer" description="ID der Lightbox">
        <example>28388</example>
      </property>
    <property name="name" type="String" description="Name der Lightbox">
        <example>Projekt2011</example>
      </property>
    <property name="description" type="String" description="Beschreibung der Lightbox">
        <example>Das ist die Beschreibung der Lightbox.</example>
      </property>
    <property name="state" type="LightboxState" description="Aktueller Zustand der Lightbox"/>
    <property name="created" type="DateTime" description="Das Erstellungsdatum"/>
    <property name="modified" type="DateTime" description="Das Datum der letzten Änderung"/>
    </complextype>

Wie man sehen kann, habe ich sehr viel Wert auf eine ausführliche Dokumentation der Elemente wert gelegt. Es gibt zu jedem Typ mindestens eine Beschreibung und dort wo es nötig ist auch ein Beispiel für den Inhalt.</p>
<p>Aus diesen Angaben lässt sich dann eine schöne Übersicht mit allen in der Kommunikation verwendeten Datentypen erzeugen.</p>
<p><a href="{{ '/uploads/2011/07/wtf-api-complextype.png' | prepend: site.baseurl | prepend: site.url }}"><img src="/uploads/2011/07/wtf-api-complextype-500x161.png" alt="" title="What The Foto API Docs Komplexer Datentyp" width="500" height="161" class="alignnone size-medium wp-image-677" /></a></p>
<p>Zu guter letzt werden die <strong>Schnittstellen-Methoden</strong> definiert. Diese sind zuerst thematisch gruppiert, in unserem Fall nach den Bezeichnungen der Entitäten aus dem Domänenmodell, z.B. Agency, Photo, Lightbox, User usw.</p>
<p>Innerhalb dieser Gruppe werden dann die dort verfügbaren Methoden definiert. Es werden alle <strong>Parameter einer Anfrage</strong> beschrieben, wie bei den Datentypen ebenfalls mit ausführlicher Beschreibung und bei Bedarf einen Beispiel, sowie die <strong>Art der Antwort</strong>.</p>
<p>Da wir mit ActiveMQ ein asynchrones Messaging verwenden und es auch Situationen gibt, in denen Ereignisse eintreten, ohne, dass der Client dazu eine Anfrage gestellt hat, werden auch bei manchen Methoden die dazugehörigen <strong>Notifications</strong> beschrieben.</p>

    <group name="Lightbox">
      <description>Enthält Methoden die für Lightboxen benötigt werden.</description>
      <action name="enter" inServer="true" inClient="true" messageType="LB_ENTER">
        <description>Sobald ein Nutzer eine Lightbox öffnet, tritt er ihr bei.</description>
        <request></p>
    <property name="session" type="String" description="Die Session-ID des Benutzers">
            <example>yvwH8WrBWqz3mabw2TDDTYDUSwDC54HC</example>
          </property>
    <property name="lightboxID" type="Integer" description="Die ID der Lightbox">
            <example>34532</example>
          </property>
        </request>
        <response></p>
    <property name="result" type="SuccessMessage" description="Liefert Aussage, ob das Eintreten erfolgreich war."/>
        </response>
        <notification></p>
    <property name="userID" type="Integer" description="userID des Nutzers, der die Lightbox betreten hat">
            <example>234544</example>
          </property>
    <property name="lightboxID" type="Integer" description="Die ID der Lightbox">
            <example>34532</example>
          </property>
        </notification>
      </action>
    </group>

<p>Daraus lässt sich dann im Wiki eine übersichtliche Darstellung der Methode erzeugen. Durch die vorher definierten Datentypen und die korrekte Einhaltung der Reihenfolge in der XML-Datei, kann der Datentyp eines Parameters direkt mit seiner Definition verlinkt werden.</p>
<p>Zusätzlich können noch mit Hilfe der Ticket-Query-Funktionen von Trac dazugehörige Tickets angezeigt werden.</p>
<p><a href="{{ '/uploads/2011/07/wtf-api-lbenter.png' | prepend: site.baseurl | prepend: site.url }}"><img src="/uploads/2011/07/wtf-api-lbenter-500x257.png" alt="" title="What The Foto API Docs Lightbox Enter Methode" width="500" height="257" class="alignnone size-medium wp-image-680" /></a></p>
<p>Die schwarze und weiße Fahne markiert übrigens, dass die Methode von Server und Client fertig implementiert ist. Diese Information ist dann auch in der Seitenleiste der Wiki-Seite (<a href="http://www.flickr.com/photos/tacker/5954159899/sizes/o/in/photostream/">die man hier in voller Größe bewundern kann</a>) einsehbar und bietet so einen schnellen Überblick über den Stand der Implementierung.</p>
<h3 class="textimage">Python-Script zum Anlegen der Wiki-Seite</h3>
<p>Die Wiki-Seite selber wird mit Hilfe eines Cronjobs über die XMLRPC-API von Trac regelmäßig erzeugt.</p>
<p>Dazu liest <a href="{{ '/svn/WTF/apidocs/ApiXML2Trac.py' | prepend: site.baseurl | prepend: site.url }}">dieses Python-Script</a> die XML-Datei aus und erzeugt daraus die Wiki-Seite.</p>
<h3 class="textimage">Fazit</h3>
<p>Die API-Dokumentation wurde vom gesamten Team sehr stark genutzt auch als sehr positiv empfunden. Leider haben wir in der Design-Phase des Projektes versäumt, explizit den Aufbau der Schnittstellen-Klassen zu definieren, wäre diese früher geschehen, hätte man mit Hilfe der XML-Datei einen automatisierten Satz Unit-Tests schreiben können, der so überprüfen kann, ob die dokumentierte Version der Schnittstelle auch mit den tatsächlichen Gegebenheiten übereinstimmt. Dies hätte auch verhindert, dass im Server eine Schnittstelle <em>still</em> geändert wird und der jeweilige Entwickler keine Möglichkeit hat, seine Änderung auf Auswirkungen bezüglich der Schnittstelle zu prüfen &mdash; allerdings hätte dann auch mehr Arbeitsleistung in das reine Testen der Schnittstelle fließen müssen &mdash; und das auf beiden Seiten.</p>
