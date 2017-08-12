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
    
    Beinhaltet Angaben zu Verwendungsrechten der Website, Feeds, Cover, Poster, Images & Audiofiles 
    
    Website:
     - mode: website
     - type: text/html
     - name: name of the podcast
     - href: URL of the website
     - operator: name of producer
     - right: 
          - N/A: Inhalt darf / darf nicht...
    
    Feeds:
     - mode: feed
     - type: application/rss+xml
     - name: name (podcast feed) 
     - href: URL of the feed
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

        <!-- specify header rights -->
        <ps:rights version="1.0" xmlns:ps="http://www.podcast-society.org/pss/right-information-act">
            <ps:website> 
                      <ps:mode>website</mode>
                      <ps:type>text/html</type>
                      <ps:href>http://democast.tld</href> 
                      <ps:operator>John Dow</operator>
                      <ps:name>Democast</name>
                      <ps:rights website="none" ... />
            </ps:website>
            <ps:feeds> 
                      <ps:mode>feed</mode>
                      <ps:type>application/rss+xml</type>
                      <ps:href>http://democast.tld</href> 
                      <ps:operator>John Dow</operator>
                      <ps:name>Democast</name>
                      <ps:rights website="none" ... />
            </ps:feeds>
        </ps:rights>
        
        <item>
            ...
        </item>
    </channel>
    </feed>


