# SeatTogether

> A cloud-hosted smart seat selection and sharing platform designed to reduce canteen crowding, optimize seat usage, and make sharing dining spaces effortless.

---

## Project Overview

SeatTogether addresses peak-hour canteen inefficiencies where seats remain empty because students hesitate or feel awkward asking strangers to join partially occupied tables. Built as a cloud application, SeatTogether provides real-time seat status visibility, seat-level selection, and interactive table control to promote a welcoming campus environment.

---

## Live Demo & Deployment

* **Hosted Platform:** [SeatTogether App](https://main.dv6pqdevifs28.amplifyapp.com) *(AWS Amplify)*
* **Source Repository:** [GitHub Repository](https://github.com/Vixtoe/SeatTogether)

---

## Key System Features

* **Real-Time Interactive Seat Map:** Displays visual layout across canteen zones with live seat status indicators (Available, Selected, Occupied, Closed).
* **Seat-Level Selection:** Allows users to pick precise seats prior to occupying them.
* **Table Access Control (Open / Closed):** Table hosts can configure permissions ("Open to Join" or "Closed") to prevent awkward interactions.
* **Multi-Zone Navigation:** Supports pan and zoom capabilities for multi-zone navigation across large dining areas.
* **User Table Dashboard:** Allows users to manage active sessions, check current seat details, and leave tables in real time.

---

## Cloud Infrastructure & Architecture

The application is deployed on a fully serverless, low-cost cloud architecture using AWS Amplify and Supabase:

```text
[ Users (Web Browser) ] 
          │
          ▼
 [ AWS Amplify Hosting ] ──(Auto Deploy)── [ GitHub Main Branch ]
          │
          ▼ (HTTPS)
 [ Supabase Backend ]
  ├── PostgreSQL Database (Seat, Table, User Status)
  └── Supabase API & Realtime Sync
