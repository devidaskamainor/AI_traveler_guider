# AI Traveler Guider

Generate travel descriptions and audio guides for destinations using the Google
GenAI and Murf APIs.

## Project structure

```text
AI_traveler_guider/
├── Backend/
│   ├── app.py
│   ├── requirements.txt
│   └── .env.example
├── Frontend/
│   ├── index.html
│   └── index.js
├── .gitignore
└── README.md
```

## Backend setup (Windows)

Open PowerShell in the `Backend` folder and install the dependencies:

```powershell
.\venv\Scripts\python.exe -m pip install -r requirements.txt
```

If you do not have a virtual environment yet, create one first:

```powershell
py -m venv venv
.\venv\Scripts\python.exe -m pip install -r requirements.txt
```

Create your local environment file from the example:

```powershell
Copy-Item .env.example .env
```

Edit `Backend\.env` and replace the placeholder values with your own API keys.
Do not commit or share this file. It is ignored by Git.

Start the backend from the `Backend` folder:

```powershell
.\venv\Scripts\python.exe app.py
```

## Frontend

With the backend running, open `Frontend\index.html` in a browser and use the
destination cards to generate an audio guide. The frontend sends requests to
`http://127.0.0.1:5000`.
