# ASE TINF24 Monopoly

Demonstrationsprojekt zur Vorlesung **Advanced Software Engineering** an der Dualen Hochschule Baden-Württemberg Karlsruhe (DHBW Karlsruhe), Kurs TINF24.

Am Beispiel des Brettspiels Monopoly werden die in der Vorlesung behandelten Konzepte gezeigt, unter anderem Domain Driven Design, Clean Architecture und weitere Prinzipien des Software Engineerings. Das Spiel wird als Konsolenanwendung umgesetzt.

## Dokumentation

- Domänenmodell
  - [Sammlung](docs/domain-model/01-Sammlung.md): Spielelemente, Begriffe, Spielregeln und Aktionen als lose Sammlung
  - [Struktur nach Informationsart](docs/domain-model/02a-Struktur-nach-Informationsart.md): Begriffe, Spielelemente, Regeln, Abläufe, Szenarien und offene Fragen
  - [Struktur nach Themen](docs/domain-model/02b-Struktur-nach-Themen.md): Spielbrett, Spielablauf, Besitz, Geld, Gefängnis, Karten und Bankrott
  - [Struktur nach Themen und Informationsart](docs/domain-model/02c-Struktur-nach-Themen-und-Informationsart.md): Themen als Kapitel, darin Begriffe, Spielelemente, Regeln, Abläufe, Szenarien und offene Fragen
  - [Glossar](docs/domain-model/03-Glossar.md): Eindeutige Begriffe der Domäne als Grundlage der Ubiquitous Language

## Voraussetzungen

- Java 26
- Maven

## Bauen und Testen

```sh
mvn clean install
```

Nur die Tests ausführen:

```sh
mvn test
```
