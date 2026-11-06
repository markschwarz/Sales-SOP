# 03. GoHighLevel (GHL) Operational Setup & Tracking

To ensure total visibility and easy progress tracking across our 90-day sprint and future handover, GoHighLevel is configured as follows:

## 1. Granular Pipeline Stages (Visual Kanban)
Instead of a single "Open" column, opportunity cards move automatically through these stages:
* **Stage 1:** `New Inquiry / Uncontacted`
* **Stage 2:** `Touch 1 Sent`
* **Stage 3:** `Touch 2 Sent`
* **Stage 4:** `Touch 3 Sent`
* **Stage 5:** `Touch 4-5 Sent`
* **Stage 6:** `Touch 6-7 Sent (Final Push)`
* **Stage 7:** `Replied / Consultation Booked`

## 2. Automated Contact Tags
Workflows apply tags dynamically as touchpoints fire:
* `touch-1-sent` through `touch-7-sent`
* `7-touches-complete`
* `engaged` (automatically stops follow-up sequences when a reply or booking is received).

## 3. Contact Custom Fields
* `Follow-Up Step` (Number 0–7)
* `Last Touch Date` (Date)
* Pinned prominently to the top of the contact sidebar.

## 4. Smart Lists for Daily Action
* **Active Prospect Queue:** Pipeline Status = `Open` AND Follow-Up Step `< 7` AND Last Activity older than 3 days.
