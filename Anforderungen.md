# 📋 Anforderungen – Übersicht

## 🗂️ Feature 1 - Bewertungssystem

| ID   | Frage                                                 | Antwort                                                           |
|:-----|:------------------------------------------------------|:------------------------------------------------------------------|
| F1   | Funktioniert das 5-Sterne-System (1 Stern Minimum)?   | Ja - 1 Stern möglich                                              |
| F1   | Funktioniert das 5-Sterne-System (5 Sterne Maximum)?  | Ja - 5 Sterne möglich                                             |
| F2   | Wer darf bewerten — alle Nutzer oder nur eingeloggte? | Nur eingeloggte Nutzer; Gäste haben keine Bewertungsoption        |
| F4   | Ist das Textfeld Pflicht oder optional?               | Optional - Bewertung nur mit Sternen (ohne Text) möglich          |
| F3   | Wird die Durchschnittsbewertung visuell angezeigt?    | Ja - als ausgefüllte Sterne auf Produktseite                      |
| F5   | Kann ein Nutzer dasselbe Produkt mehrfach bewerten?   | Nein - max. 1 Bewertung/Nutzer/Produkt                            |
| F6   | Gibt es eine maximale Zeichenanzahl für Feedback?     | Nicht in Anforderung spezifiziert - muss im Test ermittelt werden |

---

## 🗂️ Feature 2 - Altersverifikation

| ID   | Frage                                                          | Antwort                                   |
|:-----|:---------------------------------------------------------------|:------------------------------------------|
| F1   | Wird jemand mit 17J 364T korrekt abgelehnt (1 Tag vor 18)?     | Ja - Zugriff verweigert (tagesgenau)      |
| F1   | Wird jemand mit exakt 18 Jahren korrekt zugelassen?            | Ja - Store freigegeben                    |
| F2   | Erscheint das Modal beim ersten /store Aufruf?                 | Ja - vor Produktanzeige                   |
| F3   | Muss das Modal bei jedem Seitenaufruf erneut bestätigt werden? | Nein - innerhalb Session nicht erneut     |
| F6   | Wie lange bleibt die Verifikation gespeichert?                 | Nicht spezifiziert - im Test zu ermitteln |
| F4   | Wird Datumsformat (TT.MM.JJJJ) verlangt?                       | Ja - Modal zeigt Datumsfelder             |
| F5   | Was passiert bei ungültigem Datum (z.B. 31.02.)?               | Nicht spezifiziert - im Test zu ermitteln |

---

## 🗂️ Feature 3 - Versandkosten

| ID   | Frage                                                    | Antwort                                          |
|:-----|:---------------------------------------------------------|:-------------------------------------------------|
| F1   | Wird bei 19,99€ korrekt 5€ Versandkosten berechnet?      | Ja - 5€ Versandkosten                            |
| F1   | Wird bei exakt 20€ korrekt 0€ Versandkosten berechnet?   | Ja - 0€ Versandkosten                            |
| F1   | Wird bei >20€ korrekt 0€ Versandkosten berechnet?        | Ja - 0€ Versandkosten                            |
| F2   | Werden 5€ angezeigt UND korrekt zur Gesamtsumme addiert? | Ja - Anzeige '5€' + Gesamtsumme = Warenkorb + 5€ |
| F3   | Aktualisieren sich Versandkosten beim Hinzufügen (≥20€)? | Ja - automatisch 0€                              |
| F3   | Aktualisieren sich Versandkosten beim Entfernen (<20€)?  | NEIN - Bug! Reload nötig                         |
| F4   | Ist /checkout ohne Login zugänglich?                     | Nein - Weiterleitung /auth                       |

---

## 🗂️ Zusammenfassung

| Feature            | Kernverhalten                                                                | Grenzfälle identifiziert                                | Offene Punkte                                                |
|:-------------------|:-----------------------------------------------------------------------------|:--------------------------------------------------------|:-------------------------------------------------------------|
| Bewertungssystem   | 1-5 Sterne, optionales Textfeld, nur eingeloggte Nutzer, 1 Bewertung/Produkt | Gast, Mehrfachbewertung, Textlänge                      | Zeichenlimit, Rundungsregel, Block vs. Update                |
| Altersverifikation | Geburtsdatum-Modal auf /store, 18+-Grenze, session-basiert                   | 17J 364T, exakt 18J (BVA), Session/Refresh, Tab-Wechsel | Session-Dauer, Cookie-Dauer, ungültiges Datum                |
| Versandkosten      | Freigrenze 20€, Versand 5€, Update nur unidirektional, Login erforderlich    | Wert 20€, 19,99€, 20,01€, leerer Warenkorb, Gast        | Versandkosten-Update nur unidirektional (Bug? Mit PO klären) |

---

