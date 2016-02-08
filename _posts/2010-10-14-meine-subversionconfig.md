---
layout: post
title: Meine .subversion/config
date: '2010-10-14 16:15:17 +0200'
tags:
- subversion
- svn
- SoftwareTechnik
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
