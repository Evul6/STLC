# 📋 Anforderungen – Überarbeitete Version

## 🗂️ Feature 1 – Bewertungssystem

| ID   | Requirement / Frage (Testbasis) |
|:-----|:-------------------------------|
| R1   | Das System muss ein Bewertungssystem von 1 bis 5 Sternen unterstützen. |
| R2   | Es muss definiert werden, ob nur eingeloggte Nutzer bewerten dürfen. |
| R3   | Das System muss festlegen, ob ein Textkommentar optional oder verpflichtend ist. |
| R4   | Es muss definiert werden, wie die Durchschnittsbewertung berechnet und angezeigt wird (Rundung, Darstellung). |
| R5   | Das System muss sicherstellen, dass ein Nutzer ein Produkt maximal einmal bewerten darf. |
| R6   | Es muss definiert werden, ob ein Nutzer seine Bewertung bearbeiten oder löschen kann. |
| R7   | Es muss eine maximale Zeichenanzahl für Kommentare definiert werden. |
| R8   | Jeder Bewertungseintrag benötigt eine eindeutige ID (RatingID). |


Details: Nur eingeloggte Nutzer, die ein Produkt gekauft haben können eine Produktbewertung abgeben. Pro Nutzer ist eine Bewertung pro Produkt erlaubt; eine erneute Abgabe überschreibt die vorherige. Die Bewertung erfolgt durch Auswahl von 1 bis 5 Sternen, wobei die Sternauswahl ein Pflichtfeld ist. Das schriftliche Feedback ist optional und auf maximal 500 Zeichen begrenzt. Das System zeigt bei Überschreitung des Zeichenlimits eine Fehlermeldung an und verhindert das Speichern. Die angezeigte Durchschnittsbewertung auf der Produktkarte wird als arithmetisches Mittel aller abgegebenen Bewertungen berechnet und auf eine Nachkommastelle gerundet.

---

## 🗂️ Feature 2 – Altersverifikation

| ID   | Requirement / Frage (Testbasis) |
|:-----|:-------------------------------|
| R9   | Das System muss Nutzer unter 18 Jahren den Zugriff verweigern. |
| R10  | Es muss definiert werden, wie das Geburtsdatum validiert wird (Format, ungültige Daten). |
| R11  | Das System muss festlegen, wann das Verifikationsmodal angezeigt wird. |
| R12  | Es muss definiert werden, wie lange die Verifikation gespeichert bleibt (Session, Cookie). |
| R13  | Das System muss klar definieren, ob die Prüfung tagesgenau erfolgt. |
| R14  | Jeder Verifikationsprozess benötigt eine eindeutige Session-/User-ID-Zuordnung. |

Details: Nur eingeloggte Nutzer, die ein Produkt gekauft haben können eine Produktbewertung abgeben. Pro Nutzer ist eine Bewertung pro Produkt erlaubt; eine erneute Abgabe überschreibt die vorherige. Die Bewertung erfolgt durch Auswahl von 1 bis 5 Sternen, wobei die Sternauswahl ein Pflichtfeld ist. Das schriftliche Feedback ist optional und auf maximal 500 Zeichen begrenzt. Das System zeigt bei Überschreitung des Zeichenlimits eine Fehlermeldung an und verhindert das Speichern. Die angezeigte Durchschnittsbewertung auf der Produktkarte wird als arithmetisches Mittel aller abgegebenen Bewertungen berechnet und auf eine Nachkommastelle gerundet.

---

## 🗂️ Feature 3 – Versandkosten

| ID   | Requirement / Frage (Testbasis) |
|:-----|:-------------------------------|
| R15  | Das System muss Versandkosten abhängig vom Warenwert berechnen. |
| R16  | Es muss eine klare Freigrenze (z. B. 20€) definiert werden. |
| R17  | Versandkosten müssen automatisch bei Änderungen im Warenkorb aktualisiert werden. |
| R18  | Versandkosten müssen sowohl korrekt angezeigt als auch berechnet werden. |
| R19  | Es muss definiert werden, ob Checkout Login voraussetzt. |
| R20  | Jeder Warenkorb benötigt eine eindeutige Cart-ID. |

Details: Ab einem Produktsubtotal von genau €20,00 oder mehr ist der Versand kostenlos. Liegt der Subtotal unter €20,00, werden Versandkosten in Höhe von €5,00 erhoben. Der Schwellenwert bezieht sich auf den Subtotal nach Abzug etwaiger Rabatte oder Gutscheincodes. Die Versandkostenanzeige im Warenkorb und im Checkout aktualisiert sich dynamisch, sobald der Subtotal den Schwellenwert über- oder unterschreitet – ohne Seitenneuladung. Bei einem Subtotal von genau €20,00 entfallen die Versandkosten (inklusiver Grenzwert).
