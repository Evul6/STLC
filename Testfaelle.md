# Testfälle (vollständig)

| Testfall-ID   | Feature            | Testtyp    | Testdesign-Technik   | Beschreibung                             | Voraussetzung             | Testschritte                                 | Erwartetes Ergebnis                      |
|:--------------|:-------------------|:-----------|:---------------------|:-----------------------------------------|:--------------------------|:---------------------------------------------|:-----------------------------------------|
| TC-01         | Bewertungssystem   | UI         | Boundary Value       | 1 Stern Bewertung möglich                | User eingeloggt           | Produkt öffnen → 1 Stern wählen → speichern  | Bewertung wird mit 1 Stern gespeichert   |
| TC-02         | Bewertungssystem   | UI         | Boundary Value       | 5 Sterne Bewertung möglich               | User eingeloggt           | Produkt öffnen → 5 Sterne wählen → speichern | Bewertung wird mit 5 Sternen gespeichert |
| TC-03         | Bewertungssystem   | UI         | Equivalence Class    | Gast kann nicht bewerten                 | Nicht eingeloggt          | Produkt öffnen                               | Keine Bewertungsoption sichtbar          |
| TC-04         | Bewertungssystem   | Backend/UI | Business Rule        | Mehrfachbewertung verhindern             | User hat bereits bewertet | Erneut bewerten versuchen                    | Bewertung wird blockiert                 |
| TC-05         | Bewertungssystem   | UI         | Equivalence Class    | Bewertung ohne Text möglich              | User eingeloggt           | Nur Sterne auswählen → speichern             | Bewertung wird ohne Text gespeichert     |
| TC-06         | Altersverifikation | UI         | Boundary Value       | User 17J 364T wird abgelehnt             | Geburtsdatum 17J 364T     | /store öffnen → Datum eingeben               | Zugriff verweigert                       |
| TC-07         | Altersverifikation | UI         | Boundary Value       | User exakt 18 Jahre wird zugelassen      | Geburtsdatum genau 18     | /store öffnen → Datum eingeben               | Store wird angezeigt                     |
| TC-08         | Altersverifikation | UI         | Equivalence Class    | Session merkt Verifikation               | User bereits verifiziert  | Seite neu laden                              | Modal erscheint nicht erneut             |
| TC-09         | Altersverifikation | UI         | Negative Test        | Ungültiges Datum wird abgefangen         | -                         | 31.02 eingeben                               | Fehlermeldung wird angezeigt             |
| TC-10         | Versandkosten      | Backend    | Boundary Value       | Versandkosten bei 19,99€                 | Warenkorb 19,99€          | Produkt hinzufügen                           | 5€ Versandkosten                         |
| TC-11         | Versandkosten      | Backend    | Boundary Value       | Versandkosten bei 20€                    | Warenkorb 20€             | Produkt hinzufügen                           | 0€ Versandkosten                         |
| TC-12         | Versandkosten      | Backend    | Boundary Value       | Versandkosten bei >20€                   | Warenkorb 20,01€          | Produkt hinzufügen                           | 0€ Versandkosten                         |
| TC-13         | Versandkosten      | UI         | Business Rule        | Anzeige + Berechnung korrekt             | Warenkorb <20€            | Produkt hinzufügen                           | Anzeige 5€ + Gesamtsumme korrekt         |
| TC-14         | Versandkosten      | UI         | Dynamic Update       | Update beim Hinzufügen                   | Warenkorb steigt über 20€ | Produkt hinzufügen                           | Versandkosten werden automatisch 0€      |
| TC-15         | Versandkosten      | UI         | Bug Case             | Update beim Entfernen funktioniert nicht | Warenkorb >20€            | Produkt entfernen <20€                       | Versand bleibt falsch → Bug              |
| TC-16         | Versandkosten      | UI         | Access Control       | Checkout nur mit Login                   | Nicht eingeloggt          | /checkout öffnen                             | Weiterleitung zu /auth                   |

---

