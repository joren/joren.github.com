---
layout: post
title: "MMS op de iPhone 2G"
description: ""
category: 'tech'
tags: ['tech', 'ios']
---
{% include JB/setup %}

De ontgoocheling na de hoop op tethering en mms was groot toen ik merkte dat ik, met mijn iPhone 2G, na het updaten naar OS 3.0 dat nog steeds niet kon.
Blijkbaar staat Apple dit niet toe voor de eerste generatie iPhones, met de uitleg dat dit toch te traag zou zijn zonder 3G.

Deze functies waren voordien, samen met filmen, de hoofdreden waarom ik hem zou willen jailberaken. Dit zou ik nu dus weer moeten doen.

Voor tethering (surfen op je laptop via je mobiele telefoon) heb je al een tijdje het programma '[iPhoneModem](http://www.iphonemodem.com/)' dat je gratis kan installeren via de Cydia installer op je iPhone.

Voor mms is er nu ook een oplossing voor een gejailbreakte iPhone 2G dat op OS3.0 draait.

*   Stap 1: voeg " [ http://cydia.alpden.com ](http://cydia.alpden.com/) " toe als source in de Cydia app.
*   Stap 2: Installeer ActivateMMS2G en herstart je iPhone. Je zou een extra icoontje moeten zien bij het versturen van een bericht.
    Je zou nu al bij Settings > Network > Cellular Data Network invulveldjes moeten zien. voor MMS. Vul deze allemaal in, (zie onderaan hoe het voor Proximus moet ingevuld worden). Helaas merkte ik dat apn, login en wachtwoord niet werden opgeslagen, elke keer ik een mms probeerde te versturen verscheen er een rood uitroepteken naast de afbeelding.
*   Stap 3: Indien de apn niet opgeslagen blijft. Surf met je toestel naar [ help.BenM.at/generator.php ](http://help.benm.at/generator.php) voor zelf de mobiele gegevens in te vullen.
    Vul deze gegevens in en installeer de config.
*   Stap 4: je zal merken dat zowel voor mobiele data als mms als voicemail deze gegevens nu gebruikt worden. Je hoeft dus nog enkel de eerste gegevens voor Cellular data weer aan te passen en niet meer aan de gegevens van mms te komen.
*   Je zou nu moeten kunnen mms'en met je iPhone 2G.

Dit zijn de gegevens die ik gebruikt heb voor mms bij proximus:
* apn: event.proximus.be
* Gebruikersnaam: mms
* Wachtwoord: mms
* MMSC: http:/mmsc.proximus.be/mms
* maximale grootte: 300000
* IP-adres: 010.055.014.075:80
* MMS UA: http:/mmsc.proximus.be/mms
