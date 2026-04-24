# srm-Hierarchy-Challenge
# Hierarchy Engine

A full-stack web application that processes node relationships and converts them into structured hierarchy trees with cycle detection, duplicate filtering, and visualization.

## Features

- Accepts node relationships in `Parent->Child` format
- Detects invalid entries
- Removes duplicate edges
- Detects cyclic relationships
- Builds hierarchy trees
- Calculates tree depth
- Displays:
  - Total Trees
  - Total Cycles
  - Largest Tree Root
- Interactive frontend visualization

---

## Tech Stack

### Frontend
- React
- CSS
- Axios

### Backend
- Node.js
- Express.js

### Deployment
- Frontend: Vercel
- Backend: Render

---

## API Endpoint

### POST `/bfhl`

#### Request
```json
{
  "data": ["A->B", "A->C", "B->D"]
}
```

#### Response
```json
{
  "user_id": "yourname_ddmmyyyy",
  "email_id": "yourcollege@example.com",
  "college_roll_number": "YOURROLLNO",
  "hierarchies": [],
  "invalid_entries": [],
  "duplicate_edges": [],
  "summary": {
    "total_trees": 1,
    "total_cycles": 0,
    "largest_tree_root": "A"
  }
}
```

---

## Installation

### Clone repository
```bash
git clone https://github.com/yourusername/hierarchy-engine.git
cd hierarchy-engine
```

### Backend setup
```bash
cd backend
npm install
npm start
```

### Frontend setup
```bash
cd frontend
npm install
npm run dev
```

---

## Deployment Links

### Frontend
Add your frontend URL here

### Backend
Add your backend URL here

---

## Project Structure

```bash
hierarchy-engine/
│── backend/
│── frontend/
│── README.md
```

---

## Processing Rules

- Valid format: `X->Y`
- Only single uppercase letters allowed
- Self loops are invalid
- First encountered parent wins
- Duplicate edges are reported
- Cycles are detected separately

---

## Author

**Your Name**  
SRM Institute of Science and Technology

---

## License

This project is developed for the SRM Full Stack Engineering Challenge.
