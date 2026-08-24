# GitHub Analytics Pipeline

**Course:** Fundamentals of Data Engineering (24DEA3101R)  
**Department:** Computer Science and Engineering (CSE)  
**Academic Year:** 2026–27

---

## Team Members

| Name | Student ID |
|------|------------|
| Satya Austin Abner | 2420030587 |
| Animesh Balaji | 2420030301 |
| Navaneeth | 2420030306 |

**Project Guide / Supervisor:** Dr.Nalla Sirisha

---

## Project Abstract

GitHub Analytics Pipeline is an end-to-end **Data Engineering** project that extracts software development data from the GitHub REST API, processes and transforms the raw data, stores it in a structured PostgreSQL database, and generates meaningful analytical insights through interactive visualizations.

The project demonstrates the complete ETL (Extract, Transform, Load) workflow by collecting repository information, commits, issues, pull requests, contributors, stars, forks, and programming language statistics from GitHub repositories. The processed data is cleaned, validated, modeled into relational tables, and analyzed to understand repository activity, developer contributions, and project health.

---

## Problem Statement

GitHub provides a large amount of software development data through REST APIs, but the raw API responses are not directly suitable for analytics because:

- Data is distributed across multiple API endpoints.
- API responses contain nested and inconsistent structures.
- Manual data collection is time-consuming.
- Data requires cleaning, validation, and transformation.
- API rate limits affect repeated requests.
- Direct API queries are inefficient for complex analysis.

This project solves these challenges by building an automated analytics pipeline that centralizes and structures GitHub data for efficient querying and visualization.

---

## Project Objectives

- Extract repository, commit, issue, pull request, and contributor data using the GitHub REST API.
- Build a reliable data ingestion pipeline.
- Clean and transform raw API data.
- Handle missing values, duplicates, and inconsistent formats.
- Design a normalized relational data model.
- Store processed data in PostgreSQL.
- Perform SQL-based analytics on repository activity and developer contributions.
- Generate dashboards and visualizations for analytical insights.
- Build a scalable pipeline that can support multiple repositories in the future.

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| Python | ETL pipeline development |
| GitHub REST API | Data extraction source |
| Pandas | Data cleaning and transformation |
| PostgreSQL | Structured data storage |
| Streamlit | Interactive analytics dashboard |
| Git & GitHub | Version control and collaboration |
| Apache Airflow | Pipeline scheduling and orchestration |
| Docker *(Optional)* | Containerization and deployment |

---

## System Architecture

The project follows a standard ETL-based Data Engineering architecture:

1. **Extract** – Fetch repository, commit, issue, pull request, and contributor data from GitHub REST API.
2. **Transform** – Parse JSON responses, clean data, remove duplicates, validate records, and standardize formats.
3. **Load** – Store processed data into normalized PostgreSQL tables.
4. **Analytics** – Execute SQL queries to generate repository and contributor insights.
5. **Visualization** – Display metrics and trends using a Streamlit dashboard.

---

## Repository Structure

```text
KLH-CSE-2026-Team10-GitHubAnalyticsPipeline/
│── README.md
│
├── src/            # Python ETL pipeline and source code
├── docs/           # PPT, diagrams, and documentation
├── data/           # Sample datasets or data source references
├── results/        # Output reports, screenshots, and visualizations
└── reports/        # Phase-wise and final project reports
```

---

## Setup Instructions

### Clone the Repository

```bash
git clone https://github.com/<your-team>/KLH-CSE-2026-Team10-GitHubAnalyticsPipeline.git
cd KLH-CSE-2026-Team10-GitHubAnalyticsPipeline
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure GitHub API

Create a `.env` file and add your GitHub Personal Access Token.

```env
GITHUB_TOKEN=your_personal_access_token
```

### Run the Pipeline

```bash
python main.py
```

### Launch Dashboard

```bash
streamlit run app.py
```

---

## Expected Output

The pipeline generates analytics including:

- Repository activity summary.
- Commit trends over time.
- Contributor statistics.
- Issue and pull request analysis.
- Stars and forks metrics.
- Programming language distribution.
- Interactive dashboard visualizations.

---

## Project Status

| Phase | Status |
|-------|--------|
| Phase 1 – Project Proposal & PPT | ✅ Completed |
| Phase 2 – Data Extraction & ETL | 🚧 In Progress |
| Phase 3 – Database & Analytics | ⏳ Pending |
| Final Phase – Dashboard & Documentation | ⏳ Pending |

---

## Future Enhancements

- Support multiple GitHub repositories.
- Incremental data loading.
- Real-time pipeline scheduling using Apache Airflow.
- Docker-based deployment.
- Advanced contributor and project health analytics.

---

## Important Note

This repository is maintained as part of the **Fundamentals of Data Engineering** course project at **KLH University**. All team members contribute using their individual GitHub accounts, and phase deliverables are committed progressively with Git tags (`review-1`, `review-2`, `final`).
