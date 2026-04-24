# srm-Hierarchy-Challenge
# SRM Hierarchy Challenge

A full-stack web application developed for the **SRM Full Stack Engineering Challenge** that processes node relationships, detects cycles, removes duplicate edges, and visualizes hierarchy trees.

---

## Features

- Accepts node relationships in `Parent->Child` format
- Validates input structure
- Detects invalid entries
- Detects duplicate edges
- Identifies cyclic groups
- Builds hierarchy trees
- Calculates maximum tree depth
- Displays summary statistics
- Interactive frontend UI for visualization

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

### Request Body
```json
{
  "data": ["A->B", "A->C", "B->D"]
}
```

### Sample Response
```json
{
  "user_id": "yourname_ddmmyyyy",
  "email_id": "yourcollege@example.com",
  "college_roll_number": "YOURROLLNO",
  "hierarchies": [
    {
      "root": "A",
      "tree": {
        "A": {
          "B": {
            "D": {}
          },
          "C": {}
        }
      },
      "depth": 3
    }
  ],
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

### Clone Repository
```bash
git clone https://github.com/yourusername/srm-Hierarchy-Challenge.git
cd srm-Hierarchy-Challenge
```

### Backend Setup
```bash
cd backend
npm install
npm start
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

---

## Deployment Links

### Frontend
Add your frontend deployment URL here

### Backend
Add your backend deployment URL here

---

## Folder Structure

```bash
srm-Hierarchy-Challenge/
│── backend/
│── frontend/
│── README.md
```

---

## Processing Rules

- Valid format: `X->Y`
- Only single uppercase letters allowed
- Self-loops are invalid
- Duplicate edges stored separately
- First parent relationship is preserved
- Cycles returned separately
- Tree depth is longest root-to-leaf path

---

## Author

**Your Name**  
SRM Institute of Science and Technology

---

## License

This project was created for the **SRM Full Stack Engineering Challenge**.


