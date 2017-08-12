                                      PODCAST SOCIETY SPECIFICATION
                                      
                                      
    /*
    * Title: Legal Podcast Information
    * Author: Michael McCouman Jr.
    * Version: 0.0.1
    * Specifiyer: PSLI
    * Area: XML Header
    * Date: Aug 12 2017
    * Status: draft
    */                                  

    PS Legal Podcast Information:

    Diese Angaben im Feed geben Auskunft über die gestezlichen Hintergründe 
    bei der Verwendung des Feeds und Website. 

    Es gibt viele Podcaster die ein komerzielles Anbieten verhindern möchten.
    Mit diesen Informationen soll Auskunft über die Möglichen verwendungen gegeben werden.

    XML Namespace:

    Der XML Namensraum für das URI Format ist:
    => http://www.podcast-society.org/pss/project-banner

    Der hier genutzte Prefix für den Namensraum ist "ps:rights"


    Tags und Attribute:
    
    Beinhaltet Angaben zu Verwendungsrechte für Webiste, Feeds, Audiofiles 
    


    Example:

    Dies ist ein einfacher RSS Podcast Feed mit eingebundenen Projekt Banner Informationen:


    <?xml version="1.0" encoding="utf-8"?>
    <rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Democaster</title>
        <atom:link type="text/html" href="http://www.podcast-society.org/de/podcast" />

        <!-- specify right information act -->
        <ps:rights version="1.0" xmlns:ps="http://www.podcast-society.org/pss/right-information-act">
            <ps:right mode="website"
                      type="text/html"
                      href="http://democast.tld" 
                      operator="John Dow"                                 //Website Betreiber
                      name="Ultraschall"
                      right="none"/>
        </ps:rights>
        
        <item>
            ...
        </item>
    </channel>
    </feed>


