# SQL Query Filters

**Project Description**  
This project showcases how I used SQL queries to investigate login activity 
and isolate department-specific data during a system audit. The queries include 
logical filters, time-based conditions, and pattern matching.

---

## 🔐 After-Hours Failed Login Attempts

Filtered for failed login attempts occurring after business hours (6:00 PM).

![After Hours Failed Login](https://raw.githubusercontent.com/eldoktor1/SQL-Query-Filters/main/sql_filters_images/sql_page_1_img_1.png)

    SELECT * FROM log_in_attempts
    WHERE login_time > '18:00'
      AND success = FALSE;

---

## 📅 Logins on Specific Dates

Queried for login attempts on May 8th and May 9th, 2022.

![Query Date Filtering](https://raw.githubusercontent.com/eldoktor1/SQL-Query-Filters/main/sql_filters_images/sql_page_2_img_1.png)

    SELECT * FROM log_in_attempts
    WHERE login_date = '2022-05-08'
       OR login_date = '2022-05-09';

![Result Sample](https://raw.githubusercontent.com/eldoktor1/SQL-Query-Filters/main/sql_filters_images/sql_page_2_img_2.png)

---

## 🌍 Logins Outside Mexico

Filtered records where the login country is not Mexico.

![Not Mexico Filter](https://raw.githubusercontent.com/eldoktor1/SQL-Query-Filters/main/sql_filters_images/sql_page_3_img_1.png)

    SELECT * FROM log_in_attempts
    WHERE country NOT LIKE 'MEX%';

---

## 🧑‍💼 Marketing Team in East Office

Queried only employees from the Marketing department in East offices.

![Marketing East Office](https://raw.githubusercontent.com/eldoktor1/SQL-Query-Filters/main/sql_filters_images/sql_page_4_img_1.png)

    SELECT * FROM employees
    WHERE department = 'Marketing'
      AND office LIKE 'East%';

---

## 💼 Finance or Sales Departments

Targeted systems tied to either Finance or Sales employees.

![Finance or Sales](https://raw.githubusercontent.com/eldoktor1/SQL-Query-Filters/main/sql_filters_images/sql_page_4_img_2.png)

    SELECT * FROM employees
    WHERE department = 'Finance'
       OR department = 'Sales';

---

## ✅ Summary

- Used `SELECT` with `WHERE`, `AND`, `OR`, `NOT`, and `LIKE` filters  
- Analyzed time, date, location, and department-based conditions  
- Returned filtered results for investigative and maintenance purposes

---

**Author:** Mina Abskhron  
**GitHub:** [@eldoktor1](https://github.com/eldoktor1)
