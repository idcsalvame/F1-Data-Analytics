# 🏎️ F1 Data Analytics Project

This project explores and analyzes Formula 1 race data using Python and the [FastF1](https://github.com/theOehrly/Fast-F1) library, PostgreSQL for structured data storage, and Power BI for data visualization. The development environment is fully containerized using Docker and Dev Containers in VS Code for clean and reproducible development.

---

## 📌 Objectives

- Practice and improve my skills in **Python**, **SQL**, and **Power BI**
- Learn how to ingest and work with real-world Formula 1 data via FastF1
- Build structured and queryable data models using **PostgreSQL**
- Create insightful **Power BI dashboards** connected directly to the data
- Develop the project in a **reproducible Docker environment** for easy reuse and sharing

---

## 🧱 Tech Stack

| Tool                   | Role                          |
|------------------------|-------------------------------|
| Python                 | Data collection & processing  |
| FastF1                 | F1 data acquisition via API   |
| PostgreSQL             | Relational database storage   |
| Power BI               | Data visualization/dashboard  |
| Docker & Compose       | Containerized environment     |
| VS Code + DevContainer | Development environment setup |

---

## 📂 Project Structure

```bash
f1-data-analytics/
│
├── .devcontainer/         # VS Code Dev Container configuration
│   ├── devcontainer.json
│   └── Dockerfile
│
├── docker/                # Docker-related configuration files
│   └── db/                # PostgreSQL container config & init
│       ├── init.sql
│       └── [optional PostgreSQL configs]
│
├── data/                  # Raw or processed data artifacts
├── notebooks/             # Jupyter notebooks for data exploration
├── src/                   # Python scripts (ETL, helpers, etc.)
│   └── ingest.py
│
├── dashboards/            # Power BI files (.pbix)
├── requirements.txt       # Python dependencies
├── docker-compose.yml     # Docker orchestration file
├── .env                   # Environment variables (not committed)
└── README.md              # Project documentation
````

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/f1-data-analytics.git
cd f1-data-analytics
```

### 2. Open in VS Code

* Make sure you have the **Dev Containers** extension installed.
* Open the project folder in VS Code.
* When prompted, select **"Reopen in Container"**.

### 3. Start the Containers

```bash
docker-compose up -d
```

This will spin up:

* A Python dev environment
* A PostgreSQL database container named `F1Data`

### 4. Install Python Dependencies

Inside the dev container terminal:

```bash
pip install -r requirements.txt
```

---

## 🔄 Data Flow Overview

1. **FastF1** retrieves session, lap, and telemetry data.
2. **Python scripts** (in `src/`) transform the data as needed.
3. Data is loaded into **PostgreSQL**, using `psycopg2-binary`.
4. **Power BI** connects via ODBC/Npgsql to build dashboards.

---

## 🗄️ PostgreSQL Setup

All PostgreSQL container configuration files are located in:

```bash
docker/db/
```

* `init.sql`: Runs on first container startup to initialize your schema or seed test data.

---

## 📊 Power BI Integration

Once the database has data:

* Use **Power BI Desktop**
* Connect to `localhost:5432` using PostgreSQL (via ODBC or Npgsql)
* Import and model the data
* Design visual dashboards

---

## 🔍 Sample Dashboards (Coming Soon)

> Planned visuals:

* Lap time comparisons
* Race pace overviews
* Driver telemetry overlays
* Pit strategy breakdowns

Dashboards will be stored in the `dashboards/` folder.

---

## 📌 Roadmap

* [x] Set up VS Code Dev Container and Docker environment
* [x] Set up PostgreSQL container with init SQL
* [ ] Create schema for F1 data
* [ ] Write data ingestion scripts using FastF1
* [ ] Run exploratory data analysis via notebooks
* [ ] Design and export Power BI dashboards
* [ ] Finalize and polish GitHub repo for portfolio

---

## 🧠 Key Learnings

* Setting up a reproducible container-based workflow
* Working with motorsport telemetry and timing data
* Designing a structured relational database for real-world data
* Building polished visual insights using Power BI

---

## 📜 License

This project is for learning and personal portfolio use. Feel free to fork, reference, or build on it with credit.

---

## 🙋‍♂️ About Me

I'm Ivan — a Computer Science graduate and aspiring data analyst.
This project is part of my data analytics journey and serves as both a sandbox and portfolio piece.
📫 [GitHub](https://github.com/idcsalvame) | [LinkedIn](https://www.linkedin.com/in/ivan-salvame)
