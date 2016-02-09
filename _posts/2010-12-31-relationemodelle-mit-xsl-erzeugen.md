---
layout: post
permalink: relationemodelle-mit-xsl-erzeugen
title: Relationemodelle mit XSL erzeugen
excerpt: "Für unser <a href=\"/tag/Datenbanksysteme\">Datenbank-Projekt</a>
  habe ich ein XML-Stylesheet geschrieben, dass aus einer einfachen XML-Datei ein
  schönes Relationenmodell erzeugt.\r\n\r\n<img src=\"/uploads/2010/12/2010-12-31-115.png\"
  alt=\"Relationemodelle mit XSL erzeugen\" title=\"2010-12-31-115\" width=\"500\"
  class=\"alignnone size-full wp-image-402\" />\r\n"
date: '2010-12-31 15:40:14 +0100'
tags:
- XML
- Datenbanksysteme
---
<p>Für unser <a href="{{ '/tag/Datenbanksysteme' | prepend: site.baseurl | prepend: site.url }}">Datenbank-Projekt</a> habe ich ein XML-Stylesheet geschrieben, dass aus einer einfachen XML-Datei ein schönes Relationenmodell erzeugt.</p>
<p><img src="/uploads/2010/12/2010-12-31-115.png" alt="Relationemodelle mit XSL erzeugen" title="2010-12-31-115" width="500" class="alignnone size-full wp-image-402" /><br />
<a id="more"></a><a id="more-394"></a></p>
<h3 class="textimage">XML</h3>
<p>[cc lang="xml"]<br />
<?xml version="1.0" encoding="UTF-8"?><br />
<?xml-stylesheet type="text/xsl" href="relationenmodell.xsl"?><br />
<relationmodel><br />
	<relation><br />
		<name>Relation</name></p>
<property primary="true">Primärschlüssel</property>
<property foreign="true">Fremdschlüssel</property>
<property>Datenfeld</property>
	</relation><br />
</relationmodel><br />
[/cc]</p>
<h3 class="textimage">XSL</h3>
<p>[cc lang="xml"]<br />
<?xml version="1.0" encoding="UTF-8" ?><br />
<xsl:stylesheet version="1.0"<br />
	xmlns:xsl="http://www.w3.org/1999/XSL/Transform"><br />
	<xsl:output method="html" indent="yes" /><br />
	<xsl:template match="/relationmodel"><br />
		<html><br />
			<head><br />
				<title>Relationenmodell Auktionsdatenbank 2010db02</title></p>
<link rel="stylesheet" type="text/css"<br />
					href="http://yui.yahooapis.com/3.2.0/build/cssreset/reset-min.css" />
<link rel="stylesheet" type="text/css"<br />
					href="http://yui.yahooapis.com/3.2.0/build/cssbase/base-min.css" />
<link rel="stylesheet" type="text/css"<br />
					href="http://yui.yahooapis.com/3.2.0/build/cssfonts/fonts-min.css" />
<link rel="stylesheet" type="text/css" href="relationenmodell.css" />
			</head><br />
			<body></p>
<h1>Relationenmodell Auktionsdatenbank 2010db02</h1>
<p>				<xsl:apply-templates /><br />
			</body><br />
		</html><br />
	</xsl:template><br />
	<xsl:template match="relation"></p>
<table>
<tbody>
<tr>
<th>
						<xsl:value-of select="name"></xsl:value-of>
					</th>
<p>					<xsl:for-each select="property"><br />
						<xsl:element name="td"><br />
							<xsl:attribute name="class"><br />
							<xsl:if test="@primary">primary</xsl:if><br />
							<xsl:if test="@foreign">foreign</xsl:if><br />
							</xsl:attribute><br />
							<xsl:value-of select="."></xsl:value-of><br />
						</xsl:element><br />
					</xsl:for-each><br />
				</tr>
</tbody>
</table>
<p>	</xsl:template><br />
</xsl:stylesheet><br />
[/cc]</p>
<p>Und damit es hübsch aussieht, dazu noch ein CSS-File:</p>
<p>[cc lang="css"]<br />
body { margin: 1em 2em; }<br />
th { background-color: #ccc; font-weight: bold; min-width: 15em; }<br />
td { min-width: 8em; }<br />
.primary { text-decoration: underline; }<br />
.foreign { font-style: italic; }<br />
[/cc]</p>
