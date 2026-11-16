# CAN LED Dimmer

KiCad-10-Projekt fuer einen vierkanaligen CAN-/Bluetooth-LED-Dimmer.

## Projekt oeffnen

`CAN LED Dimmer.kicad_pro` oeffnen. Bibliotheken und 3D-Modelle sind projektlokal ueber `${KIPRJMOD}` eingebunden.

## Dateien

| Datei / Ordner | Inhalt |
|---|---|
| CAN LED Dimmer.kicad_sch | Hauptblatt / Hierarchie |
| MCU - Bluetooth - CAN.kicad_sch | Controller und Kommunikation |
| Power Supply.kicad_sch | Spannungsversorgung |
| LED Outputs.kicad_sch | Ausgangsstufen |
| CAN LED Dimmer.kicad_pcb | Aktueller Layoutstand |
| CAN LED Dimmer.kicad_dru | Benutzerdefinierte Designregeln |
| CAN LED Dimmer-eagle-import.kicad_sym | Bauteilbibliothek, aus Import weiterentwickelt |
| CAN_LED_Dimmer-MCU.kicad_sym | STM32C552RET6_GROUPED |
| CAN_LED_Dimmer-layout.pretty | Projekt-Footprints |
| 3dmodels | Modelle fuer Platine und Bibliotheks-Footprints |
| sym-lib-table / fp-lib-table | Bibliothekszuordnungen |

## Weiterbearbeitung

Zielcontroller: STM32C552RET6 im LQFP64. Bibliotheksaenderungen werden nicht automatisch in bereits platzierte Symbole und Footprints uebernommen. Aktualisierungen gezielt aus den Bibliotheken uebernehmen, danach Verbindungen sowie ERC/DRC pruefen.

Das Projekt ist ein Arbeitsstand, keine Fertigungsfreigabe. Fruehere ERC-/DRC-Ergebnisse gelten nicht automatisch fuer aktuelle Aenderungen. Die Bereinigung hat weder Schaltung noch Layout geaendert.

Vier LED-Kanaele, vorgesehen ca. 5 A je Kanal und 1 kHz PWM; Versorgung 12 V, optional 24 V. Transientenfestigkeit, thermische Belastung und Signalqualitaet am fertigen Entwurf verifizieren.

Der gemeinsame ACT45B/SRF0504-Footprint hat Kupferpads fuer beide Gehaeuse, aber Pastenfenster fuer TDK. Fuer automatische Bourns-Bestueckung ist die Pastenschablone anzupassen. Die Bauteile sind elektrisch nicht identisch.

## Sicherungen

Git-Historie bleibt in `.git` erhalten. Alte lokale Dateihistorie, manuelle Sicherungen und veraltete Berichte liegen ausserhalb des Projekts unter `../KiCadProject-Archiv/`. Neue KiCad-Sicherungen weiterhin verwenden; sie wurden nicht deaktiviert.

Lokale Benutzereinstellungen (`*.kicad_prl`) bleiben erhalten und werden von Git ignoriert.
