                                      PODCAST SOCIETY SPECIFICATION


    /*
    * Title: Color Settings
    * Author: Michael McCouman Jr.
    * Version: 0.0.1
    * Specifiyer: PSCS
    * Area: XML Header
    * Date: Aug 13 2017
    * Status: draft
    */                                  

    PS Color Settings

    Diese Angaben im Feed geben Auskunft über die zu drei
    Standardfarben eines Podcasts.


    XML Namespace:

    Der XML Namensraum für das URI Format ist:
    => http://www.podcast-society.org/pss/PSCS/specification

    Der hier genutzte Prefix für den Namensraum ist "pscs:"


    Example:

    Dies ist ein einfacher RSS Podcast Feed mit eingebundenen Podcast Color Settings:


    <?xml version="1.0" encoding="utf-8"?>
    <rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Democaster</title>
        <atom:link type="text/html" href="http://www.podcast-society.org/de/podcast" />

        <!-- specify color setting -->
        <pscs:settings version="1.0" xmlns:pscs="http://www.podcast-society.org/pss/PSCS/specification">
            <pscs:color hex="#f00"/>
            <pscs:light hex="#e66"/>
            <pscs:dark hex="#a00"/>
        </pscs:settings>

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
