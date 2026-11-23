# System Architecture

## **NSL les 1: Recap netwerken jaar 1**

Leerdoel bij deze les:

- op een veilige manier werken met virtuele systemen en netwerken

### Planning aankomende periode:

* Week 1 : Herhaling van de highlights netwerken- en securityonderwerpen jaar 1
* Week 2 : Netwerksegmentatie : Subnetten, VLAN’s en fysieke scheiding
* Week 3 : Cloud computing en vooruitblik Opdracht 1
* Week 4 : Security : encryptie (Opdracht 1 open)
* Week 5 : VPN, Firewalls
* Week 6 : IoT-hardware, LoRa(WAN) en Wifi (Opdracht 2 open)
* Week 7 : Nog meer security
* Week 8 : Toetsweek

### Netwerken: terminologie

- IP en de 3-way handshake
- TCP/UDP
- ARP
- MAC
- DHCP
- NMAP
- Poorten en Port farwarding
- Firewall
- DNS
- HTTP(S) : GET, POST, etc
- Protocal/ Framawork/ Service

### Identificeren van een device op het netwerken

- IP address: IP = Internet protocol
- Private (10, 172, 192)

#### Subnetten

**Subnetten is het opdelen van een groter netwerk inn kleinere meer beheersbare subnetwerken.**

notatie: /x

/24 -> de eerste 24 bits staan vast (vanaf links)

dus 32 - 24 = 8 bits

8 bits (0 - 255) = 256 mogelijkheden voor de ***host***

**Waarom?**

* Efficientie
* Betere prestatie
* Beveiliging
* Organisatie structureren

#### OSI model

| OSI Model          | Omschrijving | TCP/IP Model        | Omschrijving | TCP/IP Protocol Suite                   |
| ------------------ | ------------ | ------------------- | ------------ | --------------------------------------- |
| Application Layer  |              | Application Layer   |              | HTTP, SMTP, telnet, FTP, DNS, RIP, SNMP |
| Presentation Layer |              |                     |              |                                         |
| Session Layer      |              |                     |              |                                         |
| Transport Layer    |              | Transport Layer     |              | TCP, UDP                                |
| Network Layer      |              | Internet Layer      |              | ARP, IP, IGMP, ICMP                     |
| Data Link Layer    |              | Network Acces Layer |              | Ethernet, Token Ring, ATM, Frame Relay  |
| Physical Layer     |              |                     |              |                                         |

#### Terminologie:

Protocol:

- Een protocol is een set **afspraken** die bepaalt hoe apparaten of programma's **gegevens** met elkaar uitwisselen en interpreteren.

Framework:

- Een framework is een vooraf gebouwde **structuur** van code, regels en hulpmiddelen waarop ontwikkelaars hun eigen **software** kunne **bouwen**.

Service:

- Een service is een zelfstandig onderdeel of **dienst** die een specifieke **functionaliteit** levert en die via een vaste interface kan worden **aangeroepen**.

#### TCP/IP 3 way

Apparaat 1 vraagt verbinding aan een port op apparaat 2 ( SYN ).

Apparaat 2 zegt dat hij iets met sturen ( SYN/ACK ).

Apparaat 1 stuurt iets (ACK).

Apparaat 1 wilt toch niets sturen ( RST ).

#### ARP

- Address Resolution Protocol zorgt er voor dat apparaten zichzelf kunnen identificeren op een netwerk

Request: vraagt wie IP x.x.x.x heeft

Reply: geeft aan dat hij IP x.x.x.x heeft en MAC address x.x.x.x.x.x

#### DHCP

Dynamic Host Configuration Protocol

Een apparaat vraagt aan de DHCP server of hij een IP mag als hij deze niet automatisch heeft ontvangen

Stappen (DORA![1795427284140](image/NSL/1795427284140.webp)):

- Discover
- Offer
- Request
- ACK

#### Port forwarding

- Configuratie op een router
- Port forward zorgt ervoor dat jij een port op een prive apparaat open zet naar de buitenwereld
- Denk bij port forwarding aan minecraft (19132 of 25655)

#### HTTP Methods

- GET
- POST
- PUT
- DELETE
- ...PATCH

Wat kan een GET:

Het blijft in je browser history, kan gebookmarked worden, gecached worden. Het heeft een lengte restrictie dus je kan niet oneindig lange dingen ophalen.

Wat kan een POST:

Het kan gebookmarked worden. Geen ristricite aan lengte, data wordt niet gecached en deze request blijft niet in je browser geschiedenis.

#### Cookies en sessie

Je cookie en sessie slaan data op zoals je Username, data dat je cookie is aangemaakt, laattste keer dat je hem hebt gebruikt. Cookies worden gebruikt om persoonlijke dingen op te slaan dus helpen ook met zoek algoritmes op bepaalde websites en advertensies.

#### SQL

```SQL
 SELECT id FROM users WHERE username = '' OR 1=1;`;
```

##### Blind SQLi

SQL injectie is zonder de behulpzame foutmeldingen, dus veel trial en error.


#### Stored / Reflected XSS

**Reflected**

- Ingevoerde code wordt uitgevoerd, maar dit verdwijnt als je de pagina reload
- Andere gebruikers hebben er geen last van
- input fields die user input in de URL parameters stoppen

**Stored**

- Ingevoerde code wordt opgeslagen
- Bijv. in de database of commentaarveld op een pagina
- Andere gebruikers kunnen er last van hebben

## NSL les 2:
