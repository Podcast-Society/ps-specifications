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

    Der hier genutzte Prefix für den Namensraum ist "psli:rights"


    Tags und Attribute:
    
    Beinhaltet Angaben zu Verwendungsrechten der Website, Feeds, Cover, Poster, Images & Audiofiles 
    
    Website:
     - mode: website
     - type: text/html
     - name: name of the podcast
     - url: URL of the website
     - operator: name of producer
     - right: 
          - N/A: Inhalt darf / darf nicht...
    
    Feeds:
     - mode: feed
     - type: application/rss+xml
     - name: name (podcast feed) 
     - url: URL of the feed
     - page: name (podcast)
     - right: 
          - N/A: Inhalt darf / darf nicht...
    



    Example:

    Dies ist ein einfacher RSS Podcast Feed mit eingebundenen Projekt Banner Informationen:


    <?xml version="1.0" encoding="utf-8"?>
    <rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
    <channel>
        <title>Democaster</title>
        <atom:link type="text/html" href="http://www.podcast-society.org/de/podcast" />

        <!-- specify PSLI: legal podcast information -->
        <psli:rights version="1.0">
            <!-- website -->
            <psli:website mode="website"
                          name="Democast"
                          type="text/html"
                          url="http://democast.tld"
                          operator="John Dow">
                <psli:right feed="none"/>
            </psli:website>
            
            <!-- feed -->
            <psli:feeds mode="feed"
                        name="Democast"
                        type="application/rss+xml"
                        url="http://democast.tld"
                        operator="John Dow">
                <psli:right feed="none"/>
            </psli:feeds>
        </psli:rights>
        
        <item>
            ...
        </item>
    </channel>
    </feed>


