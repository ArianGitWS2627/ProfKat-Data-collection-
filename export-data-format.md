
# Datenformat für den Export der ProfKatalog-Daten

Im Folgenden wird das Datenformat beschrieben, in dem die ProfKatalog-Daten nach der Aufarbeitung exportiert werden sollen.


---

## Beispieldatensatz

### Originale Datenkodierung

```txt
##
#0 REK641 PK1 UAT55/131 jk2001+ JH19 LK19+ UAT51- OEW . #011 männlich  #012 UNIANG: Student #012 UNIANG: Lehrkörper (o. Prof)
#1 PIT 5 % Abel, Friedrich (1751-1829)
#1* PIT 5 % Abel, Jakob Friedrich (1751-1829)
#1a {Bio5} Ev. Theologe, Prof. an der Philosophischen Fakultät.
#1b {Bio5} 1768 imm., Bacc. art., 1770 Mag. art., 1770-1772 stud. theol.
#1c {BIB+} {Bio5} 1790 o. Prof. für Logik und Metaphysik, Beredsamkeit und Dichtkunst, 1798-1811 o. Prof. für Prakt. Philosophie und Dichtkunst, 1801/02 und 1808/09 Rektor der Universität. 1811 Prälat und Generalsuperintendent ((oÖhringen)) und Leiter des Seminars ((oSchöntal)). 1823 Generalsuperintendent ((oUrach)) und ((oReutlingen)).
#2 1790-1811
#3 (Alte) Philosophische Fakultät 1477-1969
#4 Logik und Metaphysik; Beredsamkeit und Dichtkunst; Praktische Philosophie
#5
#6 9.5.1751 ((oVaihingen/Enz))
#7 7.7.1829 ((oSchorndorf))
#8 Konradin Ludwig Abel, Oberamtmann
#9 Eva Regine Bojons
#10 a) 1786 Luise Wilhelmine Rosine, Tochter des Christian Gottlieb Schmid, Stadtschreiber ((oSchorndorf)); b) 1810 Friederike Beate, Tochter des Karl Heinrich Rieger, Stiftsprediger und Konsistorialrat ((oStuttgart)), Witwe des Gotthilf Köstlin, Diakon ((oEsslingen))
#11 Schule ((oVaihingen)), 1764-1768 Klosterschulen ((oDenkendorf)) und ((oMaulbronn)); 1768 Imm. ((oTübingen)) M̑UT 36715%), Bacc. art.; 1770 Mag. art.; 1770-1772 Studium der Theol.
#12 1772-1790 Prof. für Philos. an der Hohen Karlsschule ((oStuttgart)); 1790 o. Prof. für Logik und Metaphysik, zugleich auch der Beredsamkeit und Dichtkunst ((oTübingen)); 1798 o. Prof. für Prakt. Philos. und Dichtkunst; 1811 Prälat und Generalsuperintendent ((oÖhringen)) und Leiter des Seminars ((oSchöntal)); 1823 Generalsuperintendent ((oUrach)) und ((oReutlingen))
#13 1786-1790 Prorektor an der Hohen Karlsschule ((oStuttgart)); 1796/97, 1801/02 und 1808/09 Rektor der Universität ((oTübingen)); 1792-1802 Rektor der Burse; 1798-1811 Pädagogarch der Lat. Schulen ob der Steig; 1819 Mitglied der Kammer der Abgeordneten.
#14 1812 Zivilverdienstorden.
#17c *ao UAT 44/106 (1798). *nz UAT 51/1a (1808/09-1811). *nz UAT 55 bzw. UAT 131 (1812). *nz UAT 44/117,1 (1791-1796). *nz UAT 44/117,2 (1796-1802). *nz UAT 44/117,3 (1802-1806). *nz UAT 44/117,4 (1806-1808). *nz UAT 44/117,5 (1808-1810). *nz UAT 44/117,6 (1810-1811).
#17d *ao UBT Programmata.
#18 *ao Seck, S. 297. *nz NDB 1 (1953) S. 11. *nz Zeller, Bernhard: Jacob Friedrich Abel 1751-1829, in: Heimatbuch für Schorndorf und Umgebung 1964, S. 87-99. *nz Faber 25/369. *nz Tübinger Blätter 38 (1951), S. 38ff.
#19 *ao Zeller, aaO. *nz LB Stuttgart.
#21 An
#23 BIB+
##
```

### JSON-Datenformat

```json
{
  "(0) PK": "REK641 PK1 UAT55/131 jk2001+ JH19 LK19+ UAT51- OEW",
  "(011) Geschlecht": "männlich",
  "(012) Uni-Angehörigkeit": [ "Student", "Lehrkörper (o. Prof)" ],
  "(1) Name": {
    "PIT": "5",
    "Nachname": "Abel",
    "Vorname": "Friedrich",
    "Geburtsjahr": "1751",
    "Sterbejahr": "1829"
  },
  "(1*) Namensvarianten": [{
    "PIT": "5",
    "Nachname": "Abel",
    "Vorname": "Jakob Friedrich",
    "Geburtsjahr": "1751",
    "Sterbejahr": "1829"
  }],
  "(1a) Kurzcharakterisierung": "Ev. Theologe, Prof. an der Philosophischen Fakultät",
  "(1b) Studium-in-Tübingen": "1768 imm., Bacc. art., 1770 Mag. art., 1770-1772 stud. theol.",
  "(1c) Biogramme": "1790 o. Prof. für Logik und Metaphysik, Beredsamkeit und Dichtkunst, 1798-1811 o. Prof. für Prakt. Philosophie und Dichtkunst, 1801/02 und 1808/09 Rektor der Universität. 1811 Prälat und Generalsuperintendent ((oÖhringen)) und Leiter des Seminars ((oSchöntal)). 1823 Generalsuperintendent ((oUrach)) und ((oReutlingen))",
  "(2+3) Fakultätszugehörigkeit": [{
    "Anfangsjahr": "1790",
    "Endjahr": "1811",
    "Fakultät": "(Alte) Philosophische Fakultät 1477-1969"
  }],
  "(4) Lehrfach": [ "Logik und Metaphysik", "Beredsamkeit und Dichtkunst", "Praktische Philosophie" ],
  "(5) Konfession": "",
  "(6+7) Lebensdaten": {
    "Geburtsdatum": "9.5.1751",
    "Geburtsort": "Vaihingen/Enz",
    "Sterbedatum": "7.7.1829",
    "Sterbeort": "Schorndorf",
    "(7a) Begräbnisdaten": ""
  },
  "(8+9) Eltern": {
    "Vater": "Konradin Ludwig Abel, Oberamtmann",
    "Mutter": "Eva Regine Bojons"
  },
  "(10) Ehepartner": [
    {
      "Eheschließung": "1786",
      "Vorname": "Luise Wilhelmine Rosine",
      "Vater": "Christian Gottlieb Schmid, Stadtschreiber ((oSchorndorf))"
    },
    {
      "Eheschließung": "1810",
      "Vorname": "Friederike Beate",
      "Vater": "Karl Heinrich Rieger, Stiftsprediger und Konsistorialrat ((oStuttgart))",
      "Bemerkung": "Witwe des Gotthilf Köstlin, Diakon ((oEsslingen))"
    }
  ],
  "(10a) Kinder": [],
  "(11) Bildungsgang": [
    "Schule ((oVaihingen)), 1764-1768 Klosterschulen ((oDenkendorf)) und ((oMaulbronn))",
    "1768 Imm. ((oTübingen)) M̑UT 36715%), Bacc. art.",
    "1770 Mag. art.",
    "1770-1772 Studium der Theol."
  ],
  "(12) Berufslaufbahn": [
    "1772-1790 Prof. für Philos. an der Hohen Karlsschule ((oStuttgart))",
    "1790 o. Prof. für Logik und Metaphysik, zugleich auch der Beredsamkeit und Dichtkunst ((oTübingen))",
    "1798 o. Prof. für Prakt. Philos. und Dichtkunst",
    "1811 Prälat und Generalsuperintendent ((oÖhringen)) und Leiter des Seminars ((oSchöntal))",
    "1823 Generalsuperintendent ((oUrach)) und ((oReutlingen))"
  ],
  "(13) Akademische-Ämter": [
    "1786-1790 Prorektor an der Hohen Karlsschule ((oStuttgart))",
    "1796/97, 1801/02 und 1808/09 Rektor der Universität ((oTübingen))",
    "1792-1802 Rektor der Burse",
    "1798-1811 Pädagogarch der Lat. Schulen ob der Steig",
    "1819 Mitglied der Kammer der Abgeordneten"
  ],
  "(14) Titel": [ "1812 Zivilverdienstorden" ],
  "(15) Mitgliedschaft Wissenschaft": [],
  "(15a) Mitgliedschaft Studium": [],
  "(17) Archivalische-Quellen": {
    "UAT": [
        "UAT 44/106 (1798)",
        "UAT 51/1a (1808/09-1811)",
        "UAT 55 bzw. UAT 131 (1812)",
        "UAT 44/117,1 (1791-1796)",
        "UAT 44/117,2 (1796-1802)",
        "UAT 44/117,3 (1802-1806)",
        "UAT 44/117,4 (1806-1808)",
        "UAT 44/117,5 (1808-1810)",
        "UAT 44/117,6 (1810-1811)"
    ],
    "Andere": [ "UBT Programmata" ]
  },
  "(18) Literatur": [
    "Seck, S. 297",
    "NDB 1 (1953) S. 11",
    "Zeller, Bernhard: Jacob Friedrich Abel 1751-1829, in: Heimatbuch für Schorndorf und Umgebung 1964, S. 87-99",
    "Faber 25/369",
    "Tübinger Blätter 38 (1951), S. 38ff"
  ],
  "(18a) Online-Quellen": [],
  "(19) Bildnachweise": [ "Zeller, aaO", "LB Stuttgart" ],
  "(20) Bemerkungen": [],
  "(21) Bearbeiter": "An",
  "(23) BIB": "BIB+",
  "(24) GND": [],
}
```

----

# Konvertierungsanleitung

Diese folgende Anleitung beschreibt die strukturierte Transformation eines Rohdatensatzes im Textformat in das zielgerichtete JSON-Format.

---

## 1. Metadaten und Kennungen (`#0`, `#011`, `#012`)

* **Original:**
```txt
#0 REK641 PK1 UAT55/131 jk2001+ JH19 LK19+ UAT51- OEW . #011 männlich  #012 UNIANG: Student #012 UNIANG: Lehrkörper (o. Prof)

```


* **JSON-Konvertierung:**
  * **`"(0) PK"`:** Die vollständige Parameter- und Kennungskette wird nach Bereinigung von Trennzeichen (z. B. abschließenden Punkten) als einzelner String übernommen.
  * **`"(011) Geschlecht"`:** Der Wert hinter `#011` (z. B. `"männlich"`) wird direkt zugewiesen.
  * **`"(012) Uni-Angehörigkeit"`:** Mehrfach vorkommende `#012 UNIANG:`-Einträge werden extrahiert und als Array von Strings abgebildet (z. B. `["Student", "Lehrkörper (o. Prof)"]`).



---

## 2. Namen und Namensvarianten (`#1`, `#1*`)

* **Original:**
```txt
#1 PIT 5 % Abel, Friedrich (1751-1829)
#1* PIT 5 % Abel, Jakob Friedrich (1751-1829)

```


* **JSON-Konvertierung:** Textzeilen werden in strukturierte Objekte aufgeteilt:
  * `PIT`: Kennziffer nach `PIT` (z. B. `"5"`).
  * `Nachname`: Der Teil vor dem Komma (`"Abel"`).
  * `Vorname`: Der Teil nach dem Komma bis zur Klammer (`"Friedrich"` bzw. `"Jakob Friedrich"`).
  * `Geburtsjahr` / `Sterbejahr`: Die in runden Klammern angegebenen Jahreszahlen (`"1751"`, `"1829"`).
  * `#1*` wird analog als Array von Objekten unter `"(1*) Namensvarianten"` geführt.



---

## 3. Biografische Kurztexte und Studiennotizen (`#1a`, `#1b`, `#1c`)

* **Original:** Textzeilen, die oft mit Status-Tags wie `{Bio5}` oder `{BIB+}` beginnen.
* **JSON-Konvertierung:** Die Status-Tags werden für das reine Textfeld bereinigt. Der verbleibende Beschreibungstext wird als String zugewiesen:
  * `"(1a) Kurzcharakterisierung"`
  * `"(1b) Studium-in-Tübingen"`
  * `"(1c) Biogramme"`



---

## 4. Fakultätszugehörigkeit und Lehrfächer (`#2`, `#3`, `#4`)

* **Original:**
```txt
#2 1790-1811
#3 (Alte) Philosophische Fakultät 1477-1969
#4 Logik und Metaphysik; Beredsamkeit und Dichtkunst; Praktische Philosophie

```


* **JSON-Konvertierung:**
  * **Fakultäten (`#2` + `#3`):** Werden im kombinierten Objekt-Array `"(2+3) Fakultätszugehörigkeit"` zusammengeführt, aufgeteilt in `Anfangsjahr`, `Endjahr` und die vollständige Bezeichnung der `Fakultät`.
  * **Lehrfächer (`#4`):** Durch Semikolon getrennte Lehrfächer werden aufgespalten und als String-Array unter `"(4) Lehrfach"` gespeichert.



---

## 5. Konfession und Lebensdaten (`#5`, `#6`, `#7`, `#7a`)

* **Original:**
```txt
#5 
#6 9.5.1751 ((oVaihingen/Enz))
#7 7.7.1829 ((oSchorndorf))

```


* **JSON-Konvertierung:**
  * **`"(5) Konfession"`:** Bleibt bei Leerzeilen ein leerer String `""`.
  * **`"(6+7) Lebensdaten"`:** Datum und Ort werden getrennt. Interne Ortsmarkierungen (wie `((o...))`) werden bereinigt (`"Vaihingen/Enz"`, `"Schorndorf"`). Das Feld `"(7a) Begräbnisdaten"` ist standardmäßig als leerer String hinterlegt, sofern keine Daten vorliegen.



---

## 6. Eltern, Ehepartner und Kinder (`#8`, `#9`, `#10`, `#10a`)

* **Original:**
```txt
#8 Konradin Ludwig Abel, Oberamtmann
#9 Eva Regine Bojons
#10 a) 1786 Luise Wilhelmine Rosine... ; b) 1810 ...

```


* **JSON-Konvertierung:**
  * **Eltern (`#8`, `#9`):** Werden direkt als Strings den Attributen `Vater` und `Mutter` unter `"(8+9) Eltern"` zugewiesen.
  * **Ehepartner (`#10`):** Mehrere Eheschließungen (gekennzeichnet durch `a)`, `b)`) werden in ein Array von Objekten überführt. Jedes Objekt enthält Attribute wie `Eheschließung` (Jahr), `Vorname`, `Vater` und optional `Bemerkung` (z. B. für Witwenstatus).
  * **Kinder (`#10a`):** Wird als leeres Array `[]` (oder mit entsprechenden Einträgen) repräsentiert.



---

## 7. Bildungsgang, Berufslaufbahn, Ämter und Titel (`#11`, `#12`, `#13`, `#14`)

* **Original:** Textzeilen mit chronologischen Stationen, Titeln oder Auszeichnungen.
* **JSON-Konvertierung:** Die Einträge werden anhand von Satz- oder Strukturmarkern in saubere Arrays von Strings aufgeteilt:
  * `"(11) Bildungsgang"`
  * `"(12) Berufslaufbahn"`
  * `"(13) Akademische-Ämter"`
  * `"(14) Titel"` (z. B. Auszeichnungen wie *Zivilverdienstorden*)



---

## 8. Mitgliedschaften (`#15`, `#15a`)

* **JSON-Konvertierung:** Fällt in den Beispieldaten kein Eintrag an, werden die Felder als leere Arrays (`[]`) für wissenschaftliche (`"(15) Mitgliedschaft Wissenschaft"`) und studentische (`"(15a) Mitgliedschaft Studium"`) Vereinigungen ausgegeben.

---

## 9. Archivalische Quellen, Literatur und Nachweise (`#17` bis `#24`)

* **Original:**
```txt
#17c *ao UAT 44/106 (1798). *nz UAT 51/1a...
#18 *ao Seck, S. 297. *nz NDB 1 (1953)...
#19 *ao Zeller, aaO. *nz LB Stuttgart.
#21 An
#23 BIB+

```


* **JSON-Konvertierung:**
  * **Archivalische Quellen (`#17`):** Steuerzeichen wie `*ao` oder `*nz` werden entfernt. Die Signaturen werden nach Beständen gruppiert (z. B. `UAT` als String-Array, `Andere` für Bestände wie UBT Programmata).
  * **Literatur (`#18`) & Bildnachweise (`#19`):** Die durch Punkte getrennten Nachweise werden bereinigt (Entfernung von `*ao`/`*nz`) und als Arrays von Einzelliteraturen bzw. Nachweisen abgelegt. Online-Quellen (`#18a`), Bemerkungen (`#20`) und GND-Nummern (`#24`) werden als leere Arrays initialisiert, wenn keine Daten vorliegen.
  * **Bearbeiter (`#21`) & BIB-Status (`#23`):** Kürzel (z. B. `"An"`) und Flag-Status (z. B. `"BIB+"`) werden als direkte Strings übertragen.
