---
layout: post
permalink: drucker-automatisch-passend-zum-raum-setzen
title: Drucker automatisch passend zum Raum setzen
date: '2011-05-17 11:49:23 +0200'
tags:
- allgemein
- python
---
<p><a href="https://github.com/tacker/hsrm-mi-utils/blob/master/printer-autoselect.py">Dieses Python-Script</a> ermittelt anhand des Hostnamens des Rechners, an dem man sich im Fachbereich der Medieninformatik an der Hochschule RheinMain einloggt, den passenden Drucker.</p>
<h3 class="textimage">Installation</h3>
<p>[cc lang="bash"]<br />
wget --no-check-certificate https://github.com/tacker/hsrm-mi-utils/raw/master/printer-autoselect.py -O ~/printer-autoselect.py<br />
chmod +x ~/printer-autoselect.py<br />
echo '~/printer-autoselect.py > /dev/null' >> ~/.bashrc</p>
<p>[/cc]</p>
<p>Anschließend wird das Script nach jedem Login ausgeführt.</p>
