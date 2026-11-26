Hier ist der Inhalt der angehängten Datei als strukturierter Markdown-Text:

# Aufbau des Datensatzes der Datei „Bio“

* **#0 PK:** Laufende Nr. der Grunddatei. Sonstige Angaben (Parameter), mit denen u.U. die Auswahl oder Datenauswahl erreicht werden kann (analog Datei Prov), stehen unter „Abkürzungen“.
    * **#0a UNIANG: Funktion an der Uni Tübingen**
* **#1 PIT [n] % Name, Rufname [Zusätzlich in runden Klammern:] sämtliche Vornamen incl. Varianten des Rufnamens [in runden Klammern: Geburts-, Todesjahr, z.B. 1733-1802**
* **#1\* Namensvarianten (kann mehrmals vorkommen)**
* **#1a Kurzcharakterisierung [Fach, Beruf, Funktion]** (Angaben zum Bearbeitungsstand wie `^#1c`. (Aufgliederung von `^#1a` (Kurzvita) in `#1a-d Okt. 2004)`)
* **#1b Studium in Tübingen bis einschl. Promotion (jedoch: Ehrenpromotionen: `^#1c`).** (Angaben zum Bearbeitungsstand wie `^#1c`)
* **#1c Biogramme**
* Zusatzangabe zum Bearbeitungsstand bei `^#1a-c`
    * `{Bio0}`: Daten fehlen und müssen ergänzt werden
    * `{Bio1}`: Daten ungeprüft.
    * `{Bio2}`: Daten geprüft, weitere Bearbeitung/Recherche erforderlich.
    * `{Bio3}`: Daten geprüft: Angabe entfällt / ist nicht erforderlich.
    * `{Bio4}`: Daten nutzbar (Reduzierter Standard: Ehrensenatoren, Absolventen u.a. Personen, die nicht zum Lehrkörper gehören, Laufbahnen oder Laufbahnende außerhalb Tübingens etc.).
    * `{Bio5}`: Fertig (Standard: Jubiläumskalender / NS-Bibliographie)
* **#1d Würdigung, zusätzliche Hinweise (nur ausnahmsweise!!!)**
* **#2 Anfangs- und Endjahr der Tätigkeit in Tübingen / Zugehörigkeit zum Lehrkörper!** kann mehrfach auftauchen differenziert nach Fakultäten ODER kann auch mehrere semikolon-getrennte Einträge enthalten
* **#3 Fakultät;** kann mehrfach auftauchen ODER semikolon-getrennte Einträge enthalten. Fakultätennamen sind mit Zeiträumen angegeben die sich auf die Fakultät selbst beziehen.
* **#4 Disziplin, Lehrfach** komma- oder semikolon-getrennte Einträge
* **#5 Konfession**
* **#6 Geburtsdatum, -ort**
* **#7 Sterbedatum, -ort**
* **#7a Begräbnisdatum / -ort / Grabnummer**
* **#8 Name und Stand des Vaters** (bei mehreren Vornamen analog `^#1`)
* **#9 Name und Geburtsname der Mutter**
* **#10 Datum der Eheschließung – Name der Ehefrau**
* **#10a Kinder**
* **#11 Bildungsgang** semikolon-getrennte Einträge
* **#12 Berufslaufbahn** semikolon-getrennte Einträge
* **#13 Akademische Ämter, Ehrenämter [auch politische]** semikolon-getrennte Einträge
* **#14 Titel, Ehrendoktorate, Orden und andere Auszeichnungen** semikolon-getrennte Einträge
* **#15 Mitgliedschaft in Akademien und wissenschaftlichen Gesellschaften {auch in Parteien}** semikolon-getrennte Einträge
* **#15a Mitgliedschaft in studentischen Vereinigungen ({Verbindungen, Korporationen})**
* **#16 [Würdigung] den Datensatz gibt es nicht mehr.** Eingearbeitet in andere Datensätze. Siehe auch `#1d`.
* **#17b-d Archivalische Quellen:** Der erste Verweis wird eingeleitet mit: `*ao`, jeder weitere mit `*nz`, jeder wird mit Punkt abgeschlossen. Verweise auf Signaturen des UAT werden eingeleitet mit `**ao UAT"` bzw. `"**nz UAT"`. Laufzeiten werden mit Doppelpunkt an die Signaturangabe angefügt.
    * **#17a Den Datensatz gibt es nicht mehr.**
    * **#17b Den Datensatz gibt es nicht mehr.** Eingearbeitet in **#17c** oder **#17d.**
    * **#17c Personenbezogene Akten im UAT** (auch Nachlass im UAT)
    * **#17d Nachlässe in anderen Archiven**
* **#18-18a Literatur:** Der erste Verweis wird eingeleitet mit: `*ao`, jeder weitere mit `*nz`, jeder wird mit Punkt abgeschlossen.
* **#18 Literatur: Heyd, Bd. 2.**
* `#18 *ao Bib. = Personenbezogener Titel in Bib`
* **#18a Internet-Belege / Internet-Adressen**
* **#19 Bildnachweis**
* **#20 Bemerkungen**
* **#21 Bearbeiter:** Zweibuchstabige Abkürzung: z.B. `An`; `Em`; `JK=Ergänzt aufgrund der Jubiläumskartei des UAT`; `Kü=Ergänzt aufgrund der Angaben in Kürschners Gelehrtenkalender`, `Br`.
* **#23 Bib+ = einschlägiger Titel in der Bibliographie / Bib- = keine einschlägiger Titel in der Bibliographie**
* **#24 GND [n]** [Wenn mehr als eine Nummer, getrennt durch Semikolon]
* `##`



---

## $0 Auswahlparameter und sonstige Abkürzungen

* **#23 BIB / BIBNS :** `+` = eigener Personeneintrag in Bib bzw. `Bibns` `-` = kein Eintrag
* **#0 AB** Die Angaben wurden aus der Kartei Tübinger Absolventen übernommen. (Zwischen 8.5.1998 und 27.8.1998 von Herrn Heine eingelesen, Datenstruktur am 21.9.1998 von Wi überprüft und leicht korrigiert, aber nicht redigiert)
* **#0 TP75** Die Angaben wurden Ende 1997 aus dem 1975 erstellten Verzeichnis "Tübinger Professoren" von Wilfried Setzler (UAT S 101/5) ergänzt.
* **#0 ES** Ehrensenatoren
* **#0 G80+** Aufnahmen in die Liste der Professorengräber (Verstorbene bis 1980, grundsätzlich nur Ordinarien.
* **#0 G80++** Desgl., hervorgehobene Nennung (Rektoren, Nobelpreisträger, Pour le merite und wenige zusätzliche Ausnahmen)
* **#0 AB Absolventen**
* **#0 BN Bildnachweis.** Ergänzt nach S 19ff. Personenindex.
* **#0 BIA** Ergänzt nach "Fotos aus Attempto" (in der Kartei der
* **#18 BLNW:** Grüttner, Biographisches Lexikon
* **#18 DBE:** Deutsche Biographische Enzyklopädie
* **#18 DBI:** Deutscher Biographischer Index
* **#18 ZDN** Nachlaß wurde an die Zentraldatei der Nachlässe beim Bundesarchiv gemeldet. Gegebenenfalls lautet der Eintrag in `^#17`: "nicht in ZDN" (sofern Meldung nicht vorgesehen) bzw. "noch nicht in ZDN" (sofern Meldung noch vorzunehmen ist).
* **#0 FKZ2005** Anfrage Ev. AG für kirchliche Zeitgeschichte 2005
* **#0 G+** Wie vor, aufzunehmen bei künftiger Weiterführung der Gräberliste.
* **#0 G-** In Tübingen bestattet, jedoch nicht in Gräberliste aufzunehmen.
* **#0 GLP01-** Nicht in Liste "Grabstätten Tübinger Professoren" (Andreas Vogt und Katrin Weber, 27.11.01)
* **#0 GLSF** Gräberliste Stadtfriedhof
* **#0 GLSF?** Biografie recherchieren
* **#0 GRW** Greifswald
* **#0 HNSN+/-** Habilitationen 1933-1945 und zwar:
HNS033.n bzw. n=034.n Habilitationen "alter Ordnung" 1933-1934/35 (die Ziffer nach dem Punkt steht für den Monat)
* **HNS101ff:** Habilitationen nach den Reichshab.Ordnung 1935-1945 lt. "Liste der Habilitationen" in 117C/38, gegebenenfalls mit Zusatz "b" für dort fehlende Fälle (Vollständigkeit erstrebt!) [Zusatz "+/-": Dozentur ja/nein]
* **HNS201ff:** Habilitation 1933-1945 an anderer Universität, spätere Zuweisung bzw. Berufung nach Tübingen bis 1945 (nicht vollständig!)
* **HNS301ff.:** Habilitation 1933-1945, nach 1945 umhabilitiert bzw. berufen nach Tübingen (nicht vollständig!) nicht vollständig bzw. Vollständigkeit nicht angestrebt!)
* **#0 JH19** Aufnenmen in die Liste "Lehrkörper und andere Universitätsangehörige des 19. Jahrhunderts"
* **#0 JK2001+** `JK2001-` `JK2001?` Jubiläumskalender 2001 (Aufnahme, Nichtaufnahme, prüfen, noch zu bearbeiten) Markierungen für die Jubiläumskalender 2008 bis 2019: `JK*2008ff.` (für Bearbeitung en bloc)
* **#0 Kth20c** Kath.-Theol. Fak. ab 1945 (Juni 2008 zur Beantwortung einer Anfrage)
* **#0 LK** LK15, LK16 LK17 etc., LK-, LK? Mitglied des Lehrkörpers bzw. nicht Mitglied oder fraglich. Am 1.10.2003 wurden die vorhandenen Datensätze sämtlich mit LK ausgezeichnet.
* **#0 KN** Nekrolog Kürschner
* **#0 NDB** Ergänzt nach Neuer Deutscher Biographie Br. `*NDB =` wurde in Bib nachgetragen. (Dezember 08, Bisch)
* **#0 OEW** OEW19 OEW20 OEW-Literaturprojekt (vor 1800, ab 1800, ab 1900 geborene Schriftsteller)
* **#0 PA1** Ergänzt nach UAT 126
* **#0 Q** Ergänzt nach 139/373 - 378 Karteien).
* **#0 REP** Repetent
* **#0 REPW** Repetent Wilhelmstift
* **#0 Requiem** Auswahl für einen 2003 geplanten Gedenkgottesdienst der Kath.-theol. Fak.
* **#0 SP** Sonstige Personen
* **#0 UAT126a** Ergänzt nach UAT 126a
* **#0 UAT51** Ergänzt nach UAT 51
* **#0 UB** Universitätsbediensteter
* **#0 UV** Universitätsverwandter bzw. -bürger
* **#0 VLV** Ergänzt nach den Vorlesungsverzeichnissen SoSe 1927 - SoSe 1945
* **#0 WÜBI** Aufnahme in Württembergische Biographien (Auszeichnung mit - besagt nicht abschließend, daß dort nicht aufgenommen, sondern daß diese Person nicht auf der übersandten Prüfliste stand). 2003
