# Role and Objective
You are an expert Database Architect and Technical Interview Coach specializing in MySQL, MongoDB, and system troubleshooting. Your task is to generate a fully functional, interactive single-page web application (HTML, CSS, JavaScript) that serves as a "101 SQL Coaching & Optimization" platform. 

# Target Audience Profile
The user is an experienced IT operations professional preparing for a technical support role in the cross-border payment sector in Thailand. They are comfortable with Linux environments, Docker, and infrastructure troubleshooting, but need to sharpen their database skills—specifically MySQL query optimization, indexing, and data retrieval for real-world business pain points.

# Application Specifications
Generate a self-contained web app with the following features:

## 1. Mock Database Context (The "Payment Ecosystem")
Provide a reference schema for a mock cross-border payment system. Display this schema clearly in the UI.
*   **Tables:**
    *   `transactions` (txn_id, sender_id, receiver_id, amount, source_currency, target_currency, status, created_at)
    *   `users` (user_id, country_code, kyc_status, joined_date)
    *   `system_logs` (log_id, service_name, error_code, response_time_ms, timestamp)

## 2. Interactive Practice Modules
Create a tabbed or step-by-step interface containing three specific coaching modules:

*   **Module A: Day-to-Day Troubleshooting (Selects & Joins)**
    *   *Scenario:* Customer support escalates a failed transaction. 
    *   *Task:* Write a query to find all 'FAILED' transactions originating from Thailand ('TH') within the last 24 hours, joined with the user's KYC status.
    *   *Interactive element:* A text area for the user to input their SQL, with a "Run" button that reveals the correct answer and explains the logic.

*   **Module B: Query Optimization & Indexing**
    *   *Scenario:* The operations team reports that the internal dashboard is timing out during peak hours. The current query doing a full table scan is: `SELECT * FROM transactions WHERE status = 'PENDING' AND created_at > '2023-01-01';`
    *   *Task:* Identify the performance bottleneck. 
    *   *Interactive element:* Multiple choice or drag-and-drop to select the best indexing strategy (e.g., Composite Index on `status` and `created_at`). Include an explanation of how a B-Tree index prevents a full table scan.

*   **Module C: Linux & DB Intercept (The CLI perspective)**
    *   *Scenario:* A slow query is dragging down the MySQL process.
    *   *Task:* Provide a quick flashcard or interactive terminal mock asking for the common Linux commands (like `top`, `htop`, or `grep` on MySQL slow logs) and MySQL commands (like `SHOW PROCESSLIST` or `EXPLAIN`) used to locate the offending query.

## 3. UI/UX Requirements
*   Use a clean, modern, dark-mode interface that mimics a terminal or IDE environment.
*   Include syntax highlighting for the SQL code blocks.
*   Provide immediate, constructive feedback for any interactive quizzes or code checks.

# Output Format
Output the entire application as a single `index.html` file containing all necessary inline CSS and JavaScript. Ensure the code is production-ready and error-free so it can be opened directly in a browser.