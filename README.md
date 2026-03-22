# Frammer AI Analytics Dashboard
Following are the run instructions for the dashboard. The link for it is here: [Open Website](https://frammer-dashboard-3apj.vercel.app/dashboard2)
It takes 10-15 minutes to load.

## Prerequisites
- Node.js
- Python
- pip
- Git

## Clone the Repository
```
git clone <https://github.com/KopalJain0630/FrammerDashboard>
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

Open: https://frammer-dashboard-3apj.vercel.app/dashboard

### Backend Finetuning

You can create the custom dataset using code
```
python backend/create_database.py
```

To see the finetuning run `backend/textsql.ipynb`