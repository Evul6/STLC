# 📋 Testfälle – Überarbeitete Version (Deutsch)

## 🗂️ Bewertungssystem

| Testfall-ID | Beschreibung | Voraussetzung | Testschritte | Erwartetes Ergebnis |
|:------------|:-------------|:--------------|:-------------|:--------------------|
| TC-01 | Verifizieren, dass ein Nutzer eine 1-Stern-Bewertung für ein gekauftes Produkt abgeben kann | Nutzer ist eingeloggt und hat das Produkt gekauft | 1. Produktseite öffnen<br>2. 1 Stern auswählen<br>3. Speichern klicken | Bewertung wird mit 1 Stern gespeichert |
| TC-02 | Verifizieren, dass ein Nutzer eine 5-Sterne-Bewertung für ein gekauftes Produkt abgeben kann | Nutzer ist eingeloggt und hat das Produkt gekauft | 1. Produktseite öffnen<br>2. 5 Sterne auswählen<br>3. Speichern klicken | Bewertung wird mit 5 Sternen gespeichert |
| TC-03 | Verifizieren, dass ein Gast keine Bewertung abgeben kann | Nutzer ist nicht eingeloggt | 1. Produktseite öffnen | Keine Bewertungsoption sichtbar |
| TC-04 | Verifizieren, dass ein Nutzer ein Produkt nicht mehrfach bewerten kann | Nutzer ist eingeloggt, hat Produkt gekauft und bereits bewertet | 1. Produktseite öffnen<br>2. Erneut Bewertung abgeben | Zweite Bewertung wird blockiert |
| TC-05 | Verifizieren, dass eine Bewertung ohne Textkommentar möglich ist | Nutzer ist eingeloggt und hat das Produkt gekauft | 1. Produktseite öffnen<br>2. Sterne auswählen<br>3. Kein Text eingeben<br>4. Speichern | Bewertung wird ohne Text gespeichert |
| TC-06 | Verifizieren, dass ein Nutzer eine bestehende Bewertung bearbeiten kann | Nutzer ist eingeloggt, hat Produkt gekauft und bereits bewertet | 1. Produktseite öffnen<br>2. Bewertung bearbeiten<br>3. Speichern | Bewertung wird aktualisiert |
| TC-07 | Verifizieren, dass ein Nutzer eine bestehende Bewertung löschen kann | Nutzer ist eingeloggt, hat Produkt gekauft und bereits bewertet | 1. Produktseite öffnen<br>2. Bewertung löschen | Bewertung wird entfernt |

---

## 🗂️ Altersverifikation

| Testfall-ID | Beschreibung | Voraussetzung | Testschritte | Erwartetes Ergebnis |
|:------------|:-------------|:--------------|:-------------|:--------------------|
| TC-08 | Verifizieren, dass Nutzer unter 18 Jahren keinen Zugriff auf eingeschränkte Produkte erhalten | Geburtsdatum < 18 Jahre | 1. /store öffnen<br>2. Geburtsdatum eingeben | Zugriff auf alkoholische Produkte wird verweigert |
| TC-09 | Verifizieren, dass ein Nutzer mit exakt 18 Jahren Zugriff erhält | Geburtsdatum = 18 Jahre | 1. /store öffnen<br>2. Datum eingeben | Store wird angezeigt |
| TC-10 | Verifizieren, dass ein Nutzer über 18 Jahren vollen Zugriff erhält | Geburtsdatum > 18 Jahre | 1. /store öffnen<br>2. Datum eingeben | Voller Zugriff auf alle Produkte |
| TC-11 | Verifizieren, dass die Altersverifikation innerhalb der Session gespeichert wird | Nutzer bereits verifiziert | 1. Seite neu laden | Modal erscheint nicht erneut |
| TC-12 | Verifizieren, dass ungültige Datumsangaben abgelehnt werden | Keine | 1. Ungültiges Datum eingeben (z. B. 31.02.) | Fehlermeldung wird angezeigt |
| TC-13 | Verifizieren, dass Nutzer unter 18 Jahren weiterhin Zugriff auf nicht eingeschränkte Produkte haben | Geburtsdatum < 18 Jahre | 1. /store öffnen<br>2. Datum eingeben | Zugriff auf nicht-alkoholische Produkte möglich |

---

## 🗂️ Versandkosten

| Testfall-ID | Beschreibung | Voraussetzung | Testschritte | Erwartetes Ergebnis |
|:------------|:-------------|:--------------|:-------------|:--------------------|
| TC-14 | Verifizieren, dass Versandkosten von 5€ berechnet werden, wenn der Warenwert unter der Freigrenze liegt | Warenkorb enthält Produkte im Wert von 19,99€ | 1. Warenkorb öffnen | 5€ Versandkosten werden angezeigt |
| TC-15 | Verifizieren, dass keine Versandkosten anfallen, wenn der Warenwert der Freigrenze entspricht | Warenkorb enthält Produkte im Wert von 20€ | 1. Warenkorb öffnen | 0€ Versandkosten |
| TC-16 | Verifizieren, dass keine Versandkosten anfallen, wenn der Warenwert über der Freigrenze liegt | Warenkorb enthält Produkte im Wert über 20€ | 1. Warenkorb öffnen | 0€ Versandkosten |
| TC-17 | Verifizieren, dass Versandkosten korrekt angezeigt und berechnet werden | Warenkorb enthält Produkte unter 20€ | 1. Produkt hinzufügen<br>2. Warenkorb öffnen | 5€ Versandkosten + korrekte Gesamtsumme |
| TC-18 | Verifizieren, dass Versandkosten automatisch aktualisiert werden, wenn der Warenwert über die Freigrenze steigt | Warenkorb < 20€, danach Produkt hinzufügen | 1. Produkt hinzufügen<br>2. Schwelle überschreiten | Versandkosten werden automatisch auf 0€ gesetzt |
| TC-19 | Verifizieren, dass Versandkosten aktualisiert werden, wenn der Warenwert unter die Freigrenze fällt | Warenkorb > 20€, danach Produkt entfernen | 1. Produkt entfernen | Versandkosten werden auf 5€ gesetzt |
| TC-20 | Verifizieren, dass der Checkout nur für eingeloggte Nutzer möglich ist | Nutzer nicht eingeloggt, Warenkorb enthält Produkt | 1. /checkout öffnen | Weiterleitung zur Login-Seite |
