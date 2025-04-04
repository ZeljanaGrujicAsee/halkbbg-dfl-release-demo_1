# Repozitorijum za Arhiviranje Dokumenata Isporučenih Halk banci

Ovaj repozitorijum služi kao centralizovano mesto za arhiviranje dokumentacije koja se isporučuje banci prilikom svakog release-a. Cilj je da se obezbedi jasna organizacija, istorija promena i efikasna pretraga dokumenata prema nazivu i/ili sadržaju fajla.

## Struktura Repozitorijuma

Repozitorijum je organizovan po sledećoj strukturi:

```
halkbbg-dfl-release-demo_1/
├── main/
│   ├── configuration-packages
│   ├── hemlfiles
│   ├── sql-scripts
│   ├── documents/
│   │   ├── ProizvodA/
│   │   │  ├── release-1.0.0/
│   │   │  │  ├── YYYY-MM-DD_HH_MM/ (timestamp kreiranja PR-a)
│   │   │  │  │  ├── dokument1.md
│   │   │  │  │  ├── dokument2.pdf
│   │   │  │  │  └── ...
│   │   │  │  ├── YYYY-MM-DD_HHMMSS/
│   │   │  │  │  ├── ...
│   │   │  │  │   ── ...
│   │   │  ├── release-1.1.0/
│   │   │  │  ├── ...
│   │   │  │  └── ...
│   │   ├── ProizvodB/
│   │   │  ├── release-2.0.0/
│   │   │  ├── ...
│   │   │  └── ...
├── Archive/
│   ├── documents/
│   │   ├── ProizvodA/
│   │   │  ├── release-1.0.0/
│   │   │  │  ├── YYYY-MM-DD_HH_MM/ (timestamp kreiranja PR-a)
│   │   │  │  │  ├── dokument1.md
│   │   │  │  │  ├── dokument2.pdf
│   │   │  │  │  └── ...
│   │   │  │  ├── YYYY-MM-DD_HHMMSS/
│   │   │  │  │  ├── ...
│   │   │  │  │   ── ...
│   │   │  ├── release-1.1.0/
│   │   │  │  ├── ...
│   │   │  │  └── ...
│   │   ├── ProizvodB/
│   │   │  ├── release-2.0.0/
│   │   │  ├── ...
│   │   │  └── ...
└── ...
```

* **` halkbbg-dfl-release-demo_1/`**: Root direktorijum repozitorijuma.
* **` Archive branch`**: grana na kojoj će se arhivirati dokumenta isporučena banci.
* **`ProizvodA/`, `ProizvodB/`, ...**: Folder za svaki proizvod npr. DigitalBranch, DigitalCIF, DigitalOrigination....
* **`release-1.0.0/`, `release-1.1.0/`, ...**: Podfolder za svaku verziju (release) proizvoda.
* **`YYYY-MM-DD_HHMMSS/`**: Podfolder za svaki pull request, sa timestamp-om kreiranja PR-a.
* **`dokument1.md`, `dokument2.pdf`, ...**: Dokumenti vezani za svaki pull request.

## Mehanizam Arhiviranja

1.  **Kreiranje Pull Request-a (PR), Merge PR-a, Kreiranje Release-a, Kopiranje Dokumenata:**
    * Pull request sa izmenama dokumenata se kreira na repozitorijumu (https://github.com/assecosee/halkbbg-dfl-release/tree/main) koji generiše .zip koji se isporučuje banci, a sadržaj repoa-a se prazni i priprema za sledeću isporuku, pre nego što se sadržaj ovog repo-a isprazni sadržaj documents podfoldera se kopira na **Archive granu** repozitorijuma.

## Prednosti

* **Jasna organizacija:** Dokumentacija je organizovana po proizvodima, verzijama i pull request-ovima.
* **Precizna istorija:** Timestamp-ovi omogućavaju precizno praćenje redosleda primene promena.
* **Efikasna pretraga:** Lako je pronaći dokumentaciju vezanu za određeni proizvod, verziju ili pull request.
* **Automatizacija:** Proces arhiviranja se može automatizovati pomoću Git akcija ili sličnih alata.

## Upotreba

* Koristiti Markdown format (`.md`) za dokumentaciju, jer se na taj način omogućava pretraga po imenu i/ili sadržaju fajlova.
