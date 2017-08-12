                                      PODCAST SOCIETY PODCAST SPECIFICATION
                                      
                                      
    /*
    * Title: Sound License
    * Author: Michael McCouman Jr.
    * Version: 0.0.1
    * Date: Aug 12 2017
    * Status: draft
    */                                  


# PS Sound License #

DE: Diese Angaben im Feed geben Auskunft über die Sound und Audio Lizenzen wie auch die Herkunft der Werke. 

## XML Namespace ##

Der XML Namensraum für das URI Format ist

=> http://www.podcast-society.org/psp/sound-license

Der hier genutzte Prefix für den Namensraum ist "pssl:"

## Angaben



## Example 

Dies ist ein einfacher RSS Podcast Feed mit eingebundenen Projekt Banner Informationen:

    <?xml version="1.0" encoding="utf-8"?>
    <rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Democaster</title>
        <atom:link type="text/html" href="http://www.podcast-society.org/de/podcast" />

        <!-- specify sound lizense -->
        <pssl:license version="1.0" xmlns:pspb="http://www.podcast-society.org/psp/sound-license">
            <pssl:license title="Soundflore 1"
                          type="Intro"                                //Intro, Outro
                          genre="08"                                  //optional more: https://de.wikipedia.org/wiki/Liste_der_ID3v1-Genres
                          creator="Michael McCouman Jr."              //producer, creator ...
                          href="http://website-download.tld"          //website url
                          lic="cc0"                                   //license
                          />
        </pssl:license>
        
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

