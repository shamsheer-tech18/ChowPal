# 🍲 ChowPal — Community-Driven Cultural Cooking & Grocery Marketplace

> Connecting international students with authentic recipes, local ethnic grocers, and food creators — all in one platform.

[![Status](https://img.shields.io/badge/Status-Product%20Case%20Study-blue.svg)](#)
[![Course](https://img.shields.io/badge/Course-DPDM%20Fall%202025-green.svg)](#)
[![University](https://img.shields.io/badge/Northeastern%20University-red.svg)](#)

---

## 📌 Overview

ChowPal is a **three-sided marketplace** designed for international students who struggle to find authentic cultural ingredients and trusted recipes in their college towns. The platform connects three key user groups: **students** discovering and cooking cultural recipes, **food creators** sharing expertise and earning money, and **local ethnic grocery stores** reaching new student customers.

Unlike existing grocery delivery apps or social recipe platforms, ChowPal bridges the gap between "I want to cook this" and "Where do I buy these ingredients?" - combining recipe discovery, ingredient sourcing, and local store partnerships into a single experience.

This repository contains the **complete product lifecycle documentation** for ChowPal, from initial concept and customer discovery through PRD, market research, roadmap, and wireframes developed as part of the Digital Product Design & Management (DPDM) course at Northeastern University.

---

## 🎯 The Problem

International students face three interconnected pain points that no single product solves today:

**Finding authentic ingredients is difficult.** Students don't know which stores carry specific cultural items. Generic grocery apps lack ethnic grocery partnerships, and substitution information is unreliable.

**Recipe discovery lacks shopping integration.** TikTok and Instagram provide recipes but no ingredient sourcing. There's no connection between finding a recipe and actually buying what you need to cook it.

**Ethnic grocery stores can't reach student customers.** Small ethnic grocers lack digital presence and marketing budgets. Students don't know these stores exist, and store owners have no platform to reach them.

### Validation

Our team conducted **25 customer development interviews** (15 buyers, 10 sellers) that confirmed these pain points: 87% of international students reported difficulty finding cultural ingredients as a frequent challenge, 60% have abandoned cooking certain dishes due to ingredient unavailability, and 100% of ethnic store owners expressed interest in better ways to reach student customers.

---

## 💡 The Solution

ChowPal works as a **video-first recipe discovery feed** (similar to TikTok) with integrated grocery purchasing. A student describes what they want to cook, discovers culturally authentic recipes from verified creators, sees ingredients grouped by nearby stores with real-time availability, and checks out through linked delivery services — all in one flow.

### Three User Experiences

**For Students** — A swipe-based discovery feed with dietary filters (halal, kosher, vegan, Jain, gluten-free), a servings adjustment slider that auto-scales ingredient quantities, ingredients grouped by store with prices and availability, and one-tap checkout through Instacart or Uber Eats.

**For Creators** — A creator studio with upload tools, AI-assisted ingredient tagging, video analytics (views, engagement, orders generated), earnings dashboard ($0.01/view + $0.50/order + tips), and store partnership management.

**For Store Owners** — A business portal showing order volume and revenue, a creator discovery tool to find and partner with local food creators, inventory management with low-stock alerts, and ingredient-level performance analytics to move slow inventory.

---

## 🏗️ Product Architecture

```
┌──────────────────────────────────────────────────────────────┐
│                     ChowPal Mobile App                       │
│              (React Native — iOS & Android)                   │
├──────────┬───────────────┬───────────────┬───────────────────┤
│ Student  │   Creator     │  Store Owner  │     Admin         │
│ Feed &   │   Studio &    │  Dashboard &  │   Moderation &    │
│ Shopping │   Analytics   │  Partnerships │   Operations      │
└────┬─────┴───────┬───────┴───────┬───────┴─────────┬─────────┘
     │             │               │                 │
     ▼             ▼               ▼                 ▼
┌──────────────────────────────────────────────────────────────┐
│                      Backend APIs                            │
│            (PostgreSQL · S3 · Stripe Connect)                │
├──────────────────────────────────────────────────────────────┤
│  AI Layer: Recommendations · Dietary Filtering · Ingredient  │
│  Detection · Content Moderation                              │
├──────────────────────────────────────────────────────────────┤
│  Integrations: Instacart API · Uber Eats API · Google Maps   │
│  · Cloudflare Stream (Video) · AWS CloudFront (CDN)          │
└──────────────────────────────────────────────────────────────┘
```

---

## 📊 Market Opportunity

| Metric | Value |
|---|---|
| International students in the US | 1.1 million (2024) |
| Ethnic grocery market in college towns | $2 billion |
| TAM (recipe-driven grocery shopping) | $260M annual revenue opportunity |
| Target CAC | < $15 |
| Target LTV | > $150 |
| Commission model | 10–15% per transaction |

---

## 🗺️ Product Roadmap

**Q1 — MVP Launch (Version 1.0):** Recipe discovery feed, dietary filters, delivery integration, creator video upload, 10–15 ethnic store partnerships. Target: 500 active users, 100 orders.

**Q2 — Community Features (Version 2.0):** Ratings, comments, save collections, social sharing, push notifications. Target: 2,000 users, 500 monthly orders.

**Q3 — AI & Monetization (Version 3.0):** AI meal recommendations, voice-guided cooking mode, ingredient substitutions, creator monetization scaling. Target: 5,000 users, 2,000 monthly orders.

**Q4 — National Scale (Version 4.0):** Live cooking sessions, community challenges, multi-language support, store inventory integration, expansion to 10 cities. Target: 15,000 users, $50K monthly revenue.

---

## 📂 Repository Structure

```
ChowPal/
│
├── README.md                                    ← This file
│
├── 01-project-proposal/
│   └── Project_Proposal.docx                    ← Initial concept & idea selection
│
├── 02-customer-discovery/
│   ├── Customer_Segmentation_Part_1.docx        ← Target segments & interview questions
│   └── Customer_Segmentation_Part_2.docx        ← Interview findings & insights
│
├── 03-market-research/
│   └── Market_Research.docx                     ← Competitive analysis & market sizing
│
├── 04-personas/
│   └── Persona.docx                             ← Detailed user personas
│
├── 05-user-stories/
│   └── User_Stories.docx                        ← 15 user stories across all user types
│
├── 06-metrics/
│   └── Metrics.docx                             ← KPIs across acquisition, engagement,
│                                                   retention, and business performance
│
├── 07-product-roadmap/
│   └── Product_Roadmap.docx                     ← Quarterly roadmap with milestones
│
├── 08-prd/
│   └── PRD_ChowPal.pdf                          ← Full Product Requirements Document
│
├── 09-budget/
│   └── ChowPal_Budget_Estimations.docx          ← Year 1 cost projections (~$850K)
│
├── 10-wireframes/
│   ├── Storyboard_Student_Flow.jpeg             ← Student onboarding & recipe discovery
│   ├── Storyboard_Creator_Studio.jpeg           ← Creator dashboard & analytics flow
│   └── Storyboard_Store_Dashboard.jpeg          ← Store owner partnership flow
│
├── 11-presentations/
│   ├── MRD_Presentation.pptx                    ← Market Requirements Document deck
│   └── PRD_Presentation.pptx                    ← Product Requirements Document deck
│
└── 12-project-summary/
    └── Project_Experience.docx                  ← Concise project summary for portfolios
```

---

## 📄 Key Deliverables at a Glance

| Deliverable | What It Covers |
|---|---|
| **Project Proposal** | Vision statement, problem definition, TAM ($260M opportunity), target segments |
| **Customer Discovery** | 25 interviews (15 buyers, 10 sellers), 3 buyer + 3 seller segments, key findings |
| **Market Research** | Competitive landscape (Instacart, TikTok, HelloFresh), positioning, SWOT |
| **Personas** | Detailed profiles for student cook, recipe creator, store owner, and admin |
| **User Stories** | 15 stories spanning students, creators, store owners — with acceptance criteria |
| **Metrics** | KPIs for acquisition, engagement, retention, and business health |
| **Product Roadmap** | 4-quarter plan from MVP to national scale with measurable targets |
| **PRD** | Complete requirements doc with use cases, wireframes, tech stack, and risk register |
| **Budget** | Year 1 projection: $850K (70% personnel, 20% infrastructure, 10% operations) |
| **Wireframes** | Hand-drawn storyboards for all 3 user flows (student, creator, store owner) |
| **Presentations** | MRD and PRD slide decks for stakeholder communication |

---

## 🔮 Future Vision

ChowPal's long-term roadmap includes AI-powered meal planning, voice-controlled cooking mode, multi-language support (Spanish, Mandarin, Hindi), native iOS/Android apps, national expansion to 20 US cities, and international pilots in Toronto, London, and Sydney. The subscription model (Free / ChowPal Plus at $5/mo / ChowPal Pro at $15/mo) and creator memberships provide a path to sustainable revenue beyond transaction commissions.

---

<p align="center">
  <b>⭐ If you found this product case study interesting, consider giving the repo a star!</b>
</p>
