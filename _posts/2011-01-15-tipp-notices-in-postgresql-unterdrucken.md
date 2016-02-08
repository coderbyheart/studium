---
layout: post
status: publish
published: true
title: 'Tipp: Notices in PostgreSQL unterdrücken'
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 409
wordpress_url: /?p=409
date: '2011-01-15 21:56:25 +0100'
date_gmt: '2011-01-15 19:56:25 +0100'
categories:
- Uncategorized
tags:
- PostgreSQL
- Datenbanken
comments: []
---
<p>Diese Statement am Anfang eines SQL-Skriptes unterdrückt die Ausgabe von Hinweisen (Notices):</p>
<p>[cc lang="sql]<br />
SET client_min_messages TO 'WARNING';<br />
[/cc]</p>
<p>Die Dokumentation des Features findet sich <a href="http://www.postgresql.org/docs/8.1/static/runtime-config-logging.html">hier</a>.</p>
