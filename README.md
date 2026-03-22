# Frammer AI Analytics Dashboard
Frammer Dashboard is a *full-stack analytics platform* that combines interactive visualizations with an *AI-powered chatbot*.  
Users can explore data, identify trends, and generate insights — all using simple natural language queries. The link for it is here: [Open Website](https://frammer-dashboard-3apj.vercel.app/dashboard2)
It takes 10-15 minutes to load.

---

## Key Features  

*Interactive Dashboard* – Visualize data with charts and trends  
*AI Chatbot* – Ask questions in plain English  
*Text-to-SQL Engine* – Converts queries into SQL automatically  
*Trend Analysis* – Monthly insights and performance tracking  
*Real-time Processing* – Fast and responsive system  
*Clean UI/UX* – Simple and intuitive design  

---

## Tech Stack  

| Layer       | Technology |
|------------|-----------|
| Frontend | Next.js, React, Tailwind CSS, Recharts |
| Backend  | FastAPI, Python |
| Database | SQLite |
| AI       | Text-to-SQL / Chatbot Logic |

---

## Project Structure

```
FrammerGC/
│
├── backend/                      # FastAPI backend
│   ├── data/                     # Processed datasets
│   ├── models/                   # Fine-tuned NLP model
│   │   └── final_text2sql_model/
│   ├── routes/                   # API routes
│   ├── schemas/                  # Pydantic schemas
│   ├── services/                 # Business logic and SQL generation
│   └── main.py                   # FastAPI entry point
│
├── frontend/                     # Next.js frontend
│   ├── app/
│   │   ├── componentNav/         # Navigation components
│   │   ├── components/           # Reusable UI components
│   │   ├── dashboard/            # Executive Summary
│   │   ├── dashboard2/           # Usage & Trends
│   │   ├── dashboard3/           # Multi-dimensional Analysis
│   │   ├── dashboard4/           # Output Mix
│   │   ├── dashboard5/           # Video Funnel
│   │   ├── layout.tsx            # Root layout
│   │   └── page.tsx              # Home page
│   │
│   ├── lib/                      # Utility functions
│   ├── public/                   # Static assets
│   └── services/                 # API calling functions
│
└── README.md
```

## Clone the Repository
```
git clone https://github.com/KopalJain0630/FrammerDashboard
cd FrammerDashboard
```

## Start Backend
```
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

Backend runs on: http://127.0.0.1:8000

## Start Frontend
```
cd frontend
npm install
npm run dev
```

Frontend runs on: https://frammer-dashboard-3apj.vercel.app/dashboard

## Environment Variable
Create a file named `.env.local` inside the frontend folder and add:
```
NEXT_PUBLIC_API_URL=http://127.0.0.1:8000
```

## Run Full Application

| Service  | Command |
|----------|---------|
| Backend  | uvicorn main:app --reload |
| Frontend | npm run dev |

Open: https://frammer-dashboard-3apj.vercel.app/dashboard OR http://localhost:3000

### Backend Finetuning

You can create the custom dataset using code
```
python backend/create_database.py
```

To see the finetuning run `textsql.ipynb` in the `backend` folder.
Please refer to [DA2026_08_Report.pdf] for detailed report.
