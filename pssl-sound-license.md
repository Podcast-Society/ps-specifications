                                      PODCAST SOCIETY SPECIFICATION
                                      
                                      
    /*
    * Title: Sound License
    * Author: Michael McCouman Jr.
    * Version: 0.0.1
    * Area: XML Episode
    * Date: Aug 12 2017
    * Status: draft
    */                                  

    PS Sound License:

    Diese Angaben im Feed geben Auskunft über die Sound und Audio 
    Lizenzen wie auch die Herkunft der Werke. 


    XML Namespace:

    Der XML Namensraum für das URI Format ist:
    => http://www.podcast-society.org/psp/sound-license

    Der hier genutzte Prefix für den Namensraum ist "pssl"


    Example:
    
    Dies ist ein einfacher RSS Podcast Feed mit eingebundenen Projekt Banner Informationen:


    <?xml version="1.0" encoding="utf-8"?>
    <rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Democaster</title>
        <atom:link type="text/html" href="http://www.podcast-society.org/de/podcast" />
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
            
            <!-- specify sound license -->
            <pssl:license version="1.0" xmlns:pssl="http://www.podcast-society.org/psp/sound-license">
                <pssl:license title="Soundflore 1"
                              type="intro"                                //intro, outro
                              genre="08"                                  //optional see ID3v1 Genres
                              producer="Michael McCouman Jr."             //producer, creator ...
                              prodUrl="http://website-download.tld"       //website url from sound creator
                              license="cc0"                               //sound license
                              licUrl="https://creativecommons.org/licenses/by/3.0/de/" //sound license url
                              />
                 <pssl:license title="Soundflore 1"
                              type="ontro"                                //intro, outro
                              genre="08"                                  //optional see ID3v1 Genres
                              producer="Michael McCouman Jr."             //producer, creator ...
                              prodUrl="http://website-download.tld"       //website url from sound creator
                              license="cc0"                               //sound license
                              licUrl="https://creativecommons.org/licenses/by/3.0/de/" //sound license url
                              />
            </pssl:license>
        
        </item>
    </channel>
    </feed>

    Links:
    - https://de.wikipedia.org/wiki/Liste_der_ID3v1-Genres
