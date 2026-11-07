# GoHighLevel Configuration Guide & API Setup

This document records the programmatic and manual GHL setup completed for the WellnessFi Sales SOP.

## 1. Pipeline Setup
* **Pipeline Name:** New Client Sales
* **Pipeline ID:** `OTObWNjjDgdB7cNUklFC`
* **Stages & Order:**
  1. `New Lead`
  2. `Discovery Booked`
  3. `No Show`
  4. `Discovery Completed` (Post-call starting point)
  5. `Touch 1-2 Sent`
  6. `Touch 3-4 Sent`
  7. `Touch 5-6 Sent`
  8. `Touch 7 (Final Push)`
  9. `Replied / Booked`
  10. `Closed Won`
  11. `Closed Lost`

## 2. Custom Field Setup
* **Field Name:** Follow-Up Step (Contact Field)
  * **Field ID:** `kXAW1iJzGseynQLTfX2L`
  * **Field Key:** `contact.followup_step`
  * **Data Type:** `NUMERICAL`
* **Field Name:** Sales Goal (Opportunity Field)
  * **Field ID:** `mGyy2gWgk9uEEV9AtmMN`
  * **Field Key:** `opportunity.sales_goal`
  * **Data Type:** `TEXT`
* **Field Name:** Follow-Up Notes (Opportunity Field)
  * **Field ID:** `VKxdVWBySFUQp04Xguc0`
  * **Field Key:** `opportunity.followup_notes`
  * **Data Type:** `LARGE_TEXT`
* **Location ID:** `3PhlgdBHBj8nLILjDYQR`

## 3. Workflow & Smart List Implementation Plan
* **Workflow Trigger:** Opportunity entered into `Discovery Completed` stage (post-consultation).
* **Action Steps:** 7-touch cadence with 3–5 day wait intervals, incrementing `contact.followup_step` and moving pipeline stages automatically.
* **Smart List Filter:** Pipeline = `New Client Sales` AND `Follow-Up Step` < 7 AND Last Activity > 3 days.
