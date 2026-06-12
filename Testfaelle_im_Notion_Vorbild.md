# Beispielaufgabe Testfallentwurf

Entwirf deine Testfälle auf Grundlage der folgenden Funktionen des Shopsystems.

Du musst sie nur entwerfen – die Testdurchführung erfolgt in einer späteren Phase.

Füge, falls zutreffend, das verwendete Testentwurfsverfahren hinzu.

---

## 1. Bewertungssystem

**Testentwurfsverfahren:** Grenzwertanalyse (BVA), Äquivalenzklassenbildung (EP), Anwendungsfalltest (Use Case Testing), Fehlerraten / Error Guessing

**Testfälle:**

1. **Grenzwertanalyse / Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass ein Nutzer eine 1-Stern-Bewertung für ein gekauftes Produkt abgeben kann.
   - **Voraussetzung:** Nutzer ist eingeloggt und hat das Produkt gekauft.
   - **Testschritte:**
     - Produktseite öffnen.
     - 1 Stern auswählen.
     - Speichern klicken.
   - **Erwartetes Ergebnis:** Bewertung wird mit 1 Stern gespeichert.

2. **Grenzwertanalyse / Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass ein Nutzer eine 5-Sterne-Bewertung für ein gekauftes Produkt abgeben kann.
   - **Voraussetzung:** Nutzer ist eingeloggt und hat das Produkt gekauft.
   - **Testschritte:**
     - Produktseite öffnen.
     - 5 Sterne auswählen.
     - Speichern klicken.
   - **Erwartetes Ergebnis:** Bewertung wird mit 5 Sternen gespeichert.

3. **Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass ein Gast keine Bewertung abgeben kann.
   - **Voraussetzung:** Nutzer ist nicht eingeloggt.
   - **Testschritte:**
     - Produktseite öffnen.
   - **Erwartetes Ergebnis:** Keine Bewertungsoption sichtbar.

4. **Fehlerraten / Error Guessing:**
   - **Testfall:** Verifizieren, dass ein Nutzer ein Produkt nicht mehrfach bewerten kann.
   - **Voraussetzung:** Nutzer ist eingeloggt, hat das Produkt gekauft und bereits bewertet.
   - **Testschritte:**
     - Produktseite öffnen.
     - Erneut Bewertung abgeben.
   - **Erwartetes Ergebnis:** Zweite Bewertung wird blockiert.

5. **Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass eine Bewertung ohne Textkommentar möglich ist.
   - **Voraussetzung:** Nutzer ist eingeloggt und hat das Produkt gekauft.
   - **Testschritte:**
     - Produktseite öffnen.
     - Sterne auswählen.
     - Kein Text eingeben.
     - Speichern.
   - **Erwartetes Ergebnis:** Bewertung wird ohne Text gespeichert.

6. **Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass ein Nutzer eine bestehende Bewertung bearbeiten kann.
   - **Voraussetzung:** Nutzer ist eingeloggt, hat das Produkt gekauft und bereits bewertet.
   - **Testschritte:**
     - Produktseite öffnen.
     - Bewertung bearbeiten.
     - Speichern.
   - **Erwartetes Ergebnis:** Bewertung wird aktualisiert.

7. **Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass ein Nutzer eine bestehende Bewertung löschen kann.
   - **Voraussetzung:** Nutzer ist eingeloggt, hat das Produkt gekauft und bereits bewertet.
   - **Testschritte:**
     - Produktseite öffnen.
     - Bewertung löschen.
   - **Erwartetes Ergebnis:** Bewertung wird entfernt.

---

## 2. Altersverifikation

**Testentwurfsverfahren:** Grenzwertanalyse (BVA), Äquivalenzklassenbildung (EP), Anwendungsfalltest (Use Case Testing), Fehlerraten / Error Guessing

**Testfälle:**

1. **Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass Nutzer unter 18 Jahren keinen Zugriff auf eingeschränkte Produkte erhalten.
   - **Voraussetzung:** Geburtsdatum liegt unter 18 Jahren.
   - **Testschritte:**
     - `/store` öffnen.
     - Geburtsdatum eingeben.
   - **Erwartetes Ergebnis:** Zugriff auf alkoholische Produkte wird verweigert.

2. **Grenzwertanalyse:**
   - **Testfall:** Verifizieren, dass ein Nutzer mit exakt 18 Jahren Zugriff erhält.
   - **Voraussetzung:** Geburtsdatum entspricht exakt 18 Jahren.
   - **Testschritte:**
     - `/store` öffnen.
     - Datum eingeben.
   - **Erwartetes Ergebnis:** Store wird angezeigt.

3. **Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass ein Nutzer über 18 Jahren vollen Zugriff erhält.
   - **Voraussetzung:** Geburtsdatum liegt über 18 Jahren.
   - **Testschritte:**
     - `/store` öffnen.
     - Datum eingeben.
   - **Erwartetes Ergebnis:** Voller Zugriff auf alle Produkte.

4. **Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass die Altersverifikation innerhalb der Session gespeichert wird.
   - **Voraussetzung:** Nutzer ist bereits verifiziert.
   - **Testschritte:**
     - Seite neu laden.
   - **Erwartetes Ergebnis:** Modal erscheint nicht erneut.

5. **Fehlerraten / Error Guessing:**
   - **Testfall:** Verifizieren, dass ungültige Datumsangaben abgelehnt werden.
   - **Voraussetzung:** Keine besondere Voraussetzung.
   - **Testschritte:**
     - Ungültiges Datum eingeben, z. B. `31.02.`.
   - **Erwartetes Ergebnis:** Fehlermeldung wird angezeigt.

6. **Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass Nutzer unter 18 Jahren weiterhin Zugriff auf nicht eingeschränkte Produkte haben.
   - **Voraussetzung:** Geburtsdatum liegt unter 18 Jahren.
   - **Testschritte:**
     - `/store` öffnen.
     - Datum eingeben.
   - **Erwartetes Ergebnis:** Zugriff auf nicht-alkoholische Produkte möglich.

---

## 3. Versandkosten

**Testentwurfsverfahren:** Grenzwertanalyse (BVA), Äquivalenzklassenbildung (EP), Anwendungsfalltest (Use Case Testing), Fehlerraten / Error Guessing

**Testfälle:**

1. **Grenzwertanalyse:**
   - **Testfall:** Verifizieren, dass Versandkosten von 5 € berechnet werden, wenn der Warenwert unter der Freigrenze liegt.
   - **Voraussetzung:** Warenkorb enthält Produkte im Wert von 19,99 €.
   - **Testschritte:**
     - Warenkorb öffnen.
   - **Erwartetes Ergebnis:** 5 € Versandkosten werden angezeigt.

2. **Grenzwertanalyse:**
   - **Testfall:** Verifizieren, dass keine Versandkosten anfallen, wenn der Warenwert der Freigrenze entspricht.
   - **Voraussetzung:** Warenkorb enthält Produkte im Wert von 20 €.
   - **Testschritte:**
     - Warenkorb öffnen.
   - **Erwartetes Ergebnis:** 0 € Versandkosten.

3. **Grenzwertanalyse / Äquivalenzklassenbildung:**
   - **Testfall:** Verifizieren, dass keine Versandkosten anfallen, wenn der Warenwert über der Freigrenze liegt.
   - **Voraussetzung:** Warenkorb enthält Produkte im Wert über 20 €.
   - **Testschritte:**
     - Warenkorb öffnen.
   - **Erwartetes Ergebnis:** 0 € Versandkosten.

4. **Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass Versandkosten korrekt angezeigt und berechnet werden.
   - **Voraussetzung:** Warenkorb enthält Produkte unter 20 €.
   - **Testschritte:**
     - Produkt hinzufügen.
     - Warenkorb öffnen.
   - **Erwartetes Ergebnis:** 5 € Versandkosten plus korrekte Gesamtsumme.

5. **Grenzwertanalyse / Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass Versandkosten automatisch aktualisiert werden, wenn der Warenwert über die Freigrenze steigt.
   - **Voraussetzung:** Warenkorb liegt unter 20 €, danach wird ein Produkt hinzugefügt.
   - **Testschritte:**
     - Produkt hinzufügen.
     - Schwelle überschreiten.
   - **Erwartetes Ergebnis:** Versandkosten werden automatisch auf 0 € gesetzt.

6. **Grenzwertanalyse / Anwendungsfalltest:**
   - **Testfall:** Verifizieren, dass Versandkosten aktualisiert werden, wenn der Warenwert unter die Freigrenze fällt.
   - **Voraussetzung:** Warenkorb liegt über 20 €, danach wird ein Produkt entfernt.
   - **Testschritte:**
     - Produkt entfernen.
   - **Erwartetes Ergebnis:** Versandkosten werden auf 5 € gesetzt.

7. **Anwendungsfalltest / Fehlerraten:**
   - **Testfall:** Verifizieren, dass der Checkout nur für eingeloggte Nutzer möglich ist.
   - **Voraussetzung:** Nutzer ist nicht eingeloggt, Warenkorb enthält Produkt.
   - **Testschritte:**
     - `/checkout` öffnen.
   - **Erwartetes Ergebnis:** Weiterleitung zur Login-Seite.
