# SQL-LAB

## Objective

The objective of this project is to demonstrate the application of SQL queries with filters to enhance the organization's system security. By using operators such as AND, OR, NOT, and LIKE, the queries help identify potential security incidents, optimize employee machine updates, and investigate suspicious login attempts. This process contributes to the integrity and protection of the company's data, ensuring that only relevant information is accessed and analyzed efficiently.

### Skills Learned

- **Data filtering**: By using specific operators I can search for data according to my needs.
- **IT Asset Management**: ​​Identify employee devices for security updates.
- **Access and Authentication Monitoring**: Analysis of login attempts to detect unauthorized access.
- **Data-Driven Decision Making**: Using information obtained through consultations for corrective actions.
- **Process Optimization** – Use of filters to reduce analysis time and make investigation more efficient.

## Project Description

My organization is working to make its system more secure. It is my job to ensure that the system is secure, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.

## Steps

### Identifying Failed Login Attempts Outside Business Hours

A potential security incident took place after business hours (post 6:00 PM). It is necessary to investigate all failed login attempts that occurred during this period.  

The following code illustrates how I designed an SQL query to filter and retrieve failed login attempts made after business hours.

![image](https://github.com/user-attachments/assets/f5f75bec-9871-45c6-8cdf-82f0b001d738)

The first part of the screenshot shows my query, while the second part displays a portion of the output. This query filters failed login attempts that occurred after 6:00 PM. I began by selecting all data from the **log_in_attempts** table. Then, I applied a **WHERE** clause with an **AND** operator to refine the results, ensuring that only login attempts made after 6:00 PM and unsuccessful ones were retrieved. The first condition, **login_time > '18:00'**, filters attempts occurring after 6:00 PM, while the second condition, **success = FALSE**, isolates the failed login attempts.

### Retrieve login attempts on specific dates

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.

The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.

![image](https://github.com/user-attachments/assets/25f5de65-7969-417d-baf9-205a718e6122)

The first part of the screenshot shows my query, while the second part displays a portion of the output. This query retrieves all login attempts that took place on either 2022-05-09 or 2022-05-08. I started by selecting all data from the **log_in_attempts** table. Then, I applied a **WHERE** clause with an **OR** operator to filter the results, ensuring only login attempts from these specific dates were returned. The first condition, **login_date = '2022-05-09'**, filters logins from May 9, 2022, while the second condition, **login_date = '2022-05-08'**, filters those from May 8, 2022.
