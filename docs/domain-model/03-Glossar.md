# Programmentwurf Monopoly – Glossar

Das Glossar legt für jeden Begriff der Domäne genau eine Bedeutung fest. Es ist der erste Schritt zur Ubiquitous Language: Dieselben Begriffe werden in Gesprächen, in der Dokumentation und später im Code verwendet. Begriffe in der Spalte „Nicht verwenden“ kommen in der [Sammlung](01-Sammlung.md) und den Strukturdokumenten noch vor und werden durch den Begriff in der ersten Spalte ersetzt.

Einträge unter **offen** am Ende einer Tabelle sind noch nicht entschieden. Die zugehörigen Fragen stehen in den Strukturdokumenten unter „Offene Fragen“ → „Fachsprache“ bzw. „Annahmen im Glossar“, z.B. in der [Struktur nach Themen und Informationsart](02c-Struktur-nach-Themen-und-Informationsart.md#offene-fragen).

## Spielbrett und Felder

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Aktionsfeld | Spielfeld, das nicht gekauft werden kann. Beim Betreten wird eine Feldaktion ausgeführt | |
| Bahnhof | Grundstück, dessen Miete von der Anzahl der Bahnhöfe des Besitzers abhängt | |
| Farbgruppe | Alle Straßen derselben Farbe | Farbe, Gruppe |
| Feldaktion | Was beim Betreten eines Aktionsfeldes passiert | Aktion |
| Grundstück | Spielfeld, das gekauft werden kann: Straße, Bahnhof oder Werk | Spielfeld, wenn es um Kaufen, Besitz oder Miete geht |
| Spielbrett | Das Brett mit 4 Spielfeldseiten, auf dem die Spielfiguren gezogen werden | |
| Spielfeld | Jedes einzelne Feld auf dem Spielbrett | Feld; Grundstück, wenn das Feld gemeint ist, auf das die Spielfigur zieht |
| Spielfeldseite | Eine der 4 Seiten des Spielbretts. Legt die Baukosten für die Straßen dieser Seite fest | |
| Straße | Grundstück, das zu einer Farbgruppe gehört und bebaut werden kann | Grundstück, wenn es um Bebauung geht |
| Werk | Grundstück, dessen Miete von der Anzahl der Werke des Besitzers und der Augenzahl abhängt | |
| **offen** |
| Ecke | Offen, welche Spielfelder die Ecken sind. Annahme: Spielfeld an der Ecke des Spielbretts: Los, Gefängnis, Frei Parken, Direkt in das Gefängnis | |

## Spielablauf und Würfeln

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Pasch | Wurf, bei dem beide Würfel dieselbe Augenzahl zeigen | |
| Runde | Jeder Spieler hatte einmal einen Spielzug | |
| Spieler | Teilnehmer am Spiel. Besitzt eine Spielfigur, Geld und Grundstücke | |
| Spielfigur | Figur des Spielers auf dem Spielbrett, z.B. Hut, Hund, Schiff, Auto | |
| Spielzug | Alles, was ein Spieler tut, solange er an der Reihe ist, auch mehrere Würfe nach einem Pasch | Zug, am Spielzug sein |
| **offen** |
| Aktionen im Spielzug | Offen, wie Handeln, Bauen, Hypothek aufnehmen oder auflösen zusammen heißen | Aktionen ausführen |
| Augenzahl | Offen, siehe Wurf. Annahme: Summe der beiden Würfel eines Wurfs | |
| Wurf | Offen, ob mit zwei Würfeln gewürfelt wird. Annahme: Einmaliges Würfeln mit zwei Würfeln | Zufällige Zahl zwischen 2 und 12 |

## Besitz und Bebauung

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Abreißen | Bebauung von einer Straße entfernen. Die Bank erstattet die Hälfte der Baukosten | Bebauung entfernen |
| Baukosten | Preis eines Hauses oder Hotels, festgelegt je Spielfeldseite | Preis Bebauung, Kaufpreis bei Häusern und Hotels |
| Bebauung | Häuser oder Hotel auf einer Straße | |
| Besitzer | Spieler, dem ein Grundstück gehört | Vermieter |
| Freies Grundstück | Grundstück, das keinem Spieler gehört | gehört keinem anderen |
| Gebot | Betrag, den ein Spieler beim Versteigern bietet | |
| Grundmiete | Miete eines Grundstücks ohne Bebauung und ohne vollständige Farbgruppe | |
| Haus | Bebauung, bis zu 4 je Straße | |
| Hotel | Bebauung, die 4 Häuser auf einer Straße ersetzt | |
| Kaufen | Ein Spieler erwirbt ein freies Grundstück von der Bank zum Kaufpreis | |
| Kaufpreis | Preis eines Grundstücks beim Kaufen | Wert, Grundstückswert |
| Miete | Betrag, den ein Spieler beim Betreten eines Grundstücks an dessen Besitzer zahlt | |
| Versteigern | Ein Grundstück geht an den Spieler mit dem höchsten Gebot | |
| **offen** |
| Handeln / Tauschen | Offen, ob Geld und Grundstücke gemischt werden dürfen. Bisher: Handeln = Grundstück gegen Geld, Tauschen = Grundstück gegen Grundstück | Grundstücke von anderen Spielern kaufen |
| Karte zum Grundstück | Offen, ob es eine Karte zum Grundstück gibt. Bisher: „Karte verdecken“, „Karte in seinen Besitz nehmen“ | Karte |

## Geld und Bank

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Hypothek auflösen | Hypothekenwert und Hypothekenzinsen an die Bank zahlen | Hypothek zurückbezahlen, Hypothek begleichen |
| Hypothekenwert | Hälfte des Kaufpreises | Hypotheken Wert |
| Monopoly | Währungseinheit des Spiels | |
| Steuer | Fester Betrag, den ein Spieler auf dem Steuerfeld an die Bank zahlt | Steuerbetrag |
| **offen** |
| Bank | Offen, ob die Bank alle freien Grundstücke besitzt. Bedeutung: Zahlt Geld an Spieler aus und erhält Geld von Spielern | |
| Hypothek | Offen, ob nur für Straßen oder für alle Grundstücke ohne Bebauung. Bedeutung: Der Spieler erhält von der Bank den Hypothekenwert, das Grundstück bringt keine Miete | |
| Hypothekenzinsen | Offen, worauf sich die 10 % beziehen. Annahme: 10 % des Hypothekenwerts, beim Auflösen der Hypothek an die Bank zu zahlen | Zinsen |
| Liquidität | Offen, ob der Begriff bleibt oder z.B. durch Guthaben ersetzt wird. Bedeutung: Geld, das ein Spieler besitzt | Menge in Monopoly |

## Gefängnis

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Freikommen | Das Gefängnis verlassen: durch Pasch, Zahlung von 50 Monopoly oder Gefängnis-frei-Karte | |
| Im Gefängnis | Spieler sitzt im Gefängnis und muss freikommen, bevor er normal weiterziehen kann | |
| Zu Besuch | Spielfigur steht mit normaler Augenzahl auf dem Gefängnis, ohne im Gefängnis zu sein | Nur zu Besuch |

## Karten

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Aktionskarte | Oberbegriff für Ereigniskarte und Gemeinschaftskarte | Karte |
| Ereigniskarte | Aktionskarte vom Ereigniskartenstapel | |
| Gefängnis-frei-Karte | Aktionskarte, die der Spieler behält und später zum Freikommen einlöst | Frei aus dem Gefängnis, Freikommen aus Gefängnis |
| Gemeinschaftskarte | Aktionskarte vom Gemeinschaftskartenstapel | |
| Kartenaktion | Was beim Ziehen einer Aktionskarte passiert | Aktion, Aufgabe auf Karte |
| Kartenstapel | Stapel der Ereignis- bzw. Gemeinschaftskarten. Gezogene Karten kommen unter den Stapel | Stapel |

## Bankrott

| Begriff | Bedeutung | Nicht verwenden |
|---|---|---|
| Bankrott | Ein Spieler kann seine Verbindlichkeiten nicht bezahlen und scheidet aus dem Spiel aus | |
| Verbindlichkeit | Betrag, den ein Spieler zahlen muss | Kosten |
