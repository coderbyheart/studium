---
layout: post
title: Dateien in der Dropbox löschen
date: '2012-07-19 09:31:09 +0200'
tags: []
---
<p><a href="http://db.tt/NYepoPI"><img class="alignright size-full wp-image-553" title="Dropbox" src="/uploads/2011/05/logo.png" alt="Dropbox Logo" width="231" height="60" /></a><a href="/kleines-update-am-read-mi-zu-dropbox-sync">Inzwischen wird verhindert</a>, dass Dateien aus der Dropbox gelöscht werden. Manchmal will man das aber doch und bis jetzt war es nur durch mich möglich. Jetzt habe ich eine Möglichkeit implementiert, mit der das jeder, der Zugriff auf die Dropbox hat, das selber machen kann.</p>
<p>Es genügt an den Dateinamen der Datei oder den Ordner ".delete" anzuhängen. Dann wird diese Datei durch einen stündlichen Cronjob gelöscht.</p>
