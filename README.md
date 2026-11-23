# ASE TINF24 Monopoly

Demonstrationsprojekt zur Vorlesung **Advanced Software Engineering** an der Dualen Hochschule Baden-Württemberg Karlsruhe (DHBW Karlsruhe), Kurs TINF24.

Am Beispiel des Brettspiels Monopoly werden die in der Vorlesung behandelten Konzepte gezeigt, unter anderem Domain Driven Design, Clean Architecture und weitere Prinzipien des Software Engineerings. Das Spiel wird als Konsolenanwendung umgesetzt.

## Dokumentation

- Domänenmodell
  - [Sammlung](docs/domain-model/01-Sammlung.md): Spielelemente, Begriffe, Spielregeln und Aktionen als lose Sammlung

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
