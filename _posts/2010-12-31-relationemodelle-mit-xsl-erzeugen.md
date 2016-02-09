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
</p>
<h3 class="textimage">XML</h3>

    <?xml version="1.0" encoding="UTF-8"?>
    <?xml-stylesheet type="text/xsl" href="relationenmodell.xsl"?>
    <relationmodel>
        <relation>
            <name>Relation</name></p>
    <property primary="true">Primärschlüssel</property>
    <property foreign="true">Fremdschlüssel</property>
    <property>Datenfeld</property>
        </relation>
    </relationmodel>

<h3 class="textimage">XSL</h3>

    <?xml version="1.0" encoding="UTF-8" ?>
    <xsl:stylesheet version="1.0"
        xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
        <xsl:output method="html" indent="yes" />
        <xsl:template match="/relationmodel">
            <html>
                <head>
                    <title>Relationenmodell Auktionsdatenbank 2010db02</title>
    <link rel="stylesheet" type="text/css"
                        href="http://yui.yahooapis.com/3.2.0/build/cssreset/reset-min.css" />
    <link rel="stylesheet" type="text/css"
                        href="http://yui.yahooapis.com/3.2.0/build/cssbase/base-min.css" />
    <link rel="stylesheet" type="text/css"
                        href="http://yui.yahooapis.com/3.2.0/build/cssfonts/fonts-min.css" />
    <link rel="stylesheet" type="text/css" href="relationenmodell.css" />
                </head>
                <body>
    <h1>Relationenmodell Auktionsdatenbank 2010db02</h1>
    <xsl:apply-templates />
                </body>
            </html>
        </xsl:template>
        <xsl:template match="relation">
    <table>
    <tbody>
    <tr>
    <th>
                            <xsl:value-of select="name"></xsl:value-of>
                        </th>
    <xsl:for-each select="property">
                            <xsl:element name="td">
                                <xsl:attribute name="class">
                                <xsl:if test="@primary">primary</xsl:if>
                                <xsl:if test="@foreign">foreign</xsl:if>
                                </xsl:attribute>
                                <xsl:value-of select="."></xsl:value-of>
                            </xsl:element>
                        </xsl:for-each>
                    </tr>
    </tbody>
    </table>
    </xsl:template>
    </xsl:stylesheet>

<p>Und damit es hübsch aussieht, dazu noch ein CSS-File:</p>

    body { margin: 1em 2em; }
    th { background-color: #ccc; font-weight: bold; min-width: 15em; }
    td { min-width: 8em; }
    .primary { text-decoration: underline; }
    .foreign { font-style: italic; }
