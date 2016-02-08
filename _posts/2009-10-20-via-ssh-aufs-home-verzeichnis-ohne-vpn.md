---
layout: post
status: publish
published: true
title: Via ssh aufs Home-Verzeichnis (ohne VPN)
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 41
wordpress_url: /?p=41
date: '2009-10-20 10:38:59 +0200'
date_gmt: '2009-10-20 08:38:59 +0200'
categories:
- Uncategorized
tags:
- allgemein
- IT
comments:
- id: 24
  author: Til
  author_email: tilmanpotthof@online.de
  author_url: http://twitter.com/chapter_29
  date: '2009-11-02 11:47:36 +0100'
  date_gmt: '2009-11-02 09:47:36 +0100'
  content: "SSH, SCP, SFTP geht alles ohne VPN. Allerdings bietet der login1-Rechner
    ausschließlich Zugriff auf das File-System.\r\n\r\nSpannender wird es wenn man
    vom login1 aus noch eine weitere ssh-Verbindung zum linux001.intern.mi.hs-rm.de
    aufbaut. Dieser Rechner ist von außen nicht sichtbar undhat sämtliche Commandline-Tools
    installiert die in der FH verfügbar sind."
---
<p><code>ssh username@login1.mi.hs-rm.de</code></p>
<p>Mittels SSH, und damit auch mit guten FTP-Clients wie <a href="http://filezilla.sf.net/">FileZilla</a>, kommt man ohne das nervige VPN auf sein Home-Dir.</p>
<p>Alle Infos dazu finden sich im entsprechenden <a href="http://www-intern.informatik.fh-wiesbaden.de/doku/login/getdatafromfbi.pdf">HowTo auf dem MI-Portal</a>.</p>
