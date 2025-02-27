---
layout: post
permalink: alternativer-ansatz-fur-die-php-abgabe
title: Alternativer Ansatz für die PHP-Abgabe
date: '2011-04-27 09:01:00 +0200'
tags:
- webanwendungen
- php
---
<p>Mein ursprünglicher Ansatz zur Umsetzung der ersten Abgabe in Webanwendungen war deutlich komplexer — und damit auch eine Nummer zu kompliziert für mein Team.</p>
<p>Da der Code keine Verwendung für die Abgabe gefunden hat (bis auf ein paar Kleinigkeiten), aber doch ein paar nette Features von PHP verwendet werden, habe ich ihn auf github zur Verfügung gestellt: <a href="https://github.com/tacker/webanwendungen-2011-php-oo">webanwendungen-2011-php-oo</a>.</p>
<p>Ich habe ein paar interessante Features, die in PHP möglich sind,  implementiert:</p>
<ul>
<li>einen Autoloader</li>
<li>einen ORM-Mapper, der die Informationen über die Datenbanktabellen aus Quellcode-Kommentaren der Models zieht und daraus dynamisch</li>
<li>Listing-Objekte erzeugt, die über große Tabellen mittels PDO blättern können und bei dem</li>
<li>mittels Iterator auf die Einträge zugegriffen werden kann.</li>
</ul>
<p>Für die Kernfeatures liegen auch schon Unit-Tests vor, die gut die Verwendung des ORM-Mappers illustrieren.</p>
<p>Zwei ant-Jobs sind auch noch definiert, einen für phpdoc und einen für PHPUnit.</p>
