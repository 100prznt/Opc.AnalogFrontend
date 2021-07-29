# R&D AnalogFrontend


Dieses Repository dient als Sammler für alle Notizen, Dokumentationen, Ergebnisse welche wärend der Entwicklung und Qualifikation analoger Messverstärker mit D/A-Wandler erstellt werden. Eingesetzt werden soll dieses analoge Frontend zum Anschluss von pH, Redox (ORP) u.Ä. Messelektroden.

# Design
![Blockschaltbild vom analogen Frontend](schemes/frontend.png)

## Anforderungen

* Eingangsimpedanz: > 5 GOhm
* Eingangsspannungsbereich: xxx


# Bauelementeauswahl

## Operationsverstärker
Um die geforderte Eingangsimpedanz (GOhm Bereich) zu erreichen kann vor dem ADC ein Operationsverstärker vorgesehen werden.

* AD8603 (Precision Micropower, Low Noise CMOS, Rail-to-Rail Input/Output Operational Amplifiers)

## Analogdigitalwandler
Digitalisierung und ggf. Vorverstärkung (PGA) des analogen Signals.

* ADS1115 (Ultra-Small, Low-Power, I2C-Compatible, 860-SPS, 16-Bit ADCs with Internal Reference, Oscillator, and Programmable Comparator)
* MCP3427 (16-Bit, Multi-Channel ΔΣ Analog-to-Digital Converter with I2C™ Interface and On-Board Reference)

## Isolator
Galavanische Trennung von Messverstärker und -elektrode um Interferenzen zwischen verschiedenen Elektroden zu vermeiden.

* ADUM5401 (Quad-Channel, 2.5 kV Isolators with Integrated DC-to-DC Converter) (EUR 12,00) NICHT FÜR I2C!

### Diskreter Aufbau (DC/DC + Isolator)

#### DC/DC
* R1SE-0505 (EUR 3,00)
* ADUM5010 (EUR 3,00)

#### Isolator
* SI8600 (EUR 3,00)
* ADUM1250 (EUR 5,00)
