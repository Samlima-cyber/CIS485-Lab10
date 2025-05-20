# Lab 10: Candidate Search & Filter API

**Course:** CIS 485 - Web Programming II  
**Student:** Sam Lima  

## 🧠 Objective
This API allows users to:
- Search political candidates by query string (`GET /search`)
- Filter candidates by JSON body content (`POST /filter`)

It demonstrates:
- Query string parsing
- JSON body handling
- Express routing and filtering logic

---

## 🚀 Setup Instructions

1. Install dependencies:
```bash
npm install express
Start the server:

bash
Copy
Edit
node server.js
Open in your browser:
http://localhost:3000

📌 API Endpoints
🔹 GET /
Displays a friendly HTML homepage with usage instructions.

🔹 GET /search
Search candidates by party and/or platform.

Examples:

One filter:

bash
Copy
Edit
curl "http://localhost:3000/search?party=Cheese%20Liberators"
Multiple filters:

bash
Copy
Edit
curl "http://localhost:3000/search?party=Jam%20Union&platform=Spread"
🔹 POST /filter
Filter candidates by JSON body with platform and/or slogan.

Example:

bash
Copy
Edit
curl.exe --% -X POST http://localhost:3000/filter -H "Content-Type: application/json" -d "{\"platform\":\"Pro-Biscuit Legislation\"}"
Another Example:

bash
Copy
Edit
curl.exe --% -X POST http://localhost:3000/filter -H "Content-Type: application/json" -d "{\"slogan\":\"Cheddar for President!\"}"
✅ Sample Response
json
Copy
Edit
[
  {
    "id": 3,
    "name": "Count Gorgonzola III",
    "party": "Cheese Liberators",
    "platform": "Free the Cheese!",
    "slogan": "Cheddar for President!"
  }
]
🧪 Testing Tools
curl (with curl.exe --% in PowerShell)

Postman (optional)

📁 File Structure
pgsql
Copy
Edit
candidate-lab/
├── server.js
├── candidates.json
├── package.json
└── node_modules/
