---
layout: post
permalink: meine-subversionconfig
title: Meine .subversion/config
date: '2010-10-14 16:15:17 +0200'
tags:
- subversion
- svn
- SoftwareTechnik
---

Das svn-Kommando auf der Kommando-Zeile wird u.a. durch die Datei `~/.subversion/config` konfiguriert.

Meine Einstellungen daraus lauten:

    [helpers]
    diff-cmd = colordiff
    diff-args = --ignore-all-space --ignore-blank-lines
    [miscellany]
    enable-auto-props = yes
    [auto-props]
    * = svn:keywords=Id Rev
