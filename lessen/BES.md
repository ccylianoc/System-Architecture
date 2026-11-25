# System Architecture

## Eindopdracht:

Bouw je eigen besturingssysteem.

Wat houd dit in?

- Ontwerp en bout een operating system voor de Arduino UNO: ArduinOS.

  - Multitasking: meerdere processen tegelijk.
  - Bestandssysteem (non-volatile).
  - Geheugenbeheer.
  - Commad line interface (input/ output).
- Waarom Arduino?

  - Nog geen OS.
  - Uitdagin m.b.t. geheugen.
- Programmeertaal: C++
- Samenwerken toegestaan, maar individueel inleveren en toelichten.

## **Besturingssystemen les 1: Booting up**

### Planning?

- Wat is een OS?
- Wat is een kernel?
- Herhaling C++
- Blokdiagram OS

### Wat is een besturingssysteem?

Een operating system (OS) is de centrale software op een apparaat dat alles bestuurt.

De laag die tussen de fysieke wereld en digitale wereld zit.

Bekendste OS:

- Windows
- MacOS
- Android
- iOS
- Linux

### Wat is Linux?

Linux is een ***Open Source*** versie van ***UNIX***.

UNIX is een multi-processing OS uit de 70's.

Stabiel platform wat veilig is.

Bediening is vooral via de Command Line Interface (CLI).

	- Typ commando's om programma's te starten

	- Nu ook met Graphical User Interface (GUI)

Linux is/kan multi user zijn. iedereen heeft dan zijn eigen home directory /dir.

Je hebt niet net als windows toegang tot andere hun bestanden behalve als deze vrijgegeven zijn.

Alleen de super-gebruiker (***root***) heeft toegang tot alles ==> net als jezelf admin en full premissions geven in windows alleen standaard

Het concept is simpel, kleine programma's zijn goed in een specifieke taak en worden gecombineerd tot complexe acties.

![1795596018844](image/BES/1795596018844.png)

**In vergelijking met andere OS'en:**

- Minder gebruikvriendelijk voor beginners en niet IT'ers
- Meer geschikt voor heavy-duty toepassingen zoals servers en procesbesturing in de industrie

Linux is alleen de kernel, GNU alle hulpprogramma's.

### Wat is een kernel?

"De *kernel* is de kern van een OS waarmee alle hardware op basisniveau aangestuurd wordt."

Linux kernel: geschreven door Linus Torvalds in 1991 in C

Most recente versie: **7.2**

Dit is ook de basis van Android (andere soort OS).

#### Wat doet de kernel?

| col1                                 | col2                                                                                                           |
| ------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| **Bestuurt de processor(en)**       | Houdt bij welke processen draaien en hoeveel processortijd de krijgen (prioriteit)                             |
| **Geheugenbeheer**                  | Bepaalt welke delen dan het geheugen worden gebruikt voor het opslaan van programma's en data                  |
| **Beheer van I/O-apparaten**        | (toetsenbord, muis, USB-apparaten, netwerkkaart enz.): Bepaalt welk programma toegang kruigt tot welk apparaat |
| **Bestandssysteem**                 | Beheert de toegang tot opslagmedia en harde schijven                                                           |
| **Inter-Proces-Communicatie (IPC)** | Zorgt ervoor dat data en resources (bij. geheugen) gedeeld kunnen worden tussen processen                      |

#### Distributies

Distro: "Linux kernel samen met hulpprogramma's, applicaties, package manager, installatieprogramma."

Een distro is geoptimaliseerd voor andere functionaliteiten. Het heeft ook verschillende desktop enviroment (grafische verschillen en andere keuzes).

Vaak verspreid als .iso bestand of on-line.

In praktijk gaan we uit van ***Debian*.**

### Virtual machines

Wat is een virtual machine? "Een programma dat een complete computer simuleert". Je kunt hier net als een computer een OS op installeren, bijv. windows, linux.

Veel servers zijn virtual machines, denk aan de servers die wij vorig jaar hebben gebruikt voor de medicijn kluizen. 

**Voordelen:**

- Veilig: een indringer komt niet bij de echt hardware.
- Makkelijk verschillende OS'en uitproberen.
- Makkelijk "bijschakelen" indien nodig.

 **Nadeel:**  iets minder performance
