# CAN LED Dimmer

Vierkanaliger LED-Dimmer mit CAN-Bus und Bluetooth LE, entwickelt in KiCad 10.

## Eckdaten

- 4 LED-KanÃ¤le mit je etwa 5 A, PWM 1 kHz (strombegrenzte LED-Streifen als Last angenommen)
- Versorgung 12 V nominal, 24 V optional; zwei Eingangszweige mit je 10-A-Sicherung und TVS-Schutz
- Steuerung: STM32G0B1CCT6 mit externem 8-MHz-Quarz
- Kommunikation: CAN (TLT9251VLE, externe Terminierung) und Bluetooth LE (WÃ¼rth Proteus-IV 2621011024000)
- High-Side-Schalter BTS70202 (je zwei KanÃ¤le) mit Stromdiagnose, P-Kanal-MOSFETs fÃ¼r die Lastzweige
- Spannungsversorgung: LM5166X (5 V) und NCP730 (3,3 V)
- 4 TastereingÃ¤nge (J5), EEPROM M24C04, Programmierung Ã¼ber Tag-Connect TC2030 (J1, J2)
- Platine 100 Ã— 75 mm, 4 Lagen, 1,6 mm, nur Oberseite bestÃ¼ckt, vier Montagebohrungen Ã˜ 3,2 mm

## Aufbau des Projekts

| Datei / Ordner | Inhalt |
|---|---|
| `CAN LED Dimmer.kicad_pro` | Projektdatei, hier Ã¶ffnen |
| `CAN LED Dimmer.kicad_sch` | Schaltplan-Ãœbersicht (hierarchisch) |
| `CAN_LED_Dimmer_MCU.kicad_sch` | Blatt MCU, Bluetooth, CAN |
| `CAN_LED_Dimmer_2.kicad_sch` | Blatt Spannungsversorgung |
| `CAN_LED_Dimmer_3.kicad_sch` | Blatt LED-AusgÃ¤nge |
| `CAN LED Dimmer.kicad_pcb` | Platinenlayout |
| `CAN LED Dimmer-eagle-import.kicad_sym` | Symbolbibliothek (aus Eagle/Fusion importiert) |
| `CAN_LED_Dimmer-layout.pretty` | angepasste Footprint-Varianten fÃ¼r dieses Layout |
| `3dmodels/` | 3D-Modelle, Herkunft siehe `3dmodels/README-3D.md` |

Alle Bibliotheken und 3D-Modelle liegen im Projekt und sind Ã¼ber `${KIPRJMOD}` eingebunden. Nach dem Klonen reicht eine KiCad-10-Installation, es mÃ¼ssen keine Bibliothekspfade angepasst werden.

## Ã–ffnen

1. Repository klonen oder als ZIP herunterladen.
2. In KiCad 10 die Datei `CAN LED Dimmer.kicad_pro` Ã¶ffnen.

## Stand

Arbeitsstand, noch keine Fertigungsfreigabe:

- Layout vollstÃ¤ndig geroutet, DRC zuletzt ohne Fehler und offene Verbindungen; bekannte Bibliotheks- und Silkscreen-Warnungen sind noch offen.
- ERC hat noch offene Meldungen, vor allem durch importierte Pin-Typen.
- Strombelastbarkeit, Thermik bei viermal 5 A und Schaltflanken sind am Prototyp zu prÃ¼fen.
- Lagenaufbau und Kupferdicke sind mit dem Hersteller festzulegen.
- Eingangsschutz fÃ¼r 24 V und Transienten ist bewusst zurÃ¼ckgestellt.

Historische Reviews, Zwischenstände und unbenutzte Importdateien wurden separat außerhalb des Projektordners archiviert. Die aktive Footprint-Bibliothek ist `CAN_LED_Dimmer-layout.pretty`.
