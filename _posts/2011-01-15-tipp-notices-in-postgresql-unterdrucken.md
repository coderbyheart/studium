---
layout: post
title: 'Tipp: Notices in PostgreSQL unterdrücken'
date: '2011-01-15 21:56:25 +0100'
tags:
- PostgreSQL
- Datenbanken
---
<p>Diese Statement am Anfang eines SQL-Skriptes unterdrückt die Ausgabe von Hinweisen (Notices):</p>
<p>[cc lang="sql]<br />
SET client_min_messages TO 'WARNING';<br />
[/cc]</p>
<p>Die Dokumentation des Features findet sich <a href="http://www.postgresql.org/docs/8.1/static/runtime-config-logging.html">hier</a>.</p>
