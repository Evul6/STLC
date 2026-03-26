# 🧪 Testfälle

## ⭐ Bewertungssystem

### TC-01: Bewertung als eingeloggter Nutzer
- **Voraussetzung:** Nutzer ist eingeloggt
- **Schritte:**
  1. Produkt öffnen
  2. Bewertung abgeben (z.B. 4 Sterne + Text)
- **Erwartet:** Bewertung wird gespeichert und angezeigt

---

### TC-02: Bewertung als Gast
- **Voraussetzung:** Nutzer ist nicht eingeloggt
- **Schritte:**
  1. Produkt öffnen
  2. Bewertung abgeben wollen
- **Erwartet:** Hinweis zum Login

---

## 🔞 Altersverifikation

### TC-03: Volljähriger Nutzer
- **Eingabe:** Alter ≥ 18
- **Erwartet:** Zugriff erlaubt

---

### TC-04: Minderjähriger Nutzer
- **Eingabe:** Alter < 18
- **Erwartet:** Zugriff verweigert

---

## 🚚 Versandkosten

### TC-05: Warenwert unter 20 €
- **Eingabe:** 15 €
- **Erwartet:** Versandkosten = 5 €

---

### TC-06: Warenwert über 20 €
- **Eingabe:** 25 €
- **Erwartet:** Versandkosten = 0 €
