# NETACONSULT Micro GFO Generator — Showcase

A browser-side web application for technical preparation and formatting of annual financial reports for Bulgarian micro-enterprises.

This repository is a public showcase / case study of the project.  
It does not contain the full production source code, secrets, environment configuration, access-control logic or private accounting data.

Live application: https://gfo.netaconsult.bg

---

## Project context

The project was developed for the practical needs of a Bulgarian accounting office.

Annual financial report preparation for micro-enterprises often includes repetitive technical work:

- reading Balance and Profit & Loss data from NSI/GOD PDF files;
- checking whether the Balance is equal;
- preparing a shortened annual financial report;
- formatting the output for Print / Save as PDF;
- avoiding unnecessary handling or transfer of sensitive accounting data.

The application is designed to support this technical workflow.  
It does not replace professional accounting judgment.

---

## Scope

The application is intended only for:

**Annual financial reports of Bulgarian micro-enterprises.**

It is not designed as:

- a full financial reporting system;
- an official state tool;
- a replacement for an accountant;
- a generator for all categories of companies;
- a full GFO engine for small, medium or large enterprises.

The application supports technical preparation and formatting of a micro-enterprise report based on the applicable shortened format.

---

## Key features

- Browser-side processing
- Local PDF reading through PDF.js
- No PDF upload to the server
- No storage of company identifiers or accounting report data
- Balance validation before report generation
- Optional Profit & Loss report section
- HTML report generation for Print / Save as PDF
- Access flow with backend protection
- Privacy-by-design architecture

---

## Privacy model

The public web version follows a browser-side processing model.

PDF files selected by the user are read locally in the browser through PDF.js.

The backend does not receive, process or store:

- PDF files;
- company identifiers;
- company names;
- personal identifiers;
- Balance data;
- Profit & Loss data;
- generated annual financial reports;
- accounting report data.

The backend is used only for access and abuse protection.

---

## Backend responsibilities

The backend is intentionally limited.

It handles:

- magic link access;
- session verification;
- rate limits;
- Turnstile validation;
- honeypot protection;
- usage control;
- privacy-safe technical logging.

It does not handle accounting data.

---

## Frontend responsibilities

The browser-side application handles:

- local PDF selection;
- local PDF parsing through PDF.js;
- extraction of Balance and Profit & Loss values;
- manual completion of missing report data;
- Balance validation;
- report rendering;
- Print / Save as PDF output.

The accounting data remains in the browser during the user session.

---

## Technologies and concepts

The project combines:

- Python / Flask backend
- HTML, CSS and JavaScript frontend
- PDF.js for browser-side PDF processing
- Cloudflare Turnstile
- SMTP magic link access
- Privacy-safe logging
- Rate limiting
- Accounting validation rules
- AI-assisted development workflow

---

## Accounting validation focus

The application performs technical validation of the Balance.

If the Balance does not match, report generation is blocked.

The purpose of this control is to prevent generation of a report with an unequal Balance.

This validation does not replace professional accounting review.

---

## Production status

The public production version is deployed at:

https://gfo.netaconsult.bg

Current confirmed production characteristics:

- browser-side PDF processing;
- production access flow;
- SMTP magic link;
- Turnstile protection;
- rate limits;
- Balance and Profit & Loss PDF processing;
- Print / Save as PDF output;
- feedback text with privacy guidance;
- no backend storage of accounting report data.

---

## AI-assisted development note

This project was developed with AI-assisted support.

ChatGPT was used as a development assistant for:

- planning;
- code review;
- debugging;
- refactoring ideas;
- documentation drafts;
- deployment reasoning;
- wording of user-facing explanations.

The accounting logic, reporting requirements, validation rules, privacy model and production testing were defined and controlled by Netaconsult.

---

## What I learned

This project was part of a practical learning-to-production path combining accounting expertise with software development.

Main learning areas:

- turning a real accounting workflow into a web application;
- separating frontend and backend responsibilities;
- designing a privacy-by-design architecture;
- using Flask for controlled access flow;
- working with PDF.js in the browser;
- validating accounting data before report generation;
- preparing a production-like deployment;
- documenting a real business automation project.

---

## Screenshots

Screenshots may be added later.

Only sanitized screenshots will be used.  
No real PDF files, company identifiers, personal identifiers or accounting data will be published in this repository.

---

## Rights and usage notice

This repository is published as a professional showcase and case study.

The production application, domain-specific logic, accounting workflow structure, text content, interface design and implementation details are part of Netaconsult's professional know-how.

No permission is granted to copy, reproduce, reverse engineer or use the project logic, structure, texts or design for creating a competing service.

For questions or professional feedback:

gfo@netaconsult.bg
