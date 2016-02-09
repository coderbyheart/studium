---
layout: post
permalink: projektergebnis-mobile-computing
title: Projektergebnis Mobile Computing
excerpt: "<a href=\"https://market.android.com/details?id=de.hsrm.mi.mobcomp.y2k11grp04\"><img
  class=\"size-medium wp-image-951\" title=\"GroupMood im Android Market\" src=\"/uploads/2012/02/logo-500x137.png\"
  alt=\"GroupMood\" width=\"500\" height=\"137\" /></a>\r\n\r\nDas Projektergebnis
  des Kurses Mobile Computing ist neben einer App auch die Erkenntnis, dass die Entwicklung
  unter Android wirklich Spaß macht — etwas das ich zu Beginn des Kurses vor etwas
  mehr als vier Monaten nicht erwartet hatte. Die Platform vereinigt nämlich einige
  Einschränkungen, die in der Kombination aber zu gutem und überlegten Programmieren
  führen. \r\n"
date: '2012-02-22 16:42:49 +0100'
tags:
- android
- mobile computing
- mobile
---
<p><a href="https://market.android.com/details?id=de.hsrm.mi.mobcomp.y2k11grp04"><img class="size-medium wp-image-951" title="GroupMood im Android Market" src="/uploads/2012/02/logo-500x137.png" alt="GroupMood" width="500" height="137" /></a></p>
<p>Das Projektergebnis des Kurses Mobile Computing ist neben einer App auch die Erkenntnis, dass die Entwicklung unter Android wirklich Spaß macht — etwas das ich zu Beginn des Kurses vor etwas mehr als vier Monaten nicht erwartet hatte. Die Platform vereinigt nämlich einige Einschränkungen, die in der Kombination aber zu gutem und überlegten Programmieren führen.<br />
<a id="more"></a><a id="more-950"></a><br />
Zum einen muss der, im Vergleich zu aktuellen Deskop-Computern, schlechten Rechenleistung Rechnung getragen werden. Jede aufwändigere Rechenoperation macht sich direkt im UI bemerkbar — man kommt also um Threading und arbeiten mit Prozessen nicht herum. Die zweite Einschränkung ist die Größe des Displays eines Smartphones und die Größe des menschlichen Zeigefingers. Dank der Touch-Bedienung kommt man mit kleinen Text-Links nicht weit, da müssen schon „riesige“ Buttons zum Einsatz kommen. Aufgrund der Größenbeschränkung bekommt man auch bei weitem nicht so viele GUI-Elemente auf einen Screen, wie z.B. auf einer Website — hier macht man sich viel eher Gedanken darüber, was wirklich wichtig ist und auf was man nicht eigentlich verzichten kann. Vom pixelgenauen Layouten muss man sich sowieso verabschieden. Im Android SDK ist zudem die Trennung zwischen GUI (XML-Layouts), Middleware (Activities) und Backend (ContentProvider, Services) so hart, dass sich prima im Team entwickeln lässt. Die XML-Layouts sind ein Traum, was Anpassbarkeit angeht und die einfache Möglichkeit, leicht zwischen GUI und Business-Logik zu trennen, beugt unbeabsichtigten Durchbrüchen zwischen den Anwendungsschichten vor. Leider hatte ich keine Zeit mich mit dem <a href="http://developer.android.com/guide/developing/tools/monkeyrunner_concepts.html">MonkeyRunner</a> zu beschäftigen, das werde ich aber versuchen beim nächsten Android Projekt nachzuholen, dass es definitiv geben wird.</p>
<p>Und nun zu unserer App. Meine Grundidee war die Möglichkeit zu haben, direkt in einer Vorlesung den Vortragenden bewerten zu können, z.B. um anonym mitzuteilen, dass er zu schnell redet oder zu leise. Aus dieser Idee hat sich dann in den letzten Monaten ein etwas allgemeinerer Ansatz entwickelt:</p>
<blockquote><p><em>GroupMood</em> ist eine Anwendung für Android und ermöglich es, eine Gruppen von Personen schnell und direkt mit Hilfe ihres Smartphones zu befragen.</p></blockquote>
<p>Eine detailliertere Beschreibung findet sich im <a href="https://github.com/tacker/GroupMood/wiki">Wiki auf der GitHub-Projektseite</a>, deswegen erspare ich mir hier die ausführlich Beschreibung. Für einen kurzen Überblick empfehle ich die folgende Präsentation:</p>
<p><iframe src="https://docs.google.com/presentation/embed?id=1M5Z04kyn0yU7hcAAPQBNGXqUFwsZrGdTiWjuwfGsB_A&amp;start=false&amp;loop=false&amp;delayms=3000" frameborder="0" width="480" height="388"></iframe></p>
<p>Die Server-Komponente habe ich übrigens in Django umgesetzt. Auch das hat mir einige „OMG! Wie geil!“-Momente, über die habe ich aber schon <a href="{{ '/was-ich-an-django-so-mag' | prepend: site.baseurl | prepend: site.url }}">an anderer Stelle</a> geschrieben.</p>
