# Calendar Perso — Grist Custom Calendar Widget (Weekdays + Business Hours)

**Calendar Perso** is a customized Grist Calendar widget used in our applications via a **Widget URL**.
It provides a cleaner scheduling view by:
- **hiding weekends (Saturday/Sunday)**
- **restricting visible hours** (ex: 07:00 → 19:00)

Hosted as a static page (GitHub Pages) and embedded directly into Grist.

---

## ✅ What it does

- Week view focused on working days (Mon–Fri)
- Optional “business hours only” display
- Reads events directly from a Grist table using the Custom Widget integration

---

## ▶️ Run it in Grist (using the Widget URL)

1) Open your Grist document  
2) Create or open a table/view (ex: `RESERVATIONS`)  
3) Click **Add New** → **New Widget** → **Custom**  
4) Select **URL personnalisée** and paste the widget URL:
   - `https://nicodioub.github.io/calendar-perso/` *(example)*

5) Set **Niveau d’accès** to:
   - **Accès complet au document** *(recommended if the widget needs to read live data)*

6) Map the columns in the right panel:
   - **Start date** → `Date debut`
   - **End date** → `Date fin` *(optional)*
   - **Title** → `Nom_salle`
   - **All day** → *(optional)*
   - **Type** → *(optional)*

Once configured, the calendar renders automatically in Grist.

---

## 🧱 Requirements (Grist table)

Your table should contain at least:
- a **start date/time** column
- a **title** column  
Optional:
- an **end date/time** column
- a **type/category** column
- an **all day** boolean column

---

## 🧑‍💻 Tech Stack

- HTML + CSS
- Vanilla JavaScript
- Static hosting (GitHub Pages)
- No build step required

---

## License

Choose one: MIT / Apache-2.0 / GPL-3.0
