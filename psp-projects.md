Title: Podcast-Society Project Banner
Author: Michael McCouman Jr.
Version: 1.0
Tags: podcast-society, podcast, chapters, feeds, atom, rss
Status: Current

# PS Project Banner #

Die Angaben zum 

## XML Namespace ##

Der XML Namensraum für das URI Format ist

=> http://www.podcast-society.org/psp/project-banner

Der hier genutzte Prefix für den Namensraum ist "pspb:"


This is an simple example of a RSS podcast feed with
embedded chapter information in Podlove Simple Chapter
format:

<?xml version="1.0" encoding="utf-8"?>
<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Podlove Podcast</title>
        <atom:link type="text/html"
                   href="http://podlove.org/"/>

        <psp:projects version="1.0" xmlns:psp="http://www.podcast-society.org">

            <check if="{{@project == 'ultraschall'}}">
                <psp:project match="http://ultraschall.fm" title="Ultraschall" version="4.0"/>
            </check>
            <check if="{{@project == 'podlove'}}">
                <psp:project match="http://podlove.org" title="Podlove Webplayer" version="4.0"/>
            </check>

        </psp:projects>

        <!-- specify projcet banner informations -->
        <psp:projects version="1.2" xmlns:psc="http://www.podcast-society.org/psp/project-banner">
            <psp:project match="http://ultraschall.fm" title="Ultraschall" version="4.0"/>
            <psp:project match="hhttp://podlove.org" title="Podlove" version="4.0"/>
        </psp:projects>
        
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

