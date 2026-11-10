# Programmentwurf Monopoly
## Spielelemente
- Spielregeln
  - Rundenbasiert
  - Würfeln
- Spieler
  - Spielfigur, z.B. Hut, Hund, Schiff, Auto, ...
  - Anzahl Spieler: 2 bis 4
  - Ort auf dem Spielbrett mit Koordinaten (Spielfeldseite und Spielfeld)
  - Liquidität: Menge in Monopoly
  - Besitz: Grundstücke in seinem Besitz
- Spielbrett
  - Spielfeldseiten
    - Preis Bebauung je Haus/Hotel: 50, 100, 150, 200
    - 11 Felder pro Seite, Ecken gehören zu beiden Seiten oder zu keiner
      - 9 Felder + 2 Ecken
    - Anzahl: 4
    - Reihenfolge
- Spielfeld
  - Attribute
    - Spielfeldseite
    - Reihenfolge
  - Spielfeldtypen
    - Grundstück
      - Kaufbares / Besitzbares Feld
      - Attribute
        - Wert
        - Grundmiete
        - Name
        - Berechnete Miete abhängig von Grundstückstyp
        - Hypotheken Wert: Wert / 2 (Halber Wert)
      - Grundstückstypen
        - Straßen
          - Farbe: Zusammengehörende Gruppe von Straßen
          - Anzahl Häuser: 0 - 4 Häuser
          - Hotel vorhanden: Ja/Nein
          - Bedingung: Entweder Häuser oder Hotel
          - Berechnete Miete: 
            - Grundmiete
            - Alle Straßen eine Gruppe im Besitz, dann doppelte Miete
            - Mit Häusern höhere Miete
        - Bahnhof
          - Namen: Süd-, West-, Nord- und Hauptbahnhof
          - Berechnete Miete:
            - 1 Bahnhof: 25 Monopoly
            - 2 Bahnhöfe: 50 Monopoly
            - 3 Bahnhöfe: 100 Monopoly
            - 4 Bahnhöfe: 200 Monopoly
            - Implementierungshinweis: Grundmiete * 2 ^(Anzahl Bahnhöfe - 1)
        - Werk
          - Namen: Wasserwerk / Elektrizitätswerk
          - Berechnete Miete:
            - 1 Werk: 4 * Augenzahl
            - 2 Werke: 10 * Augenzahl
    - Aktionsfeld
      - unverkäuflich --> gehört dem Spiel
      - Spieler muss Aktion ausführen
      - Aktionsfeldtypen
        - Ereignisfeld
          - Aktion: Ereigniskarte aufnehmen
        - Gemeinschaftsfeld
          - Aktion: Gemeinschaftskarte aufnehmen
        - Frei Parken
          - Aktion: Keine Aktion
        - Direkt in das Gefängnis
          - Aktion: Direkt ins Gefängnis gehen ohne über Los zu gehen. Kein Geld beziehen.
        - Gefängnis
          - Aktion:
            - Zu Besuch: Keine Aktion
            - Im Gefängnis: Aus dem Gefängnis freikommen
        - Steuerfeld
          - Steuerbetrag: Wert in Monopoly
          - Aktion: Fester Betrag an Steuern bezahlen an Bank
        - Los
          - Aktion: 
            - Über Los ziehen: 200 Monopoly bekommen
            - Direkt auf Los: 400 Monopoly bekommen
- Aktionskarten
  - Typen: Ereigniskarten, Gemeinschaftskarten
  - Beschreibung: Text
  - Aktion: 
    - Geld bekommen
    - Geld bezahlen
    - Frei aus dem Gefängnis
    - Spielfigur bewegen
  - Hinweise: Kunde muss alle Beschreibungen und deren Aktionen definieren
- Bebauung
  - Hotels
  - Haus
- Bank
  - Bezahlt Geld aus
    - Über/Auf Los gehen
    - Aktionskarten
    - Hyotheken ausgeben
    - Abgerissene Häuser / Hotels
  - Bekommt Geld für
    - Gebaute Häuser / Hotels
    - Aktionskarten
    - Steuerfeld
    - Freikaufen aus dem Gefängnis
    - Hypothekenzinsen
    - Grundstückskauf
- Spielzug
  1. Aktionen ausführen
  2. Würfel
  3. Spielfigur ziehen
  4. Miete bezahlen / Grundstück kaufen

## Begriffe
- Handeln
  - Grundstück gegen Geld
- Tauschen
  - Grundstück gegen Grundstück

## Spielregeln
- Auf einem Grundstück dürfen nur Häuser stehen, wenn einem Spieler alle Grundstücke dieser Farbe gehören

## Aktionen
- Handeln inkl. Tauschen
  - Grundstücke von anderen Spielern kaufen
  - Ein Spieler darf Handeln, wenn er am Spielzug ist
  - Ein Spieler darf während seines gesamten Spielzuges handeln
- Handeln und Tauschen mit Bebauung
  - Bei Übernahme eines Teils der Straßen einer Farbe muss die Bebauung entfernt werden
  - Bei Übernahme aller Straßen einer Farbe kann die Bebauung mit verkauft werden
- Kaufen
  - Spieler betritt freies Spielfeld (gehört keinem anderen)
  - Kaufpreis an Bank bezahlen
  - Karte in seinen Besitz nehmen
- Versteigern
  - Geld bieten
  - Alle dürfen bieten
  - Grundgebot: 10 Monopoly
  - Bietschritte: min. 1 Monopoly
  - Reihenfolge beim Bieten ist frei. Spielerreihenfolge hat keinen Einfluss
  - Versteigerungsende definieren?
- Miete bezahlen
  - Spieler betritt ein Spielfeld, das einem anderen Spieler gehört
  - Keine Miete bei
    - Besitzer bekommt nicht mit, dass ein Spieler auf seinem Spielfeld steht. Sobald der nächste Spieler gewürfelt hat, muss keine Miete mehr bezahlt werden
  - Bei Pasch müsste auf jedem betretenen Spielfeld Miete bezahlt werden
  - Erst Miete bezahlen, dann ist ein Handel möglich
- Miete einnehmen
  - Verdopplung der Mieteinnahmen, wenn einem Spieler alle Straßen einer Farbe gehören
  - Mieteinnahmen erhöhen sich, wenn Bebauung auf dem Spielfeld vorhanden ist
  - Vermieter muss sich darum kümmern, dass er Miete bekommt
  - Mieteinnahmen gehen an den Besitzer des Spielfeldes
- Häuser bauen
  - Geht erst, wenn einem Spieler alle Straßen einer Farbe gehören
  - Bevor ein Spieler würfelt, darf er auf allen Straßen in seinem Besitz bauen
  - Geld geht an die Bank
  - Es dürfen 4 Häuser auf einem Grundstück stehen und die anderen Straßen der Farbe dürfen leer sein.
- Hotel bauen
  - Wenn 4 Häuser auf einer Straße stehen, darf eine Hotel gebaut werden
  - Das Hotel ersetzt die Häuser
  - Häuser stehen wieder zum Bau anderer Häuser bereit
  - Häuser und Kaufpreis transformieren zu einem Hotel
- Häuser abreisen
  - Die Hälfte des Kaufpreises wird erstattet
  - Während des gesamten Spielzugs, darf ein Spieler auf allen Straßen in seinem Besitz Bebauung abreisen
- Hypothek aufnehmen
  - Karte verdecken
  - Hälfte Grundstückswert als Liquidität --> Ein anderer Betrag geht nicht
  - Keine Mieteinnahmen
  - Nur als freie Straße ohne Häuser
- Hypothek auflösen
  - Hypothek komplett zurückbezahlen
  - Zinsen (10%) an Bank bezahlen
  - Karte wieder aufdecken
- Bankrott anmelden
  - Spieler hat Kosten, die er nicht bezahlen kann, aber bezahlen muss
  - Verbindlichkeiten > Liquidität
  - Szenario 1
    - Spieler A muss an Spieler B 1.000 Monopoly Miete bezahlen
    - Spieler A hat zu wenig Liquidität
    - Spieler A hat Grundstücke mit Kaufpreis 1.500 Monopoly (mögliche Hypothek sind 750 Monopoly) ohne Bebauung
    1. Grundstücke handeln, um Liquidität zu bekommen --> Keiner will handeln
    2. Hypothek aufnehmen, um Liquidität zu bekommen --> Hypothek zu klein
    3. Spieler B bekommt alle Grundstücke von Spieler A
    4. Spieler A ist bankrott und verlässt das Spiel
  - Szenario 2
    - Spieler A muss an Bank 1.000 Monopoly Miete bezahlen
    - Spieler A hat zu wenig Liquidität
    - Spieler A hat Grundstücke mit Kaufpreis 1.500 Monopoly (mögliche Hypothek sind 750 Monopoly) ohne Bebauung
    1. Grundstücke handeln, um Liquidität zu bekommen --> Keiner will handeln
    2. Hypothek aufnehmen, um Liquidität zu bekommen --> Hypothek zu klein
    3. Grundstücke gehen direkt an die Bank und werden versteigert --> Erlös geht an die Bank
    4. Spieler A ist bankrott und verlässt das Spiel
  - Szenario 3
    - Spieler A muss an Spieler B 1.000 Monopoly Miete bezahlen
    - Spieler A hat zu wenig Liquidität
    - Spieler A hat Grundstücke mit Kaufpreis 2.000 Monopoly (mögliche Hypothek sind 1.000 Monopoly) ohne Bebauung
    - Spieler A nimmt Hypothek auf alle seine Grundstücke auf --> 0 Monopoly übrig als Liquidität
    - Spieler A spielt weiter
    - Spieler A muss Miete bei Spieler C bezahlen
    1. Grundstücke handeln, um Liquidität zu bekommen --> Keiner will handeln
    2. Hypothek aufnehmen, um Liquidität zu bekommen --> Hypothek zu klein
    3. Spieler C bekommt alle Grundstücke inklusive Hypothek von Spieler A
      - Spieler C muss Hypothek begleichen oder 10% der Hypothek an Bank bezahlen
      - Wenn Spielcer C die Hypothek nicht begleichen kann, wird das Grundstück versteigert
    4. Spieler A ist bankrott und verlässt das Spiel
- Geld bekommen, bei über Los gehen
  - 200 Monopoly von der Bank an den Spieler
- Spieler landet direkt auf Los
  - Spieler bekommt 400 Monopoly von der Bank
- Würfeln
  - Zufällige Zahl zwischen 2 und 12
- Spielfigur ziehen
  - Spieler bewegt seine Figur auf das Grundstück, je nach Augenzahl der Würfel
- Gemeinschaftskarte aufnehmen
  - Aufgabe auf Karte ausführen
  - Karte behalten, wenn "Freikommen aus Gefängnis"
  - Karte zurücklegen unter den Stapel
- Ereigniskarte aufnehmen
  - Aufgabe auf Karte ausführen
  - Karte behalten, wenn "Freikommen aus Gefängnis"
  - Karte zurücklegen unter den Stapel
- Start vorbereiten: 
  - Spielfigur auf Los stellen
  - 1.500 Monopoly
  - Reihenfolge der Spieler definieren
- Pasch würfeln --> gleicher Spieler ist noch einmal an der Reihe
  - 3 mal Pasch würfeln in einem Zug --> Spieler kommt ins Gefängnis
- Aus dem Gefängnis freikommen
  - Pro Spielzug 3 Versuche einen Pasch zu würfeln
  - Bei Pasch freikommen aus Gefängnis
  - Nach dem Freikommen, normaler Spielzug
    - Ein Pasch der 3-Pasch-Regel ist bereits verbraucht, um aus dem Gefängnis frei zu kommen
    - Bei zwei Pasch ist man dadurch wieder im Gefängnis
  - Vor dem Spielzug 50 Monopoly an Bank bezahlen
  - Gemeinschafts- oder Ereigniskarte einlösen
  - Nach 3 Spielzügen muss 50 Monopoly bezahlt werden, um frei zu kommen --> letze Augenzahl wird zum Ziehen verwendet
- Spieler landet mit Augenzahl auf dem Gefängnis
  - Nur zu Besuch
  - Keine besondere Aktion
  - Spieler kann normal weiterziehen im nächsten Spielzug 
- Spiel beendet
  - Es existiert nur noch ein Spieler, alle anderen Spieler sind bankrott






