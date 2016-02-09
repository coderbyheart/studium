---
layout: post
permalink: tipp-notices-in-postgresql-unterdrucken
title: 'Tipp: Notices in PostgreSQL unterdrücken'
date: '2011-01-15 21:56:25 +0100'
tags:
- PostgreSQL
- Datenbanken
---
Diese Statement am Anfang eines SQL-Skriptes unterdrückt die Ausgabe von Hinweisen (Notices):

    SET client_min_messages TO 'WARNING';

Die Dokumentation des Features findet sich [hier](http://www.postgresql.org/docs/8.1/static/runtime-config-logging.html).
