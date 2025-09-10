# Task Control System

A modular **task management system** built with Python. It allows users to **sign up, log in, create plans, add tasks**, and provides **analytics with predictions and visualizations**.  
All data is stored in **JSON files** for simplicity and portability.

---

## Project Structure

```
task_control_system/
│
├── data/                          # JSON storage files
│   ├── user.json                   # Stores user details
│   ├── plan.json                   # Stores plans mapped to users
│   ├── task.json                   # Stores tasks mapped to plans
│   └── taskcontrol.json            # (Optional) Master linking file
│
├── services/                      # Core business logic
│   ├── user_manager.py             # CRUD operations for users
│   ├── plan_manager.py             # CRUD operations for plans
│   ├── task_manager.py             # CRUD operations for tasks
│   └── utils.py                    # Helpers (JSON I/O, timestamps, etc.)
│
├── auth/                          # Authentication module
│   ├── signup.py                   # Register new users
│   ├── login.py                    # User login logic
│   └── auth_utils.py               # Password hashing, token/session mgmt
│
├── analytics/                     # Analytics and prediction models
│   ├── charts.py                   # Graph generation (Matplotlib/Seaborn)
│   ├── stats.py                    # Summary statistics
│   ├── prediction_model.py         # ML/DL models for task prediction
│   └── report_generator.py         # Generate PDF/Excel/HTML reports
│
├── main.py                        # Entry point for running the app
├── requirements.txt               # Python dependencies
├── README.md                      # Project documentation
└── .gitignore                     # Ignore unnecessary files
```

---

## Features

- User Management
  - Register new users (signup)
  - Login with authentication
  - Secure password hashing

- Plan Management
  - Create, update, and delete plans
  - Assign plans to specific users
  - Track progress and deadlines

- Task Management
  - Add, update, and mark tasks as complete
  - Link tasks to specific plans
  - Due date and status tracking

- Analytics
  - Generate summary statistics on tasks and plans
  - Visualize progress with charts (Matplotlib/Seaborn)
  - Predict task completion trends with ML/DL models
  - Export reports (PDF/Excel/HTML)

- Data Storage
  - JSON-based (portable and human-readable)
  - `user.json`, `plan.json`, `task.json`, `taskcontrol.json`

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/task_control_system.git
   cd task_control_system
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Linux/Mac
   venv\Scripts\activate      # On Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage

Run the main entry file:

```bash
python main.py
```

### Example Workflow
1. Sign up → Create a new user  
2. Log in → Authenticate the user  
3. Create a plan → Assign start/end dates  
4. Add tasks → Attach tasks to the plan  
5. View analytics → Generate charts/statistics/reports  

---

## Analytics & Predictions

- Task completion rates per plan/user  
- Overdue vs completed tasks  
- Trend forecasting (e.g., expected completion probability)  
- Export reports in PDF, Excel, or HTML  

---

## Tech Stack

- Language: Python 3.9+  
- Data Storage: JSON  
- Libraries:
  - pandas (data manipulation)
  - matplotlib, seaborn (visualization)
  - scikit-learn / tensorflow (predictions)
  - reportlab / openpyxl (report generation)

---

## Future Improvements

- Add SQLite/PostgreSQL support for scalability  
- Web-based dashboard (Flask/Streamlit)  
- Real-time collaboration features  
- API endpoints for integration  

---

## Contributors

- Anik Dashora – Project Lead & Developer  

---

## License

This project is licensed under the **MIT License** – feel free to use and modify it.
