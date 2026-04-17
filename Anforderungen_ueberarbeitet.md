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
