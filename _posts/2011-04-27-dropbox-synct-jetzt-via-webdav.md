---
layout: post
status: publish
published: true
title: Dropbox synct jetzt via WebDAV
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 524
wordpress_url: /?p=524
date: '2011-04-27 13:09:21 +0200'
date_gmt: '2011-04-27 11:09:21 +0200'
categories:
- Uncategorized
tags:
- Transfer
- Dropbox
- python
comments: []
---
<p><a href="http://db.tt/NYepoPI"><img class="alignright size-full wp-image-553" title="Dropbox" src="/uploads/2011/05/logo.png" alt="Dropbox Logo" width="231" height="60" /></a>Ein Update am Ilias über Ostern hatte zur Folge, dass mein Synchronisations-Script, dass sich mit wget --mirror die Daten zieht, nicht mehr funktionierte.</p>
<p>Heute habe ich das Script dann vollständig auf Python umgestellt und verwende dazu <a href="https://launchpad.net/python-webdav-lib">diese WebDAV-Bibliothek</a>.</p>
<p>Wer mag, kann sich den Quellcode meines Scripts auf github ansehen: <a href="https://github.com/tacker/ilias-webdav-mirror/blob/master/WebdavMirror.py">WebdavMirror.py</a>.</p>
