# 📊 Supplier Selection Decision Support System (DSS)

<p align="center">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/Lucide_Icons-F97316?style=for-the-badge&logo=lucide&logoColor=white" alt="Lucide Icons" />
</p>

> **Academic Group Project** for the **Business Intelligence** course at Universitas Ma Chung.

A web-based Decision Support System (DSS) dashboard engineered to evaluate, rank, and select optimal business suppliers. This application implements a hybrid decision-making approach combining the **Analytic Hierarchy Process (AHP)** for criteria weighting and the **Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS)** for alternative ranking[cite: 2].

---

## 👥 Authors & Project Team

* **Monica Clarista Gracianna** (NIM: 322410014)[cite: 2]
* **Siti Nur Hadiah** (NIM: 322410015)[cite: 2]

---

## 📌 Executive Summary

Selecting the right supplier is a critical strategic decision in supply chain management. This project provides an intuitive, data-driven dashboard that automates multi-criteria evaluation. By synthesizing qualitative expert judgment via AHP with quantitative geometric distance scoring via TOPSIS, the system reduces bias and streamlines supplier selection workflows.

---

## 🛠️ Tech Stack & Architecture

| Layer | Technology | Role & Purpose |
| :--- | :--- | :--- |
| **Frontend Framework** | **React 18** | Component-based UI architecture for interactive view switching |
| **Type Safety** | **TypeScript** | Strict typing for criteria vectors, pairwise matrices, and ranking schemas[cite: 2] |
| **Build Tooling** | **Vite** | Fast local development server and optimized bundle compilation[cite: 2] |
| **Styling & UI** | **Tailwind CSS** | Responsive dashboard layout and utility-first styling |
| **Icons** | **Lucide React** | Clean visual indicators for navigation and matrix controls |
| **Core Algorithms** | **TypeScript (Native)** | Custom implementation of matrix normalization, consistency ratio (CR) calculation, ideal solutions ($A^+$ / $A^-$), and relative closeness scores ($C_i^*$)[cite: 2] |

---

## ⚡ Core Features & Decision Modules

- 📋 **Problem Context (`PermasalahanView`)**: Detailed overview of decision criteria and business evaluation goals[cite: 2].
- 🗂️ **Dataset Management (`DatasetView`)**: Display and configuration of supplier alternatives and raw performance metrics[cite: 2].
- ⚖️ **Criteria & Weights (`KriteriaBobotView`)**: Configuration of decision parameters and weight distributions[cite: 2].
- 📐 **AHP Calculation Engine (`AHPView`)**: Pairwise comparison matrices to derive criteria weights and verify Consistency Ratios ($CR < 0.1$)[cite: 2].
- 📊 **TOPSIS Matrix Processing (`TOPSISView`)**: Matrix normalization, weighted normalized matrix computation, and positive/negative ideal solution determination[cite: 2].
- 🏆 **Ranking & Recommendations (`RankingView` & `RekomendasiView`)**: Final aggregated supplier rankings with actionable decision insights[cite: 2].
- 📈 **Summary Dashboard (`DashboardView`)**: High-level visual dashboard summarizing scores and top supplier metrics[cite: 2].

---

## 📂 Project Structure

```text
.
├── src/
│   ├── components/
│   │   ├── DashboardView.tsx     # Executive overview dashboard
│   │   ├── DatasetView.tsx       # Supplier alternative dataset management
│   │   ├── PermasalahanView.tsx  # Problem context & objective specifications
│   │   ├── KriteriaBobotView.tsx # Decision criteria configuration
│   │   ├── AHPView.tsx           # AHP pairwise comparison matrix & consistency checks
│   │   ├── TOPSISView.tsx        # TOPSIS vector normalization & distance scoring
│   │   ├── RankingView.tsx       # Aggregated supplier ranking results
│   │   └── RekomendasiView.tsx   # Automated decision recommendations
│   ├── App.tsx                   # Main layout shell & tab navigation
│   ├── calculations.ts           # Algorithmic engine for AHP & TOPSIS math
│   ├── dataset.ts                # Initial mock dataset & criteria definitions
│   ├── types.ts                  # TypeScript data interfaces & matrix definitions
│   └── main.tsx                 # React DOM entry point
├── index.html                    # Root HTML template
├── vite.config.ts                # Vite build setup
└── package.json                  # Node dependencies & project scripts
