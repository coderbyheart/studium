---
layout: post
status: publish
published: true
title: Drucker automatisch passend zum Raum setzen
author:
  display_name: Markus Tacker
  login: m
  email: m@tacker.org
  url: http://tckr.cc/
author_login: m
author_email: m@tacker.org
author_url: http://tckr.cc/
wordpress_id: 542
wordpress_url: http://studium.coderbyheart.de/?p=542
date: '2011-05-17 11:49:23 +0200'
date_gmt: '2011-05-17 09:49:23 +0200'
categories:
- Uncategorized
tags:
- allgemein
- python
comments: []
---
<p><a href="https://github.com/tacker/hsrm-mi-utils/blob/master/printer-autoselect.py">Dieses Python-Script</a> ermittelt anhand des Hostnamens des Rechners, an dem man sich im Fachbereich der Medieninformatik an der Hochschule RheinMain einloggt, den passenden Drucker.</p>
<h3 class="textimage">Installation</h3>
<p>[cc lang="bash"]<br />
wget --no-check-certificate https://github.com/tacker/hsrm-mi-utils/raw/master/printer-autoselect.py -O ~/printer-autoselect.py<br />
chmod +x ~/printer-autoselect.py<br />
echo '~/printer-autoselect.py > /dev/null' >> ~/.bashrc</p>
<p>[/cc]</p>
<p>Anschließend wird das Script nach jedem Login ausgeführt.</p>
