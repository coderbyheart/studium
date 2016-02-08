---
layout: post
title: Was ich an Django so mag
date: '2012-01-27 09:45:51 +0100'
tags:
- python
- mobile computing
---
<p>Nachdem ich im dritten Semester zum ersten Mal intensiveren Kontakt mit Python hatte, habe ich die Sprache in den vergangenen Semestern immer stärker schätzen gelernt.</p>
<p>In diesem Semester setzen wir für die Server-Komponente unseres Mobile-Computing-Projekts ebenfalls auf Python, und zwar in Form des Web-Frameworks <a href="https://www.djangoproject.com/">Django</a>. Und das ist wirklich ein Genuss.</p>
<p>Zur Implementierung des Servers lieferte Django bereits alle notwendigen Komponenten. Das Framework bietet den besonderen Vorteil, dass die typischen Aufgaben einer Webanwendung, deren Hauptaufgabe die Verwaltung von Datensätzen ist, also deren Auflisten, Anzeigen, Finden und Editieren (CRUD), nach Erstellung von nur wenig eigenem Code bereits komfortabel zur Verfügung stehen. Es muss lediglich die Datenstruktur in Form von Models definiert werden. Anhand dieser Informationen kann Djongo schon die nötige Datenbankstruktur erzeugen und passende Formulare zum Editieren der Datensätze im mitgelieferten Admin-Bereich erzeugen.</p>
<p>Zur Implementierung der öffentlichen Schnittstellen der Anwendung reichen auch lediglich wenige Zeile Code aus. In Django werden diese mithilfe der Views erstellt, wobei man hier nur Ausnahmen behandeln muss, die über das Anzeigen von einzelnen Datensätzen oder Listen von Datensätzen hinaus gehen. Die für die App zur Verfügung gestellt API wird ebenfalls mit Hilfe der Views erzeugt, wobei dann das Antwort-Format nicht HTML ist, sondern JSON. Die Unterscheidung wird anhand das Accept-Headers in der Anfrage getroffen. Um die Implementierung eines eigenen Controllers muss man sich nicht kümmern, hier übernimmt das Framework bereits alle nötigen Aufgaben, sofern man die vorgegebenen Konventionen befolgt und die bereitgestellten Hilfsfunktionen verwendet.</p>
<p>Auch die Möglichkeit zum Testen seiner Anwendung sind genial, das Test-Framework kümmert sich um alle Aufgaben, lediglich die Unit-Tests muss man selber schreiben - was elegant von der Hand geht, dank einem mitgelieferten Test-Client der URL-Request simuliert.</p>
<p>Django nimmt einem durch viele Konventionen unheimlich viel Arbeit ab, und man kann sich auf das Wesentliche konzentrieren. Die Geschwindigkeit, mit der man in Django entwickeln kann ist beeindruckend und ich bin schwer am Überlegen, es auch für meine Thesis ein zu setzen...</p>
