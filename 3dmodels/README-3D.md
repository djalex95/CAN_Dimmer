# 3D-Modelle – CAN LED Dimmer

115 Bauteile sind mit sichtbaren 3D-Modellen verknüpft. Die Dateien liegen projektlokal; die Verweise benutzen `${KIPRJMOD}/3dmodels/`.

## Herkunft und Genauigkeit

- Widerstände, Kondensatoren, LEDs und die meisten Halbleiter: installierte KiCad-10-Gehäusemodelle. Diese stellen das Standardgehäuse dar, nicht die exakte Bestellnummer, Beschriftung oder jeden Hersteller-Toleranzwert.
- IC1: vorhandene Hersteller-STEP-Datei für Würth Proteus-IV 2621011024000 aus Downloads. Ursprung auf die importierten Pads angepasst, Orientierung visuell geprüft.
- J6: vorhandene STEP-Datei 1190299 und zugehörige KiCad-Modelltransformation aus Downloads.
- U4: vorhandene STEP-Datei LM5166XDRCR aus Downloads mit der zugehörigen Modellrotation.
- L1: vorhandenes SRF0504-102Y-Modell als Darstellung der SRF0504-Gehäusefamilie. Die elektrische Bestückung bleibt SRF0504-302Y.
- I1: vereinfachtes Gehäuse mit 7,1 × 6,6 × 3,0 mm entsprechend importierter Gehäusebeschreibung.

- J7–J10: vom Nutzer bereitgestelltes STEP-Modell 1190297.stp.
- J3/J4 und J5: vom Nutzer bereitgestellte STEP-Modelle TBP02R2-381-02BE und TBP02R2-381-05BE.
- F1/F2: vom Nutzer bereitgestelltes STEP-Modell 01530008Z.stp.
- Transformationen aus den mitgelieferten KiCad-Footprints übernommen; Padkoordinaten mit dem PCB abgeglichen und Darstellung von oben und schräg geprüft.

## Absichtlich ohne Körper

- J1/J2: Tag-Connect-Kontaktflächen ohne dauerhaft bestückten Stecker; absichtlich ohne Körper.
- Vier Montagebohrungen: absichtlich ohne Körper; keine Schrauben oder Abstandshalter als bestückt angenommen.

## Prüfung

Nur Modellverknüpfungen im PCB und in der lokalen Footprint-Bibliothek wurden geändert. Alle übrigen PCB-Inhalte wurden auf unveränderte S-Ausdruck-Tokens geprüft. Positionen, Pads, Leiterbahnen, Netze und Kontur sind unverändert. 3D-Ansichten von oben und schräg wurden erzeugt und kontrolliert. DRC weiterhin 0 Fehler, 0 offene Verbindungen und die bereits bekannte IC1-Bibliothekswarnung.

Die vereinfachten Modelle und Standardgehäuse sind zur Visualisierung gedacht; daraus folgt keine vollständige mechanische Kollisions- oder Fertigungsfreigabe. Vereinfachte Modelle liegen als VRML vor; für einen vollständigen STEP-Export werden entsprechende STEP-Modelle benötigt.

## Referenzen

- KiCad-3D-Bibliothek: lokal unter `C:/Program Files/KiCad/10.0/share/kicad/3dmodels`.
- Würth Proteus-IV: https://www.we-online.com/en/components/products/PROTEUS-IV
- Phoenix 1190297: https://www.phoenixcontact.com/en-de/products/pcb-terminal-block-lpt-25-2-50-1190297
- Same Sky TBP02R2-381: https://www.sameskydevices.com/product/interconnect/connectors/terminal-blocks/tbp02r2-381-series

## Ergänzung Ausgangsanzeigen

D18–D21 und R41–R44 verwenden projektlokale KiCad-Standardmodelle für 0603-LEDs und 1206-Widerstände. Grüne LED-Bestückung ist im Schaltplan hinterlegt; das generische 3D-Modell bildet die Lichtfarbe nicht verbindlich ab. Aktuelle Vorschau: `../Review-Ausgangsanzeigen/PCB-3D.png`.
