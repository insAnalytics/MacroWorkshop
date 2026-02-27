# 📬 Exercise: Daily Invoice Mailer

## The Story

Every morning, the accounts team at HPCL needs to receive the day's invoice by email.
Right now, someone does this manually — they open the Invoices folder, find the right file,
attach it to an email, and hit send.

If they're busy, they forget. If they're on leave, it doesn't go out.

**Your job: build the bot that makes sure it always goes out.**

---

## What You Will Build

A UiPath automation that:
1. Gets today's date and formats it into a filename
2. Looks inside the `Invoices/` folder for a file matching that name
3. If no file is found — logs a clear message and stops gracefully
4. If the file is found — sends it as an email attachment to the accounts team

---

## Folder Structure

```
InvoiceMailer/
├── Invoices/                        ← Sample invoice PDFs live here
│   ├── Invoice_2026-02-25.pdf
│   ├── Invoice_2026-02-26.pdf
│   └── Invoice_2026-02-27.pdf
├── project/
│   └── InvoiceMailer.xaml           ← This is the file you will work in
└── README.md                        ← You are here
```

---

## Before You Start

1. Open **UiPath Studio**
2. Create a new **Process** project called `InvoiceMailer`
3. Copy `InvoiceMailer.xaml` into your project folder, replacing the default `Main.xaml`  
   *(or rename it to `Main.xaml`)*
4. Open it in Studio — you will see the workflow with comment blocks inside
5. Make sure you have **Microsoft Outlook** open and logged in on your machine

---

## How To Work Through It

The workflow is divided into labelled sections. Each section has:
- A **Comment activity** explaining what needs to happen
- An **empty space** directly below it — that is where you drag your activity

**Read the comment. Find the activity in the Activities panel. Drag it in. Configure it.**

Do not skip ahead. Each step uses something from the step before it.

---

## Invoice Naming Convention

Files in the `Invoices/` folder follow this exact pattern:

```
Invoice_YYYY-MM-DD.pdf
```

Examples:
```
Invoice_2026-02-25.pdf
Invoice_2026-02-26.pdf
Invoice_2026-02-27.pdf
```

Your bot will construct this filename automatically from today's date.

---

## Email Details

| Field | Value |
|---|---|
| **To** | accounts@hpcl.in *(or use your own email for testing)* |
| **Subject** | Daily Invoice — [today's date] |
| **Body** | Please find attached today's invoice. |
| **Attachment** | The matched invoice PDF |

---

## Concepts You Will Use

| Concept | Slide Reference |
|---|---|
| Variables & Data Types | Slide 15 |
| Sequences & Workflows | Slide 12 |
| File Activities | Slide 22 |
| If / Else (Flow Control) | Slide 17 |
| Exception Handling | Slide 19 |
| Send Email | Slides 28–30 |

---

## Stuck?

- Re-read the comment block carefully — it tells you exactly which activity to use
- Check the **Activities panel** (Ctrl+F to search by name)
- Check the **Properties panel** on the right after dropping the activity — that is where you fill in the values
- Every variable you need is already declared in the **Variables panel** at the bottom — you do not need to create any new ones

---

*Built for the HPCL RPA Training Programme — insAnalytics*
