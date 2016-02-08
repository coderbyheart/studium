---
layout: post
status: publish
published: true
title: Meine .subversion/config
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 340
wordpress_url: http://studium.coderbyheart.de/?p=340
date: '2010-10-14 16:15:17 +0200'
date_gmt: '2010-10-14 14:15:17 +0200'
categories:
- Uncategorized
tags:
- subversion
- svn
- SoftwareTechnik
comments: []
---
<p>Das svn-Kommando auf der Kommando-Zeile wird u.a. durch die Datei <code>~/.subversion/config</code> konfiguriert.</p>
<p>Meine Einstellungen daraus lauten:</p>
<p>[cc][helpers]<br />
diff-cmd = colordiff<br />
diff-args = --ignore-all-space --ignore-blank-lines</p>
<p>[miscellany]<br />
enable-auto-props = yes</p>
<p>[auto-props]<br />
* = svn:keywords=Id Rev[/cc]</p>
