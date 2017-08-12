Title: Podcast-Society Project Banner

Author: Michael McCouman Jr.

Version: 1.0

Status: draft


# PS Project Banner #

DE: Diese Angaben im Feed geben Auskunft über die verwendeten Sources eines Projektes und machen die Verwendungen auch im Feed sichtbar. 

## XML Namespace ##

Der XML Namensraum für das URI Format ist

=> http://www.podcast-society.org/psp/project-banner

Der hier genutzte Prefix für den Namensraum ist "pspb:"

## Vorgesehene Projekte

- ultraschall
- podlove
- podigee
- studio&link
- ...

## Example 

Dies ist ein einfacher RSS Podcast Feed mit eingebundenen Projekt Banner Informationen:

    <?xml version="1.0" encoding="utf-8"?>
    <rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Democaster</title>
        <atom:link type="text/html" href="http://www.podcast-society.org/de/podcast" />

        <!-- specify project banner informations -->
        <pspb:projects version="1.0" xmlns:pspb="http://www.podcast-society.org/psp/project-banner">
            <pspb:project rel="http://ultraschall.fm" 
                         title="Ultraschall" 
                         format="svg"
                         href="http://ultraschall.fm/banner/ultraschall-4.svg" //url is not specifiy
                         version="4.0"/>
            <pspb:project rel="http://podlove.org" 
                         title="Podlove"
                         format="png"
                         href="http://podlove.org/banner/" //url is not specifiy
                         version="4.0"/>
        </pspb:projects>
        
        <item>
            <title>Democast 001</title>
            <link href="http://podlove.org/podcast/1"/>
            <guid isPermaLink="false">
                urn:uuid:7456rfw5-hg32-ie98-9356-0274tw658761
            </guid>
            <pubDate>Fri, 01 Jan 2017 12:23:34 +0000
            </pubDate>
            <description>First episode</description>
            <link rel="enclosure" type="audio/mpeg"
                  length="067549"
                  href="http://democast.tld/podcast/democast001.mp3"/>
            ...
            
        </item>
    </channel>
    </feed>

