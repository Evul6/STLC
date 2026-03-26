# 🧪 Testplan & Testfallentwurf

## 1. 🎯 Zielsetzung (Testziele)

Sicherstellung, dass die neuen Funktionen **Bewertungssystem**, **Altersverifikation** und **Versandkosten** korrekt funktionieren.  
Validierung der Geschäftsregeln sowie Identifikation von Fehlern und Grenzfällen.

---

## 2. 👥 Nutzerbasis (Zielgruppen)

- 🔐 Eingeloggte Nutzer
- 👤 Gäste (nicht eingeloggt)
- 🧒 Minderjährige Nutzer
- 🧑 Volljährige Nutzer

---

## 3. ⚙️ Produktfunktionen

### ⭐ Bewertungssystem
- 1–5 Sterne
- Optionaler Text
- Nur für eingeloggte Nutzer

### 🔞 Altersverifikation
- 18+ Prüfung via Modal

### 🚚 Versandkosten
- 5 € unter 20 €
- Kostenlos ab 20 €

---

## 4. 📦 Testumfang (Scope)

### ✅ Im Scope
- Funktionale Tests der neuen Features
- UI- und Backend-Validierung

### ❌ Out of Scope
- Zahlungsabwicklung
- Performance- und Sicherheitstests

---

## 5. 🧩 Testarten

- Funktionale Tests
- UI-Tests
- Regressionstests
- Negative Tests

---

## 6. 🤖 Automatisierung

### Automatisiert
- Altersverifikation (klar definierte Logik)
- Versandkostenberechnung (regelbasiert)

### Manuell
- UI/UX Bewertungssystem
