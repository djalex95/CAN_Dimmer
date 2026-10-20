# 3D-Modelle â€“ CAN LED Dimmer

115 Bauteile sind mit sichtbaren 3D-Modellen verknÃ¼pft. Die Dateien liegen projektlokal; die Verweise benutzen `${KIPRJMOD}/3dmodels/`.

## Herkunft und Genauigkeit

- WiderstÃ¤nde, Kondensatoren, LEDs und die meisten Halbleiter: installierte KiCad-10-GehÃ¤usemodelle. Diese stellen das StandardgehÃ¤use dar, nicht die exakte Bestellnummer, Beschriftung oder jeden Hersteller-Toleranzwert.
- IC1: vorhandene Hersteller-STEP-Datei fÃ¼r WÃ¼rth Proteus-IV 2621011024000 aus Downloads. Ursprung auf die importierten Pads angepasst, Orientierung visuell geprÃ¼ft.
- J6: vorhandene STEP-Datei 1190299 und zugehÃ¶rige KiCad-Modelltransformation aus Downloads.
- U4: vorhandene STEP-Datei LM5166XDRCR aus Downloads mit der zugehÃ¶rigen Modellrotation.
- L1: vorhandenes SRF0504-102Y-Modell als Darstellung der SRF0504-GehÃ¤usefamilie. Die elektrische BestÃ¼ckung bleibt SRF0504-302Y.
- I1: vereinfachtes GehÃ¤use mit 7,1 Ã— 6,6 Ã— 3,0 mm entsprechend importierter GehÃ¤usebeschreibung.

- J7â€“J10: vom Nutzer bereitgestelltes STEP-Modell 1190297.stp.
- J3/J4 und J5: vom Nutzer bereitgestellte STEP-Modelle TBP02R2-381-02BE und TBP02R2-381-05BE.
- F1/F2: vom Nutzer bereitgestelltes STEP-Modell 01530008Z.stp.
- Transformationen aus den mitgelieferten KiCad-Footprints Ã¼bernommen; Padkoordinaten mit dem PCB abgeglichen und Darstellung von oben und schrÃ¤g geprÃ¼ft.

## Absichtlich ohne KÃ¶rper

- J1/J2: Tag-Connect-KontaktflÃ¤chen ohne dauerhaft bestÃ¼ckten Stecker; absichtlich ohne KÃ¶rper.
- Vier Montagebohrungen: absichtlich ohne KÃ¶rper; keine Schrauben oder Abstandshalter als bestÃ¼ckt angenommen.

## PrÃ¼fung

Nur ModellverknÃ¼pfungen im PCB und in der lokalen Footprint-Bibliothek wurden geÃ¤ndert. Alle Ã¼brigen PCB-Inhalte wurden auf unverÃ¤nderte S-Ausdruck-Tokens geprÃ¼ft. Positionen, Pads, Leiterbahnen, Netze und Kontur sind unverÃ¤ndert. 3D-Ansichten von oben und schrÃ¤g wurden erzeugt und kontrolliert. DRC weiterhin 0 Fehler, 0 offene Verbindungen und die bereits bekannte IC1-Bibliothekswarnung.

Die vereinfachten Modelle und StandardgehÃ¤use sind zur Visualisierung gedacht; daraus folgt keine vollstÃ¤ndige mechanische Kollisions- oder Fertigungsfreigabe. Vereinfachte Modelle liegen als VRML vor; fÃ¼r einen vollstÃ¤ndigen STEP-Export werden entsprechende STEP-Modelle benÃ¶tigt.

## Referenzen

- KiCad-3D-Bibliothek: lokal unter `C:/Program Files/KiCad/10.0/share/kicad/3dmodels`.
- WÃ¼rth Proteus-IV: https://www.we-online.com/en/components/products/PROTEUS-IV
- Phoenix 1190297: https://www.phoenixcontact.com/en-de/products/pcb-terminal-block-lpt-25-2-50-1190297
- Same Sky TBP02R2-381: https://www.sameskydevices.com/product/interconnect/connectors/terminal-blocks/tbp02r2-381-series

## ErgÃ¤nzung Ausgangsanzeigen

D18â€“D21 und R41â€“R44 verwenden projektlokale KiCad-Standardmodelle fÃ¼r 0603-LEDs und 1206-WiderstÃ¤nde. GrÃ¼ne LED-BestÃ¼ckung ist im Schaltplan hinterlegt; das generische 3D-Modell bildet die Lichtfarbe nicht verbindlich ab.

Die drei früheren vereinfachten Stecker-Modelle wurden nach Ersatz durch STEP-Dateien aus dem aktiven Projekt entfernt und separat archiviert.


## STM32G0B1CEU6 / U3

`STM32G0B1CEU6_UFQFPN48_simplified.wrl` ist ein vereinfachtes Visualisierungsmodell, kein Hersteller-CAD-Modell. Gehaeuse 7 x 7 x 0,55 mm, 48 Anschluesse mit 0,5-mm-Raster, Exposed Pad 5,6 x 5,6 mm und Pin-1-Markierung. Abmessungen nach ST DS13560. Der Fertigungs-Footprint basiert auf KiCad `QFN-48-1EP_7x7mm_P0.5mm_EP5.6x5.6mm`.
