**Bericht** vom 02. Juni 2021

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image1.jpg){width="6.3in"
height="7.018055555555556in"}Sichtbarmachung der Schweiz auf der
electricitymap.org und Rechenzentren-Assessment

![Logo Description automatically
generated](vertopal_96af99e20f4f4b768c982af86a817716/media/image2.jpeg){width="2.7263024934383204in"
height="0.8020833333333334in"}

**Datum:** 02. Juni 2021

**Ort:** Bern

Auftraggeberin:

Bundesamt für Energie BFE\
CH-3003 Bern\
www.bfe.admin.ch

Auftragnehmer/in:

EBP Schweiz AG

Mühlebachstrasse 11

8032 Zürich

Schweiz

Telefon +41 44 395 16 16

<info@ebp.ch>

[www.ebp.ch](http://www.ebp.ch)

Autor/in:

Kristof Kölker, EBP Schweiz AG\
Rafael Brunner, EBP Schweiz AG

**BFE-Bereichsleitung:** Dr. Matthias Galus, matthias.galus@bfe.admin.ch

**BFE-Programmleitung:** Dr. Fabian Heymann, fabian.heymann@bfe.admin.ch

**BFE-Vertragsnummer:** SI/600518-01

**Für den Inhalt und die Schlussfolgerungen sind ausschliesslich die
Autoren dieses Berichts verantwortlich.**

# Inhaltsverzeichnis  {#inhaltsverzeichnis .Überschrift-ohne-Nummerierung}

[1 Berechnung der CO~2~ Intensität auf electricitymap.org
[4](#berechnung-der-co2-intensität-auf-electricitymap.org)](#berechnung-der-co2-intensität-auf-electricitymap.org)

[1.1 Grundlagen [4](#grundlagen)](#grundlagen)

[1.2 Methodik zur Schätzung des CO~2~-Fussabdrucks
[4](#methodik-zur-schätzung-des-co2-fussabdrucks)](#methodik-zur-schätzung-des-co2-fussabdrucks)

[1.3 Situation Schweiz & Projekthistorie
[6](#situation-schweiz-projekthistorie)](#situation-schweiz-projekthistorie)

[2 Verbesserung der Datenqualität der Schweizer Stromproduktion
[7](#verbesserung-der-datenqualität-der-schweizer-stromproduktion)](#verbesserung-der-datenqualität-der-schweizer-stromproduktion)

[2.1 Annahmen [7](#annahmen)](#annahmen)

[2.2 Berechnung der CO~2~-Intensität der Kategorie «Unbekannt»
[8](#berechnung-der-co2-intensität-der-kategorie-unbekannt)](#berechnung-der-co2-intensität-der-kategorie-unbekannt)

[2.3 Validierung mit Stromproduktionsdaten der Swissgrid
[9](#validierung-mit-stromproduktionsdaten-der-swissgrid)](#validierung-mit-stromproduktionsdaten-der-swissgrid)

[2.4 Validierung mit BFE Monatsstatistik
[11](#validierung-mit-bfe-monatsstatistik)](#validierung-mit-bfe-monatsstatistik)

[3 Abschätzung der CO~2~ Erzeugung in Schweizer Rechenzentren
[13](#abschätzung-der-co2-erzeugung-in-schweizer-rechenzentren)](#abschätzung-der-co2-erzeugung-in-schweizer-rechenzentren)

[3.1 Stromverbrauch in Schweizer Rechenzentren
[13](#stromverbrauch-in-schweizer-rechenzentren)](#stromverbrauch-in-schweizer-rechenzentren)

[3.2 Anteil erneuerbare Energie am Stromverbrauch Schweizer
Rechenzentren
[14](#anteil-erneuerbare-energie-am-stromverbrauch-schweizer-rechenzentren)](#anteil-erneuerbare-energie-am-stromverbrauch-schweizer-rechenzentren)

[3.3 Anteil Importierter Strom am Verbrauch von Rechenzentren
[14](#anteil-importierter-strom-am-verbrauch-von-rechenzentren)](#anteil-importierter-strom-am-verbrauch-von-rechenzentren)

[3.4 Stündlich aufgelöste Emissionen durch Schweizer Rechenzentren
[15](#stündlich-aufgelöste-emissionen-durch-schweizer-rechenzentren)](#stündlich-aufgelöste-emissionen-durch-schweizer-rechenzentren)

[4 Aufteilung der in Rechenzentren entstandenen Emissionen auf Dienste
[16](#aufteilung-der-in-rechenzentren-entstandenen-emissionen-auf-dienste)](#aufteilung-der-in-rechenzentren-entstandenen-emissionen-auf-dienste)

[5 Literaturverzeichnis
[19](#literaturverzeichnis)](#literaturverzeichnis)

[6 Anhang [20](#anhang)](#anhang)

[6.1 Electricitymap Parser für die Schweiz
[20](#electricitymap-parser-für-die-schweiz)](#electricitymap-parser-für-die-schweiz)

[6.2 Folien zur Validierung
[22](#folien-zur-validierung)](#folien-zur-validierung)

[6.3 Abschätzung der typischen Lastkurve für Schweizer Rechenzentren
[29](#abschätzung-der-typischen-lastkurve-für-schweizer-rechenzentren)](#abschätzung-der-typischen-lastkurve-für-schweizer-rechenzentren)

# Berechnung der CO~2~ Intensität auf electricitymap.org

## Grundlagen

Auf der Website electricitymap.org wird die CO~2~ Intensität von Strom
in verschiedenen Ländern und Regionen der Welt in Echtzeit visualisiert.
Echtzeit wird hierbei definiert als eine Datengrundlage, die mit einer
Mindestfrequenz von einem Tag und einem Verzug von maximal 2 Stunden
aktualisiert wird. Für die meisten Länder werden die Daten mit
stündlicher Frequenz veröffentlicht. Die so entstehende Transparenz soll
Verbrauchern helfen den CO~2~-Fussabdruck von ihrem Konsum besser
abschätzen zu können.

Die wichtigste Kennzahl auf electricitymap.org ist die die
CO~2~-Intensität vom verbrauchten Strom in $\frac{g_{{CO}_{2}eq}}{kWh}$.
Die verwendete Methode berücksichtigt importierten und exportierten
Strom. Die CO~2~-Intensität vom verbrauchten Strom wird gegenüber der
CO~2~-Intensität vom produzierten Strom in einem Land bevorzugt, um die
Verbraucher im jeweiligen Land nicht für den aus dem Land exportierten
Strom verantwortlich zu machen. Ausserdem ist diese Kennzahl robust
gegen das Auslagern vom CO~2~-Fussabdruck von exportiertem Strom ins
Ausland. (Tomorrow, 2021)

Eine CO~2~-Intensität pro Kopf wird nicht berechnet, da diese durch den
Import von produzierten Gütern leicht verfälscht werden könnte. Die
Kennzahl der CO~2~-Intensität vergleicht nicht den absoluten Fussabdruck
der Einwohner, da dieser neben der Intensität auch von der Menge des
verbrauchten Stroms abhängt, sondern gibt an wie viel Emissionen pro kWh
Strom zusätzlich freigesetzt werden. (Tomorrow, 2021)

## Methodik zur Schätzung des CO~2~-Fussabdrucks

Zur Berechnung der verbrauchsbasierten CO~2~-Intensität verwendet
electricitymap Strömungsverfolgungstechniken (engl. flow-tracing). Mit
dieser Methodik wird jede Region/Land als Knoten $n$ abstrahiert. Es
gibt Flüsse (engl. flows) von Emissionen zwischen den Knoten und in
jedem Knoten können neue Emissionen durch die Produktion von Strom
entstehen oder durch den Verbrauch von Strom konsumiert werden. Es wird
angenommen, dass für jeden Knoten zu jedem Zeitpunkt der gesamte
importierte und produzierte Strom und die damit verbundenen Emissionen
sich gleichmässig zu einer durchschnittlichen CO~2~-Intensität $i_{n}$
vermischen. Diese CO~2~-Intensität gilt sowohl für den in der jeweiligen
Region verbrauchten Strom *V~n~* als auch für die Stromexporte in die
benachbarten Regionen $F_{n \rightarrow k}$.

Die in der jeweiligen Region produzierte Menge Strom pro
Produktionskategorie *m* ist gegeben als $P_{m,n}$. Weiterhin sind die
CO~2~-Intensität der jeweiligen Produktionskategorie gegeben als
$i_{m,n}$. Die im Knoten *n* entstandenen Emissionen lässt sich
berechnen als Summe aller Produktionskategorien
$\sum_{m}^{}{i_{m,n}P_{m,n}}$.

Ausserdem sind die Stromflüsse *F* zu den direkt benachbarten Regionen
*k* bekannt. Die Importe aus den benachbarten Regionen
$F_{k \rightarrow n}$ müssen zur Modellierung der CO~2~ Emissionen mit
der Intensität des jeweiligen Knotens $i_{k}$ multipliziert werden.

Die folgende Gleichung beschreibt das Flussmodel für Land *n*. (Bo
Tranberg, 2019)

$$i_{n}\left( V_{n} + \sum_{k}^{}F_{n \rightarrow k} \right) = \sum_{m}^{}{i_{m,n}P_{m,n}} + \sum_{k}^{}{i_{k}F_{k \rightarrow n}}$$

Formel 1: Modell der Emissions-Flüsse für die Berechnung der
CO2-Intensität auf electricitymap

Weiterhin wird eine verlustfreien Stromübertragung
($V_{n} + \sum_{k}^{}F_{n \rightarrow k} = \sum_{m}^{}P_{m,n} + \sum_{k}^{}F_{k \rightarrow n}$)
angenommen, so dass die CO~2~-Intensität für jede Region berechnet
werden kann. (Bo Tranberg, 2019) (Tomorrow, 2021)

Das oben beschrieben Modell wird auf die Daten in der Datenbank der
electricitymap angewendet. Die individuellen Quellen der Stromproduktion
pro Produktionskategorien der berücksichtigten Länder wird auf der
Internetseite von electricitymap.org veröffentlicht. (Tomorrow, 2021)
Die CO~2~-Intensitäten des produzierten Stroms beinhalten die Emissionen
des gesamten Lebenszyklus des produzierenden Kraftwerks (Bau, Betrieb
und Abbau). Die Daten werden aus Basis der ecoinvent Datenbank 3.4
abgeleitet. (Bo Tranberg, 2019)

Tabelle 1 gibt die CO~2~-Intensitäten der verschiedenen Kraftwerkstypen
in der Schweiz an. (Tomorrow, 2021)

#### Tabelle : Verwendete CO2-Intensitäten (Gesamter Lebenszyklus) pro Kraftwerkstyp des in der Schweiz produzierten Stroms (Quelle: IPCC 2014)

  ----------------------------------------------------------------------------------------------------------------------------------------------
  Produktionsart                            CO~2~-Intensität
                                            $\left\lbrack \frac{\mathbf{g}_{\mathbf{CO}_{\mathbf{2}}\mathbf{eq}}}{\mathbf{kWh}} \right\rbrack$
  ----------------------------------------- ----------------------------------------------------------------------------------------------------
  **Geothermie**                            12

  **Biomasse**                              38

  **Wasserkraft**                           230

  **Solar**                                 24

  **Pumpspeicherkraftwerke**                45
  ----------------------------------------------------------------------------------------------------------------------------------------------

##  Situation Schweiz & Projekthistorie

Für die Berücksichtigung im Modell der electricitymap muss die
Stromproduktion einer Region aufgeschlüsselt nach Produktionskategorie
mit einem maximalen Zeitverzug von 2 Stunden verfügbar sein. Für die
Schweiz werden diese Daten auf der ENTSOE-E Transparency Plattform
(Kategorie 16.1.B&C) veröffentlicht. Im Jahr 2017 wurden folgenden
Probleme auf der Website von electriciymap gemeldet (Tomorrow, 2018)

-   Im Jahr 2016 wurden von den 36.3 TWh (gem. BFE) durch Wasserkraft
    produzierten Stroms nur 13.5 TWh an die ENTSOE-E Transparency
    Plattform gemeldet. D.h. fast zwei Drittel des durch Wasserkraft
    produzierten Stroms fehlt.

-   Die 3.1 TWh die gem. BFE im Jahr 2016 in konventionell-thermischen
    Kraft- und Fernheizkraftwerken produziert wurden fehlen komplett auf
    der ENTSOE-E Transparency Plattform.

Aufgrund der fehlenden Daten kam es bei der Berechnung CO~2~-Intensität
in der Schweiz zu einem signifikanten Fehler. Wie in Kapitel 1.2
beschrieben, überträgt sich dieser Fehler durch Exporte auf benachbarte
Regionen, so dass 2017 entschieden wurde die Schweiz von den
Berechnungen auszuschliessen. (Tomorrow, 2018)

Im August 2020 initiierte das BFE auf einem von Opendata.ch
organisierten Hackathon zum Thema Energie ein Innovationsprojekt, um die
Echtzeitdaten in der Schweiz zu verbessern und eine Veröffentlichtung
auf electricitymap zu ermöglichen. Ein Team aus Fachspezialisten,
Softwareentwicklern und Data Analysts entwickelte eine Lösung, um die
fehlenden Daten auf der ENTSOE-E Transparency Plattform abzuschätzen und
für die Verwendung der Berechnung der CO~2~ Intensität zu verwenden. Die
gemeinsam erarbeitete Lösung wird im Kapitel 2 beschrieben.

# Verbesserung der Datenqualität der Schweizer Stromproduktion

Wie in Kapitel 1.2 beschrieben muss die Stromproduktion und die
zugehörige CO~2~-Intensität von Kraftwerken, die nicht in den
Produktionsdaten der ENTSOE-E Transparency Plattform erfasst werden, mit
einem maximalen Verzug von 2 Stunden bestimmt werden.

## Annahmen

Der Betreiber der electricitymap erlaubt keine Zuweisung von
national-differenzierten CO~2~-Intensitäten von einzelnen
Krakftwerkstypen. Daher wurde in dem auf dem Hackathon entwickelten
Ansatz angenommen, dass die Zusammensetzung des nicht in den ENTSOE-E
Daten erfassten Stroms der Schweiz (roter Block) über das Jahr konstant
ist.

![Chart, waterfall chart Description automatically
generated](vertopal_96af99e20f4f4b768c982af86a817716/media/image3.png){width="3.5119061679790025in"
height="2.3248293963254594in"}

Abbildung : Visualisierung der Kategorie \"unbekannt\"

Für jede Stunde kann die gesamte Stromproduktion in der Schweiz
abgeschätzt werden als die Differenz zwischen der gesamten Last in der
Schweiz (ENTSOE-E Kategorie 6.1.B[^1]: Inklusive Übertragungsverluste,
Eigenverbrauch von Kraftwerken und Verbrauch von
Pumpspeicherkraftwerken) und den Exporten/Importen mit benachbarten
Ländern (ENTSOE-E Handbuch Kategorie 12.1.G). Die Stromproduktion in
Kraftwerken, welche die Daten nicht an die ENTSOE-E Transparency
Plattform übermitteln, wird berechnet als Differenz der oben
abgeschätzten gesamten Produktion in der Schweiz und der Summe der
Stromproduktion der Kraftwerke, welche die Daten übermitteln und auf
electricitymap als «unbekannt» veröffentlicht.

$$P_{unbekannt,ch} = V_{n} + \sum_{k}^{}F_{ch \rightarrow k} - \sum_{k}^{}F_{k \rightarrow ch} - \sum_{m}^{}P_{m,ch}$$

Formel 2: Berechnung der Stromproduktion in Kraftwerken, welche die
Daten nicht an die ENTSOE-E Transparency Plattform übermitteln

## Berechnung der CO~2~-Intensität der Kategorie «Unbekannt»

Die Modelle des Betreibers der electricitymap nehmen zeitlich konstante
CO~2~-Intensitäten für einzelne Kraftwerkstypen an. Es gibt keine
Unterscheidung zwischen im Sommer oder im Winter produzierten Strom
derselben Stromerzeugungs-Technologie wie z.B. Atomstrom. Für die in
Kapitel 2.1 neu eingeführte Kategorie «unbekannt» wird daher eine über
das Jahr gemittelte durchschnittliche CO~2~-Intensität aus einem
Vergleich der BFE Gesamtenergiestatistik 2019 mit dem auf der ENTSOE
veröffentlichen Daten.

#### Tabelle : Vergleich der Elektrizitätserzeugung im Jahr 2019 nach BFE Gesamtenergistatistik 2019 (Tab. 24) und aggregierte Werte der ENTSOE-E Transparency Plattform

+------------+------------+-----------+--------------+---------------+
| 2019       | Ges        | ENTSOE-E  | Abdeckung    | Gewi          |
|            | amtenergie | Tra       | der Werte    | chtungsfaktor |
|            |            | nsparceny | der          |               |
|            | -statistik | Plat      | Gesamt-ener  | C             |
|            | BFE[^2]    | tform[^3] | giestatistik | O2-Intensität |
|            |            |           | BFE auf      |               |
|            |            |           | ENTSO-E TP   |               |
+============+============+===========+==============+===============+
|            | $$         | $$\l      | $$\lbrac     | $$\le         |
|            | \lbrack GW | brack GWh | k\%\rbrack$$ | ft\lbrack \fr |
|            | h\rbrack$$ | \rbrack$$ |              | ac{g_{{CO}_{2 |
|            |            |           |              | }eq}}{kWh} \r |
|            |            |           |              | ight\rbrack$$ |
+------------+------------+-----------+--------------+---------------+
| Atomstrom  | 25.28      | 25.71     | 101.7        | 12            |
+------------+------------+-----------+--------------+---------------+
| W          | 17.70      | 1.95      | 11.0         | 24            |
| asserkraft |            |           |              |               |
+------------+------------+-----------+--------------+---------------+
| Wind       | 0.08       | 0.15      | 187.5        | 0             |
+------------+------------+-----------+--------------+---------------+
| Solar      | 2.18       | 0.42      | 19.2         | 45            |
+------------+------------+-----------+--------------+---------------+
| Pu         | 22.85      | 19.54     | 85.5         | 150           |
| mpspeicher |            |           |              |               |
| kraftwerke |            |           |              |               |
+------------+------------+-----------+--------------+---------------+
| Konv       | 3.05       | \-        | 0.0          | 700           |
| entionell- |            |           |              |               |
|            |            |           |              |               |
| thermisch  |            |           |              |               |
+------------+------------+-----------+--------------+---------------+
| Andere     | 0.68       | \-        | 0.0          | 220           |
|            |            |           |              |               |
| e          |            |           |              |               |
| rneuerbare |            |           |              |               |
+------------+------------+-----------+--------------+---------------+

In Tabelle 2 ist zu sehen, dass Wasserkraft den grössten Anteil des
Stroms, der nicht an die ENTSOE Transparency Plattform gemeldet wird,
ausmacht. Dieser Strom wird überwiegend in kleineren Flusskraftwerken
produziert. Weitere signifikante Anteile kommen aus kleineren
Photovoltaik Anlagen (Solar) und Kraft-Wärme-Kopplungsanlagen
(Konventionell-thermisch), welche nicht als Kategorie für die Schweiz
auf der ENTSOE Transparency Plattform erfasst werden.

Mit den Gewichtungsfaktoren aus Tabelle 1 ergibt sich für den nicht an
die ENTSOE gemeldeten in der Schweiz produzierten Strom eine
CO~2~-Intensität von
$\mathbf{131.4}\frac{\mathbf{g}_{\mathbf{CO}_{\mathbf{2}}\mathbf{eq}}}{\mathbf{kWh}}$.

## Validierung mit Stromproduktionsdaten der Swissgrid

Swissgrid, die Netzwerkbetreiberin der Schweiz, veröffentlicht auf ihrer
Website mit einem Verzug von ca. 2-4 Wochen Daten zur stündlichen
Stromproduktion in der Schweiz. Diese Daten können nicht für die
electricitymap verwendet werden, da Sie nicht in Echtzeit veröffentlicht
werden und ausserdem nur die gesamte Schweizer Stromproduktion ohne
Aufschlüsselung der einzelnen Kraftwerkstypen beinhaltet. (Swissgrid,
2021)

Die Daten der Swissgrid werden im Folgenden verwendet um die in Echtzeit
berechnete, gesamte Stromproduktion in der Schweiz (siehe Kapitel 2.1)
zu validieren. Hierfür wurde die Stromproduktion in der Schweiz gemäss
dem Modell für das Jahr 2020 berechnet und mit den Swissgrid Daten sowie
den Daten auf der ENTSOE-Transparency Plattform verglichen.

#### Tabelle : In der Schweiz pro Stunde produzierter Strom \[in GWh\] gemäss Swissgrid, ENTSOE, der BFE Monatsstatistik und dem Modell für die electricitymap (Januar-November 2020)

+-------------------+-----------------+--------------+-----------------+
| \[GWh\]           | Neues Modell    | S            | ENTSOE          |
|                   |                 | wissgrid[^4] |                 |
|                   | (siehe Kapitel  |              |                 |
|                   | 2.1)            |              |                 |
+===================+=================+==============+=================+
| Durchschnitt      | 7.60            | 7.78         | 5.34            |
+-------------------+-----------------+--------------+-----------------+
| Maximum           | 14.42           | 13.84        | 10.57           |
+-------------------+-----------------+--------------+-----------------+
| Minimum           | 3.44            | 4.40         | 1.38            |
+-------------------+-----------------+--------------+-----------------+
| Summe             | 60'936          | 62'340       | 42'797          |
+-------------------+-----------------+--------------+-----------------+
| Pumps             | 22.85           | 19.54        | 150             |
| peicherkraftwerke |                 |              |                 |
+-------------------+-----------------+--------------+-----------------+
| Konven            | 3.05            | \-           | 700             |
| tionell-thermisch |                 |              |                 |
+-------------------+-----------------+--------------+-----------------+
| Andere            | 0.68            | \-           | 220             |
| erneuerbare       |                 |              |                 |
+-------------------+-----------------+--------------+-----------------+

Tabelle 3 zeigt, dass von den durch die Swissgrid publizierten 62TWh nur
42TWh auf der ENTSOE Plattform publiziert werden. Durch die in Kapitel
2.1 beschriebene Modellierung kann dieser Wert auf 61TWh korrigiert
werden. Dies stimmt ebenfalls mit vom BFE publizierten Monatsstatistiken
überein. (Bundesamt für Energie, 2021)

![Chart Description automatically
generated](vertopal_96af99e20f4f4b768c982af86a817716/media/image4.png){width="5.040411198600175in"
height="2.6145833333333335in"}

Abbildung 2: In der Schweiz produzierter Strom pro Stunde gemäss
Swissgrid (grün), ENTSOE (gelb) und dem Modell für die electricitymap
(blau) sowie deren Differenz für die ersten beiden Juli Wochen 2020.

Abbildung 2 zeigt den zeitlichen Ablauf der in Tabelle 3 aufgezeigten
Differenzen für die ersten beiden Juli Wochen 2020. Zu jedem Zeitpunkt
gibt es signifikanten Unterschiede zwischen den Swissgrid Daten (grün)
und der Summe der ENTSOE Daten (gelb). Durch die getroffenen Annahmen
(blau) kann zeitlich eine gute Übereinstimmung mit den später
veröffentlichen Swissgrid Daten erreicht werden.

Die Differenz zwischen den Swissgrid und den ENTSOE ist typischerweise
zwischen 8-12 Uhr und 18-23 Uhr besonders gross. Ausserdem ist die
Differenz zwischen April und September grösser als während des
restlichen Jahres. Wahrscheinlich wird aufgrund des hohen Strombedarfs
und der Verfügbarkeit in diesen Momenten besonders viel Strom in
Laufwasserkraftwerken produziert. Dieser wird nicht an ENTSOE gemeldet,
so dass die Differenz in diesen Momenten besonders gross ist.

Für die Berechnungen mit dem Modell (blaue Kurve) wurden die aktuell auf
der ENTSOE Transparency Plattform veröffentlichen Daten für den
Stromverbrauch sowie Importe und Exporte verwendet. Es muss beachtet
werden, dass die Daten für den Stromverbrauch bis zum 3. Mittwoch des
darauffolgenden Monats durch genauere Werte ersetzt werden. Die zum
Zeitpunkt der ersten Veröffentlichung gemeldeten Werte werden nicht
dauerhaft abgespeichert, sondern gehen mit der Veröffentlichung der
korrigierten Werte verloren. Eine Validierung mit den Werten die in
Echtzeit für die Berechnung des Stromverbrauchs auf electricitymap.org
verwendet werden ist daher nicht möglich.

Es gibt eine gute Übereinstimmung zwischen den Werten, die auf der
electricitymap für die gesamte Stromproduktion in der Schweiz in
Echtzeit veröffentlicht werden und den später durch Swissgrid
veröffentlichen Werten, so dass sich das Modell sich insgesamt gut
eignet, um die Stromproduktion in der Schweiz abzuschätzen.

## Validierung mit BFE Monatsstatistik

Das BFE veröffentlicht monatliche Informationen über die
Stromproduktion. Diese werden in diesem Kapitel verwendet, um den die
Aufteilung auf electricitymap auf die Erzeugungstechnologien zu
verifizieren. Hierfür wurden für die Berechnung der zu erwartenden Werte
auf der electricitymap erneut die aktuell auf der ENTSOE Transparency
Plattform veröffentlichen Werte verwendet. (Bundesamt für Energie, 2021)

#### Tabelle : In der Schweiz pro Stunde produzierter Strom \[in GWh\] gemäss der BFE Monatsstatistik und dem Modell für die electricitymap (Januar-Oktober 2020)

  ------------------------------------------------------------------------------------------------
  \[GWh\]     Wasserkraft            Kernkraftwerke           Rest           Total      
  ----------- ------------- -------- ---------------- ------- ------- ------ ---------- ----------
              BFE ES        EMap     BFE ES           EMap    BFE ES  EMap   BFE ES     EMap

  Januar      3013          2662     2187             2231    498     308    **5698**   **4522**

  Februar     2504          2144     2047             2087    531     449    **5082**   **4162**

  März        2705          2519     2185             2231    542     743    **5432**   **4711**

  April       2349          2401     1974             2017    519     968    **4842**   **4652**

  Mai         3071          3164     1944             1988    554     1193   **5569**   **5535**

  Juni        3694          3721     1476             1500    546     1153   **5716**   **5385**

  Juli        3979          3901     1249             1245    618     1212   **5846**   **5268**

  August      3381          3611     1626             1655    557     1026   **5564**   **5365**

  September   2979          3183     2067             2104    555     849    **5601**   **5307**

  Oktober     3006          3083     2164             2195    481     675    **5651**   **5234**
  ------------------------------------------------------------------------------------------------

Für die Aufteilung der Kategorie «unbekannt» werden die aus Tabelle 2
abgeleiteten Prozentsätze für die durchschnittliche Zusammensetzung der
nicht gemeldeten Stromproduktion verwendet (77% Wasserkraft, 23% Rest).
Die in Tabelle 4 aufgeführt Kategorie «Rest» fasst Stromproduktionen aus
konventionell-thermischen und erneuerbaren Kraftwerken wie z.B. Solar-
und Windenergie zusammen.

Bei den Echtzeitdaten der Schweizer Stromproduktion fehlte ein grosser
Anteil an Wasserkraft (siehe Tabelle 2) aus Laufwasserkraftwerken.
Tabelle 4 zeigt für die Wasserkraft eine gute Übereinstimmung zwischen
den durch das BFE veröffentlichten Werten und den auf der electricitymap
zu erwartenden Werten.

Im April-September wird in der Schweiz überdurchschnittlich viel Strom
in Laufwasserkraftwerken produziert. Da für die Zusammensetzung auf
electricitmap der Jahresdurchschnitt verwendet wird, ist die Abschätzung
der Kategorie für erneuerbare Technologien und konventionell-thermische
Kraftwerke in diesen Monaten etwas zu hoch.

# Abschätzung der CO~2~ Erzeugung in Schweizer Rechenzentren

## Stromverbrauch in Schweizer Rechenzentren

Zum Abschätzen einer typischen Lastkurve wird der gemessene
Stromverbrauch eines Rechenzentrums der Swisscom verwendet und
aufbereitet. Der Datensatz besteht aus dem Stromverbrauch von 4 Blöcken
(NOBR 1-4) zwischen dem 22.01.2020 und dem 21.01.2021 in 15 Minuten
Intervallen. Die Daten werden wie folgt aufbereitet, um eine Lastkurve
abzuschätzen.

a.  Es fehlen einzelne Datenpunkte. Da dies nie mehr als ein Datenpunkt
    und nie mehr als einer der 4 Blöcke gleichzeitig betrifft wird die
    Lücke über ein \"backwardsfill\" mit den Daten der vorherigen 15
    Minuten abgeschätzt.

b.  Im Moment der Zeitumstellung fehlt der Wert einer Stunde
    (Zeitverschiebung). Dieser wird mit dem Wert der vorherigen Stunde
    abgeschätzt.

c.  Die zwischen dem 01.01.2021 und dem 21.01.2021 werden zur
    Abschätzung der Werte für den gleichen Zeitraum im Jahr 2020
    verwendet.

d.  Die fehlenden Werte am 22.01.2020 werden durch die Werte des
    21.01.2020 geschätzt.

Für das Jahr 2013 wurde in einer Studie der Stromverbrauch der Schweizer
Rechenzentren auf 1660.71 GWh geschätzt. Dieser Wert wird zusammen mit
der typische Lastkurve benutzt, um den stündlichen Stromverbrauch in
Schweizer Rechenzentren abzuschätzen. (IWSB - Institut für
Wirtschaftsstudien Basel AG, 2014)

![Graphical user interface, chart, line chart Description automatically
generated](vertopal_96af99e20f4f4b768c982af86a817716/media/image5.png){width="4.581271872265967in"
height="2.991327646544182in"}

Abbildung : Abschätzung des gesamten Stromverbrauchs in Schweizer
Rechenzentren in der ersten Januar Woche 2020

## Anteil erneuerbare Energie am Stromverbrauch Schweizer Rechenzentren

Aktuell stehen die Ergebnisse des Modells für die CO~2~ Intensität des
verbrauchten Stroms der electricitymap noch nicht zur Verfügung, so dass
stattdessen die stündlich aufgelöste Zusammensetzung des in der Schweiz
produzierten Strom verwendet wird.

Von den auf der ENTSOE Transparency Plattform veröffentlichen Kategorien
sind Solarenergie, Windenergie, Wasserkraft, Pumpspeicher und 88% des
produzierten Stroms der Kategorie \"unbekannt\" (siehe Tabelle 2.1)
erneuerbare. So lässt sich stündlich der Anteil der erneuerbaren Energie
berechnen. Zusammen mit dem Verbrauch *V* der Lastkurve aus Kapitel 3.1
ergibt sich, dass **57.5%** des Stroms, der in Schweizer Rechenzentren
verbraucht wird, erneuerbar ist.

$$x_{erneuerbar} = \sum_{h}^{}{V_{Rechezentrum,h}*x_{erneuerbar,h}}$$

Formel 3: Jahresdurchschnitt des Anteils erneuerbare Energien

## Anteil Importierter Strom am Verbrauch von Rechenzentren

Der Strom, den die Rechenzentren in der Schweiz verbrauchen setzt sich
zusammen aus dem in der Schweiz produzierten Strom und dem importierten
Strom. Für den in der Schweiz produzierten Strom *P* wird die Summe, der
auf electricitymap aufgeschalteten Technologien m für jede Stunde
berechnet. Für den Import *I* werden alle Importe der benachbarten
Länder und Regionen *k* stündlich aufsummiert.

$$x_{importiert,h} = \frac{I_{h}}{P_{h} + I_{h}} = \frac{\sum_{k}^{}I_{h,k}}{\sum_{m}^{}P_{h,m} + \sum_{k}^{}I_{h,k}}$$

Formel 4: Stündlicher Anteil importierter Strom

![Chart Description automatically
generated](vertopal_96af99e20f4f4b768c982af86a817716/media/image6.png){width="3.7548687664041993in"
height="2.612952755905512in"}

Abbildung : Stündlicher Anteil importierter Strom am Schweizer Strom Mix
in der ersten Januar Woche 2020

Mit der in Kapitel 3.1 bestimmten Lastkurve ergibt sich ein gewichteter
Mittelwert von **23.8%** Anteil importierte Strom am Stromverbrauch
Schweizer Rechenzentren**.**

## Stündlich aufgelöste Emissionen durch Schweizer Rechenzentren

Wie in Kapitel 3.1 beschrieben, steht die CO~2~ Intensität des in der
Schweiz verbrauchten Stroms noch nicht zur Verfügung. Die CO~2~
Intensität des produzierten Stroms kann mit den in Tabelle 2
dargestellten CO~2~ Intensitäten berechnet werden. Multipliziert mit dem
Stromverbrauch aus Kapitel 3.1 ergeben sich folgende Emissionswerte
durch Schweizer Rechenzentren.

![Graphical user interface, chart, histogram Description automatically
generated](vertopal_96af99e20f4f4b768c982af86a817716/media/image7.png){width="5.0784722222222225in"
height="3.3680555555555554in"}

Abbildung : Stündlich aufgelöste CO~2~ Emissionen durch Schweizer
Rechenzentren in der ersten Januar Woche 2020

# Aufteilung der in Rechenzentren entstandenen Emissionen auf Dienste

In diesem Kapitel werden Möglichkeiten beschrieben die in Kapitel 3.4
berechneten CO~2~ Emissionen in Schweizer Rechenzentren auf verschiedene
Online-Dienstleistungen wie Videoplatformen oder soziale Netzwerke zu
desaggregieren.

Generell kann davon ausgegangen werden, dass der Energiebedarf in
Rechenzentren mit den für den jeweiligen Dienst benötigten Datenmengen
direkt korreliert. Um die CO~2~ Emissionen, die in Rechenzentren
entstanden sind, zu desaggregieren werden die durch verschiedene Dienste
*d* verursachten Datenströme Q benötigt. Zusammen mit den stündlich
aufgelösten Emissionen Schweizer Rechenzentren (siehe Kapitel 3.4)
können die Emissionen pro Dienst berechnet werden als:

$${Emissionen}_{d,h} = \frac{Q_{d}}{\sum_{d}^{}Q_{d}}{Emissionen}_{Rechenzentren,h}$$

Formel : Desegregation der Emissionen in Rechenzentren auf
Internetdienste

Für die Datenströme pro Dienst können zum Beispiel die Daten aus dem
«The Mobile Internet Phenomena Report» von Sandvine (siehe Tabelle 5)
verwendet werden. (Sandvine, 2020)

#### Tabelle : Anteil \[%\] am gesamten weltweiten Internetdatenverkehr nach Kategorie \[2020\] Quelle: (Sandvine, 2020)

  ------------------------------------------------------------------------
  Internetdienst      Downstream       Upstream        Total
  ------------------- ---------------- --------------- -------------------
  Video Streaming     65.6             22.4            62.1

  Social              12.9             16.8            12.7

  Messaging           5.9              16.9            6.8

  Marketplace         5.9              1.9             5.6

  Web                 4.2              19.5            5.5

  Gaming              3.7              3.3             3.3

  Cloud               0.3              7.0             1.8

  Security and VPN    0.8              7.9             1.3

  Filesharing         0.6              3.8             0.9

  Audio Streaming     0.2              0.5             0.1
  ------------------------------------------------------------------------

Internet-Datenverkehr wird generell unterschieden in Downstream und
Upstream, wobei Downstream Daten von einem Server zu einem Konsumenten
fliessen (z.B. wenn dieser sich ein Online Video anguckt) und Upstream
Daten die vom Benutzer zu einem Server fliessen (z.B. wenn der Benutzer
Dateien hochlädt). Es wäre zu untersuchen, ob die Bearbeitung von
Upstream Datenverkehr signifikant mehr oder weniger Energie in
Rechenzentren verbraucht als die Bearbeitung von Downstream Daten.
Insgesamt wird über 60% des Internetdatenverkehrs durch das Streamen von
Online Videos verursacht. Die beiden Internetseiten mit dem grössten
Internetdatenverkehr sind Youtube (25%) und Facebook Video (18%).

#### Tabelle : Anteil \[%\] am gesamten europäischen Internetdatenverkehr nach Website \[2020\] Quelle: (Sandvine, 2020)

  ------------------------------------------------------------------------
  Internetdienst      Downstream       Upstream        Total
  ------------------- ---------------- --------------- -------------------
  Youtube             27.0             7.4             25.5

  Facebook Video      17.8             5.5             17.8

  Instagram           7.1              8.2             7.2

  Facebook            5.2                              5.2

  Netflix             4.4                              4.1

  Http Media Stream   3.9                              3.7

  Google Play         3.5                              3.3

  Tiktok              3.1                              3.0

  Whatsapp            2.7              4.0             2.8

  Snapchat                                             2.1
  ------------------------------------------------------------------------

Weiterhin sollte der zeitliche Verlauf bei den Überlegungen zur
Desaggregation beachtet werden. Typischerweise gibt es eine Lastspitze
am frühen Abend, die vor allem durch Videodienste verursacht wird. Die
Last während dieser Spitzenzeiten wächst noch schneller als die gesamte
Datenmenge. Dies macht ggf. einen Ausbau der Infrastruktur erforderlich,
der für die Abdeckung der Grundlast nicht notwendig wäre. J. Morley et
al. haben typische Lastkurven für die verschiedenen Online-Dienste
erstellt, die für eine stündlich aufgeschlüsselte Aufteilung verwendet
werden könnten. (Janine Morley, 2018)

Bei der Berechnung durch Webdienste entstandene CO~2~ Emissionen sollte
berücksichtigt werden, dass insbesondere für Videoinhalte nur ein
kleiner Anteil der Emissionen in den Rechenzentren anfällt. Schien et
al. geben den Anteil mit 2 bis 11% abhängig vom Endgerät des Benutzers
an. Wichtig sind neben dem Energieverbrauch des Endgeräts ausserdem der
Energiebedarf des Netzwerks und ganz besonders ob die Daten über eine
mobile Datenverbindung geladen werden. Für nicht Videoinhalte beträgt
der Anteil der Rechenzentren zwischen 4 und 48%. (Daniel Schien, 2013)

Zu ähnlichen Ergebnissen kommt der Juni 2020 IEA Bericht über
Rechenzentren und Internetverkehr. Der Anteil am weltweiten
Stromverbrauch wird mit 200 TWh (\~ 0.8% am Endverbrauch) angegeben und
der Stromverbrauch Übertragungsnetzwerke mit 250TWh (\~ 0.8% am
Endverbrauch). Es wird prognostiziert, dass der Anteil am
Internetverkehr über mobile Netzwerke von 50% im Jahr 2019 auf 70% im
Jahr 2022 ansteigen wird, was aufgrund der höheren Energieintensität von
mobilen Netzwerken zu einem Anstieg des Energieverbrauchs führen könnte.
Ausserdem wird darauf verwiesen, dass der Stromverbrauch der
Übertragungsnetzwerke von der Technologie abhängt, wobei 4G ungefähr
5-mal effizienter als 3G ist. (Kamiya, 2020)

Coroma et al. argumentieren, dass bei der Berechnung durch
Internetdatenverkehr entstandenen CO~2~ Emissionen der Stromverbrauch
für die Übertragungsnetzwerke ebenfalls berücksichtigt werden sollte und
geben Formel an, um die entsprechenden Werte abzuschätzen. (Coroama
V.C., 2015)

##   {#section .list-paragraph}

# Literaturverzeichnis

##  {#section-1 .list-paragraph}

Bo Tranberg, O. C. B. L. T. G. I. S. G. B. A., 2019. Real-Time Carbon
Accounting Method for the European Electricity Markets. *Physics and
Society,* p. 20.

Bundesamt für Energie, 2017. *Ergebnisbericht zu Etappe 2: Festlegung
und Objektblätter; Entwurf vom 22. November 2017,* Bern: s.n.

Bundesamt für Energie, 2017. *Umgang mit den Stellungnahmen der
Regionalkonferenzen zu Etappe 2,* Bern: Bundesamt für Energie.

Bundesamt für Energie, 2021. *Elektrizitätsstatistik.* \[Online\]\
Available at:
[https://www.bfe.admin.ch/bfe/de/home/versorgung/statistik-und-geodaten/energiestatistiken/elektrizitaetsstatistik.html]{.underline}\
\[Zugriff am 2021\].

Coroama V.C., S. D. P. C. H. L., 2015. The Energy Intensity of the
Internet: Home and Access Networks. In: *ICT Innovations for
Sustainability. Advances in Intelligent Systems and Computing.*
s.l.:Springer, pp. 137-155.

Daniel Schien, P. S. M. Y. C. P., 2013. Modeling and Assessing
Variabilityin Energy Consumption During the UseStage of Online
Multimedia Services. *Industrial Ecology,* pp. 800-813.

ENTSOE, 2021. *ENTSOE-E Transparency Platform.* \[Online\]\
Available at: [https://transparency.entsoe.eu/]{.underline}\
\[Zugriff am 2021\].

IWSB - Institut für Wirtschaftsstudien Basel AG, 2014. *Bundesamt für
Energie.* \[Online\]\
Available at: [Rechenzentren in der Schweiz - Energieeffizienz:
Stromverbrauch und Effizienzpotenzial]{.underline}\
\[Zugriff am 2021\].

Janine Morley, K. W. M. H., 2018. Digitalisation, energy and data
demand: The impact of Internet traffic on overall and peak electricity
consumption. *Energy Research & Social Science,* pp. 128-137.

Kamiya, G., 2020. *IEA.* \[Online\]\
Available at:
[https://www.iea.org/reports/data-centres-and-data-transmission-networks]{.underline}

Nagra, 2016. *Entsorgungsprogramm 2016 (NAB 16-01),* Wettingen: Nagra.

Sandvine, 2020. \[Online\]\
Available at:
[https://www.sandvine.com/download-report-mobile-internet-phenomena-report-2020-sandvine]{.underline}\
\[Zugriff am 05 2021\].

Swissgrid, 2021. *Energieübersicht.* \[Online\]\
Available at:
[https://www.swissgrid.ch/de/home/customers/topics/energy-data-ch.html]{.underline}\
\[Zugriff am 2021\].

Tomorrow, 2018. *Bug Report Schweizer Daten.* \[Online\]\
Available at:
[https://github.com/tmrowco/electricitymap-contrib/issues/892]{.underline}\
\[Zugriff am 2021\].

Tomorrow, 2021. *Data Sources for Electricitymap.* \[Online\]\
Available at:
[https://github.com/tmrowco/electricitymap-contrib/blob/master/DATA_SOURCES.md]{.underline}

Tomorrow, 2021. *Electricitymap GitHub Repository.* \[Online\]\
Available at:
[https://github.com/tmrowco/electricitymap-contrib]{.underline}\
\[Zugriff am 2021\].

Tomorrow, 2021. *Electricitymap Website.* \[Online\]\
Available at: [https://www.electricitymap.org/map]{.underline}

# Anhang

## Electricitymap Parser für die Schweiz

#!/usr/bin/env python3\
\
import arrow\
\
from . import ENTSOE\
import logging\
import requests\
\
\
def fetch_swiss_exchanges(session, target_datetime, logger):\
*\"\"\"Returns the total exchanges of Switzerland with its neighboring
countries.\"\"\"\
*swiss_transmissions = {}\
for exchange_key in \[\'AT\', \'DE\', \'IT\', \'FR\'\]:\
exchanges = ENTSOE.fetch_exchange(zone_key1=\'CH\',\
zone_key2=exchange_key,\
session=session,\
target_datetime=target_datetime,\
logger=logger)\
if not exchanges:\
continue\
\
for exchange in exchanges:\
datetime = exchange\[\'datetime\'\]\
if datetime not in swiss_transmissions:\
swiss_transmissions\[datetime\] = exchange\[\'netFlow\'\]\
else:\
swiss_transmissions\[datetime\] += exchange\[\'netFlow\'\]\
\
return swiss_transmissions\
\
\
def fetch_swiss_consumption(session, target_datetime, logger):\
*\"\"\"Returns the total consumption of Switzerland.\"\"\"\
*consumptions = ENTSOE.fetch_consumption(zone_key=\'CH\',\
session=session,\
target_datetime=target_datetime,\
logger=logger)\
return {c\[\'datetime\'\]: c\[\'consumption\'\] for c in consumptions}\
\
\
def fetch_production(zone_key=\'CH\', session=None,
target_datetime=None,\
logger=logging.getLogger(\_\_name\_\_)):\
*\"\"\"\
Returns the total production by type for Switzerland.\
Currently the majority of the run-of-river production is missing.\
The difference between the sum of all production types and the total
production is allocated as \'unknown\'.\
The total production is calculated as sum of the consumption, storage
and net imports.\
\"\"\"\
*now = arrow.get(target_datetime, \'Europe/Zurich\') if target_datetime
else arrow.now(tz=\'Europe/Zurich\')\
r = session or requests.session()\
\
exchanges = fetch_swiss_exchanges(r, now, logger)\
consumptions = fetch_swiss_consumption(r, now, logger)\
productions = ENTSOE.fetch_production(zone_key=zone_key, session=r,
target_datetime=now, logger=logger)\
\
if not productions:\
return\
\
for p in productions:\
dt = p\[\'datetime\'\]\
if dt not in exchanges or dt not in consumptions:\
continue\
known_production = sum(\[x or 0 for x in
p\[\'production\'\].values()\])\
\
storage = sum(\[x or 0 for x in p\[\'storage\'\].values()\])\
total_production = consumptions\[dt\] + storage + exchanges\[dt\]\
unknown_production = total_production - known_production\
p\[\'production\'\]\[\'unknown\'\] = unknown_production if
unknown_production \> 0 else 0\
\
return productions\
\
\
if \_\_name\_\_ == \'\_\_main\_\_\':\
print(fetch_production())

###  {#section-2 .list-paragraph}

###  {#section-3 .list-paragraph}

## Folien zur Validierung

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image8.png){width="6.25in"
height="3.5208333333333335in"}![](vertopal_96af99e20f4f4b768c982af86a817716/media/image10.png){width="6.25in"
height="3.5208333333333335in"}

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image12.png){width="6.25in"
height="3.5208333333333335in"}![](vertopal_96af99e20f4f4b768c982af86a817716/media/image14.png){width="6.25in"
height="3.5208333333333335in"}

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image16.png){width="6.25in"
height="3.5208333333333335in"}![](vertopal_96af99e20f4f4b768c982af86a817716/media/image18.png){width="6.25in"
height="3.5208333333333335in"}

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image20.png){width="6.25in"
height="3.5208333333333335in"}![](vertopal_96af99e20f4f4b768c982af86a817716/media/image22.png){width="6.25in"
height="3.5208333333333335in"}

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image24.png){width="6.25in"
height="3.5208333333333335in"}![](vertopal_96af99e20f4f4b768c982af86a817716/media/image26.png){width="6.25in"
height="3.5208333333333335in"}

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image28.png){width="6.25in"
height="3.5208333333333335in"}\
![](vertopal_96af99e20f4f4b768c982af86a817716/media/image30.png){width="6.25in"
height="3.5208333333333335in"}

![](vertopal_96af99e20f4f4b768c982af86a817716/media/image32.png){width="6.25in"
height="3.5208333333333335in"}![](vertopal_96af99e20f4f4b768c982af86a817716/media/image34.png){width="6.25in"
height="3.5208333333333335in"}

###  {#section-4 .list-paragraph}

## Abschätzung der typischen Lastkurve für Schweizer Rechenzentren

[^1]: https://transparency.entsoe.eu/load-domain/r2/totalLoadR2/show

[^2]: https://www.bfe.admin.ch/bfe/de/home/versorgung/statistik-und-geodaten/energiestatistiken/gesamtenergiestatistik.exturl.html/aHR0cHM6Ly9wdWJkYi5iZmUuYWRtaW4uY2gvZGUvcHVibGljYX/Rpb24vZG93bmxvYWQvMTAxMzg=.html

[^3]: https://transparency.entsoe.eu/

[^4]: https://www.swissgrid.ch/de/home/customers/topics/energy-data-ch.html
