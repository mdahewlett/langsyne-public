# <img src="assets/app_icon.png" width="24" style="vertical-align: middle;" /> LangSyne — Remember Your Friends

A mobile app that helps you remember to reach out to the friends you don't see every day.

<p align="center">
  <a href="https://play.google.com/store/apps/details?id=app.langsyne">
    <img
      src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"
      width="230"
      alt="Get it on Google Play"
    />
  </a>
</p>

Developed by **Michael Hewlett**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/mdahewlett/) [![YouTube](https://img.shields.io/badge/YouTube-Channel-red?logo=youtube&logoColor=white)](https://www.youtube.com/@mochael)
[![Email](https://img.shields.io/badge/Email-Contact-red?logo=gmail&logoColor=white)](mailto:applangsyne@gmail.com)

## 🌎 Overview

**LangSyne** is an Android & iOS app (React-Native, Expo, TypeScript) with a custom backend (NestJS + Prisma + PostgreSQL on Neon) deployed on Google Cloud Run.

It helps users stay connected to friends across timezones, life stages, and friend groups through:

- Reminders (notification and in-app) when it’s time to reconnect
- Private notes for conversations and memories
- Contact import
- Fully offline storage
- Optional data backup & cloud sync  
- Fast, clean UI

> **Note:** This repository is a public overview for portfolio purposes. The full production codebase is private.
---

## 🕸️ Architecture

                       +------------------------------+
                       |            Clients           |
                       |------------------------------|
                       |  Mobile App (React Native)   |
                       |  Web Frontend (Vercel)       |
                       +---------------+--------------+
                                       |
                                       | HTTPS
                                       v
                  +-----------------------------------------+
                  |            Backend Service              |
                  |-----------------------------------------|
                  |  NestJS API (Docker container)          |
                  |  Running on Google Cloud Run            |
                  +------------------+----------------------+
                                     |
                                     | Postgres connection
                                     v
                  +-----------------------------------------+
                  |           Database Layer                |
                  |-----------------------------------------|
                  |       Neon PostgreSQL (Serverless)      |
                  +-----------------------------------------+

### Key Technologies

- **Mobile App (React Native):**
  - **Framework:** Expo
  - **UI:** Tamagui, Lucide React Native
  - **Routing:** Expo Router
  - **State:** Zustand
  - **Data:** SQLite (Expo), Drizzle ORM
  - **Networking:** SWR
  - **Builds:** EAS (local + cloud)
  - **Language:** TypeScript

- **Backend API:**
  - **Framework:** NestJS
  - **Database:** PostgreSQL (Neon)
  - **ORM:** Prisma
  - **Validation:** Zod, Class-Validator
  - **Auth:** JWT, Google Auth Library, Resend
  - **API:** OpenAPI
  - **Hosting:** Dockerized on Google Cloud Run
  - **Language:** TypeScript

- **Web Frontend:**
  - **Framework:** React (Vite)
  - **UI:** TailwindCSS, Radix UI, Lucide
  - **Routing:** React Router
  - **Networking:** SWR
  - **Validation:** Zod
  - **Deployment:** Vercel
  - **Language:** TypeScript

---

## 📱 Screenshots

<p align="center">
<img src="screenshots/friends tab.png" width="230" />
<img src="screenshots/friend profile.png" width="230" />
<img src="screenshots/friend history.png" width="230" />
<img src="screenshots/history tab.png" width="230" />
<img src="screenshots/add interaction.png" width="230" />
<img src="screenshots/privacy.png" width="230" />
<img src="screenshots/dark mode.png" width="230" />
</p>

---

## 👨🏼‍💻 About the Developer

**Hi, I’m Michael** — AI Engineer & full-stack developer.

I built LangSyne end-to-end:

- System architecture
- Data modeling
- Backend (NestJS + Prisma)
- Mobile app (React Native + Expo)
- Deployment with Docker + Cloud Run
- EAS build pipeline
- UI/UX design

Feel free to reach out if you’d like to discuss the project or opportunities to collaborate: **applangsyne [at] gmail [dot] com** (or click the badge below)

<a href="mailto:applangsyne@gmail.com"> <img src="https://img.shields.io/badge/Email-Contact-red?logo=gmail&logoColor=white" /> </a>

---
