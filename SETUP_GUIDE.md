# 🏥 Anjum Clinic Management System — Setup Guide
## Complete Working System v2.0

---

## 📁 FILES IN THIS FOLDER

| File | Purpose |
|------|---------|
| `Code.gs` | ALL backend — paste into Google Apps Script |
| `KYCForm.html` | Patient registration sidebar (inside Sheet) |
| `KYCSearch.html` | Patient search sidebar |
| `ApptForm.html` | Appointment booking sidebar |
| `ApptSchedule.html` | Today's schedule sidebar |
| `FinanceSale.html` | Record sale/invoice sidebar |
| `FinanceExpense.html` | Record expense sidebar |
| `FinanceSummary.html` | Finance summary sidebar |
| `Dashboard.html` | Live KPI dashboard sidebar |
| `index.html` | **Public patient registration form** (Vercel) |

---

## 🚀 STEP-BY-STEP SETUP (15 minutes)

### PART A — Google Sheet Setup

**Step 1: Create Spreadsheet**
- Go to sheets.google.com → New Blank Sheet
- Rename it: "Anjum Clinic Management System"

**Step 2: Open Apps Script**
- Extensions → Apps Script
- Delete the default `myFunction()` code

**Step 3: Paste Code**
- Copy EVERYTHING from `Code.gs`
- Paste into the editor
- Click Save (Ctrl+S)
- Name project: "Anjum Clinic System"

**Step 4: Create HTML Files**
- Click "+" → HTML → name it exactly:
  - `KYCForm` → paste KYCForm.html content
  - `KYCSearch` → paste KYCSearch.html content
  - `ApptForm` → paste ApptForm.html content
  - `ApptSchedule` → paste ApptSchedule.html content
  - `FinanceSale` → paste FinanceSale.html content
  - `FinanceExpense` → paste FinanceExpense.html content
  - `FinanceSummary` → paste FinanceSummary.html content
  - `Dashboard` → paste Dashboard.html content

**Step 5: Initialize System**
- Go back to your Google Sheet
- Refresh the page (F5)
- Click: 🏥 Clinic System → ✅ Initialize System
- Grant permissions when asked → Run again

**Step 6: Update Settings**
- Click "Settings" tab in your sheet
- Update: Clinic_Name, Phone_Number, Address, Admin_Email

---

### PART B — Deploy Web App (for external patient form)

**Step 7: Deploy as Web App**
- In Apps Script: Deploy → New deployment
- Type: Web app
- Execute as: Me
- Who has access: **Anyone**
- Click Deploy → Copy the Web App URL

**Step 8: Update index.html**
- Open `index.html`
- Find `apiUrl: "YOUR_WEB_APP_URL"`
- Replace with your Web App URL
- Update `whatsappNum` with clinic's WhatsApp

---

### PART C — Deploy Public Form on Vercel

**Step 9: GitHub**
```
1. Create new repo on github.com (can be Private)
2. Upload index.html → rename to index.html
3. Push to main branch
```

**Step 10: Vercel**
```
1. vercel.com → Add New Project → Import from GitHub
2. Select your repo
3. Framework: Other
4. Deploy → Get your link!
```

Your live link: `https://your-project.vercel.app`

---

## 🎯 WHAT THE COMPLETE SYSTEM DOES

### For Patients (Public Link on Vercel)
- Fill registration form → Data goes to Google Sheet
- Get Patient ID (ANJ-2026-0001)
- WhatsApp redirect to clinic

### For Clinic Staff (Inside Google Sheet)
**🏥 Clinic System Menu:**
- ➕ Register New Patient (KYC form)
- 🔍 Search / Edit Patient
- 📅 Today's Schedule
- ➕ Book Appointment (with conflict detection!)
- 🧾 Record Sale / Invoice
- 💸 Record Expense
- 📈 Finance Summary (P&L)
- 📊 Dashboard (live KPIs)

### Google Sheet Tabs (Auto-created):
- **Settings** — clinic config
- **KYC_Data** — all patients
- **Appointments** — schedule
- **Sales** — billing & invoices
- **Expenses** — cost tracking
- **Dashboard_Data** — KPI numbers
- **System_Log** — audit trail

---

## ⚙️ CUSTOMIZE PER CLIENT (B2B)

To deploy for a new client, just:
1. Make a copy of the Google Sheet (File → Make a copy)
2. Update Settings tab: Clinic_Name, Colors, Phone
3. Deploy new Web App → get new URL
4. Update index.html CONFIG → redeploy on Vercel
5. Done! New client live in 10 minutes.

---

## 📞 SUPPORT
System built by: Your Company Name
Contact: your@email.com

