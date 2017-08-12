                                      PODCAST SOCIETY SPECIFICATION
                                      
                                      
    /*
    * Title: Media License
    * Author: Michael McCouman Jr.
    * Version: 0.1.2
    * Specifiyer: PSML
    * Area: XML Episode
    * Date: Aug 12 2017
    * Status: draft
    */                                  

    PS Sound License:

    Diese Angaben im Feed geben Auskunft über die Sound und Audio 
    Lizenzen wie auch die Herkunft der Werke. 


    XML Namespace:

    Der XML Namensraum für das URI Format ist:
    => http://www.podcast-society.org/psp/license

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
            <ps:license version="1.0" xmlns:pssl="http://www.podcast-society.org/psp/sound-license">
                <ps:sound title="Soundflore Intro"
                          mode="intro"                                //intro
                          genre="08"                                  //ID3v1 Genre (optional)
                          producer="Michael McCouman Jr."             //producer
                          producerUrl="http://website-download.tld"   //website
                          license="cc0"                               //sound license
                          licenseUrl="https://creativecommons.org/licenses/by/3.0/de/" //sound license url
                          />
                 <ps:sound title="Soundflore Ending"
                           mode="ontro"                                //outro
                           genre="10"                                  //ID3v1 Genre (optional)
                           producer="Michael McCouman Jr."             //producer
                           prodUrl="http://website-download.tld"       //website url
                           license="cc0"                               //sound license
                           licenseUrl="https://creativecommons.org/licenses/by/3.0/de/" //sound license url
                           />
                 <ps:image title="Spirit Bicture"
                           mode="banner"                               //banner
                           type="image/jpg"                            //mime-type
                           creator="Michael McCouman Jr."              //creator
                           creatorUrl="http://website-download.tld"    //website url
                           license="Copyright by Democast"             //image license
                           licenseUrl="http://democast.tld"            //license url
                            />
                 <ps:image title="Episode 001"
                           mode="poster"                               //poster
                           type="image/png"                            //mime-type
                           creator="Michael McCouman Jr."              //producer, creator ...
                           creatorUrl="http://website-download.tld"    //website url
                           license="Copyright by Democast - 001"       //image license
                           licenseUrl="http://democast.tld/001/"       //license url
                            />
            </ps:license>
        
        </item>
    </channel>
    </feed>

    Links:
    - https://wiki.selfhtml.org/wiki/MIME-Type/%C3%9Cbersicht
    - https://de.wikipedia.org/wiki/Liste_der_ID3v1-Genres
