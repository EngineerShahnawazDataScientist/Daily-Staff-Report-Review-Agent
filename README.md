# Daily-Staff-Report-Review-Agent
Python automation to review daily staff reports, detect missed tasks, and generate follow-up or escalation actions using Pandas

📌 Objective

This project automates the review of daily staff reports to detect missed tasks, generate follow-ups, and escalate repeated misses.
It demonstrates automation/logic workflow design using Python (Pandas).

📂 Dataset

Input file: Candidate_Task_DailyReports.xlsx

Columns include: Employee, Task, Date, Status

⚙️ Workflow

Load Data

Read the Excel file using pandas.

Convert the Date column to datetime and sort the records by Employee, Task, and Date.

Filter Missed Tasks

Extract only rows where Status = 'Not Done'.

Group and Analyze

Group data by Employee and Task.

Check missed dates sequence:

If missed once → mark as Follow-up

If missed on two or more consecutive days → mark as Escalate

Output

Create a results table with:

Employee | Task | Date(s) Missed | Action

Save output as: Output_DailyReportReview.xlsx

📊 Example Output
Employee	Task	Date(s) Missed	Action
Alice	Send Daily Sales Report	2025-07-02	Follow-up
Alice	Send Daily Sales Report	2025-07-02, 2025-07-03	Escalate
Bob	Resolve High Priority Ticket	2025-07-01, 2025-07-02	Escalate
📜 Files in Repository

Candidate_Task_DailyReports.xlsx → Input data (mock staff reports)

daily_report_review.py → Python script to process reports

Output_DailyReportReview.xlsx → Generated output file

DailyReport_Approach.docx → Brief documentation of approach

README.md → Project description (this file)

✅ Conclusion

This automation script reviews daily staff reports, identifies missed tasks, and flags them for follow-up or escalation.
It can be extended for larger datasets or integrated into regular reporting pipelines.
