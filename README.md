# 🚗 WhatNext Vision Motors: Shaping the Future of Mobility with Innovation and Excellence

## 📌 Project Overview

**WhatNext Vision Motors** is a Salesforce CRM-based project designed to modernize and automate the vehicle ordering and customer management process.

The system improves operational efficiency by automating vehicle stock validation, order processing, dealer management, and test-drive reminders.

The project uses **Salesforce Custom Objects, Lightning App, Record-Triggered Flow, Apex Triggers, Apex Classes, Batch Apex, and Scheduled Apex** to create an integrated CRM solution.

---

## 🎯 Objectives

- Manage vehicle and dealer information efficiently.
- Manage customer and vehicle order details.
- Prevent orders when vehicles are out of stock.
- Automatically update vehicle stock after confirmed orders.
- Process pending orders when new stock becomes available.
- Send automated reminders for scheduled test drives.
- Reduce manual work through Salesforce automation.
- Improve customer experience and operational efficiency.

---

## 🏗️ Project Architecture

```text
                    ┌─────────────────────┐
                    │      Customer       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Vehicle Order     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Apex Trigger      │
                    │ Stock Validation    │
                    └──────────┬──────────┘
                               │
                     ┌─────────┴─────────┐
                     ▼                   ▼
              Stock Available      Out of Stock
                     │                   │
                     ▼                   ▼
                Confirmed             Pending
                     │                   │
                     ▼                   │
              Update Stock              │
                                         │
                              ┌──────────▼─────────┐
                              │    Batch Apex      │
                              │ Pending Orders     │
                              └──────────┬─────────┘
                                         │
                                         ▼
                                    Confirm Order
