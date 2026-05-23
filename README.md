# 📱 Social Media Addiction & Mental Health Dashboard
### How Social Media Affects Young People | Power BI Analytics Project

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![CSV](https://img.shields.io/badge/Dataset-705%20Students-E74C3C?style=for-the-badge)

---

## 📌 Project Overview

This project explores how social media usage patterns affect the mental health, sleep quality, and academic performance of young people globally. Using a dataset of 705 students across 30+ countries, this Power BI dashboard uncovers behavioural trends, platform-specific addiction patterns, and demographic differences in social media consumption.

**Dataset:** 705 student records | 13 variables | 30+ countries | 8+ social media platforms

---

## 🎯 Business / Research Problem

Social media addiction among students is a growing public health concern. But which platforms are most harmful? Which age groups are most at risk? Do gender or relationship status affect usage patterns?

This dashboard answers those questions visually, translating raw behavioural data into clear, actionable insights for educators, policymakers, and researchers.

---

## 📊 Dataset Columns Explained

| Column | Description |
|--------|-------------|
| `Student_ID` | Unique identifier for each student |
| `Age` | Student age (18–24) |
| `Gender` | Male / Female |
| `Academic_Level` | High School / Undergraduate / Graduate |
| `Country` | Country of the student (30+ countries) |
| `Avg_Daily_Usage_Hours` | Average hours spent on social media per day |
| `Most_Used_Platform` | Primary platform (Instagram, TikTok, Facebook, etc.) |
| `Affects_Academic_Performance` | Yes / No — self-reported impact on academics |
| `Sleep_Hours_Per_Night` | Average nightly sleep hours |
| `Mental_Health_Score` | Mental health score (1–10, higher = better) |
| `Relationship_Status` | Single / In Relationship / Complicated |
| `Conflicts_Over_Social_Media` | Number of conflicts caused by social media (0–5) |
| `Addicted_Score` | Addiction severity score (1–10, higher = more addicted) |

---

## 🔍 Key Findings

| Finding | Data Point |
|---------|-----------|
| Most used platform globally | Instagram (largest user base) |
| Highest usage countries | India (324 students), USA (276 students) |
| Gender usage gap | Female: 5.01 hrs/day vs Male: 4.83 hrs/day |
| Most addictive platforms | Instagram & TikTok (addiction score 8–9/10) |
| Least addictive platform | LinkedIn (addiction score 2–3/10) |
| Peak usage age group | 20–22 years old |
| Overall addiction rate | 41.70% of students flagged as addicted |
| Mental health correlation | Higher addiction score = lower mental health score |
| Sleep impact | High-addiction students average less sleep per night |
| Academic impact | Majority of high-addiction students report academic performance affected |

---

## 📈 Dashboard Visuals

### KPI Cards (Top Row)
- **Total Students** — 705
- **Average Daily Usage** — 4.92 hrs/day
- **Average Mental Health Score** — 6.23 / 10
- **Average Sleep Hours** — 6.87 hrs/night
- **Addiction %** — 41.70%

### Charts & Visuals
- **Bar Chart** — Avg Daily Usage Hours by Gender
- **Treemap** — Total Students by Most Used Platform (Instagram dominates)
- **Bar Chart** — Avg Daily Usage Hours by Country (India & USA highest)
- **Area Chart** — Average Daily Usage by Age (peaks at 20–22, drops at 24)
- **Donut Chart** — Addicted Students by Addiction Score distribution
- **Matrix Table** — Gender vs Avg Usage Hours & Avg Sleep Hours
- **Gender Slicer** — Dynamic filter for all visuals
- **Q&A Feature** — Natural language queries on the dataset

---

## 💡 Insights & Interpretation

**Platform Risk Ranking (High to Low Addiction):**
1. Instagram / TikTok — Score 8–9 (highest risk)
2. Facebook / WhatsApp — Score 6–7 (moderate risk)
3. Twitter / Snapchat — Score 5–6 (moderate risk)
4. LinkedIn / YouTube — Score 2–3 (lowest risk)

**Why LinkedIn users score lowest:**
LinkedIn is used professionally, not for entertainment — usage is purposeful and time-limited, leading to lower addiction and better sleep patterns.

**Why the 24-year age group shows sharp decline:**
Students entering the workforce at 24 shift to professional platforms and reduce recreational usage — visible clearly in the age trend chart.

---

## 🛠️ Technical Stack

| Tool | Usage |
|------|-------|
| Power BI Desktop | Dashboard development, all visuals |
| Power Query | Data loading, type setting, transformations |
| DAX | KPI measures — averages, addiction %, counts |
| CSV | Raw dataset source |

---

## 📁 Repository Structure

```
social-media-mental-health-dashboard/
│
├── data/
│   └── social_media_mental_health.csv
│
├── dashboard/
│   └── Social_Media_Mental_Health.pbix
│
├── screenshots/
│   └── dashboard_overview.png
│
└── README.md
```


---

## 🔗 Key DAX Measures Used

```dax
Total Students = COUNTROWS('Dataset')

Avg Daily Usage = AVERAGE('Dataset'[Avg_Daily_Usage_Hours])

Avg Mental Health Score = AVERAGE('Dataset'[Mental_Health_Score])

Avg Sleep Hours = AVERAGE('Dataset'[Sleep_Hours_Per_Night])

Addiction % = 
DIVIDE(
    COUNTROWS(FILTER('Dataset', 'Dataset'[Addicted_Score] >= 6)),
    COUNTROWS('Dataset')
) * 100
```

---

## ⚠️ Disclaimer

This project uses a publicly available dataset for educational and portfolio purposes. All findings are based on the data provided and are intended for analytical demonstration only.
