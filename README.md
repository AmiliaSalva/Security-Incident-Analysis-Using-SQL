# Security Incident Investigation: After-Hours Failed Login Attempts Analysis Using SQL

## Introduction

The purpose of this scenario is to assess my proficiency in using SQL for data analysis and problem-solving. It aims to validate my ability to construct SQL queries, apply filters, and retrieve relevant information from a database based on specific criteria.

## Objective 

By simulating a scenario involving data analysis, this exercise evaluates my understanding of SQL syntax, query construction, and data retrieval techniques. It assesses my capability to navigate and query a database effectively, extracting valuable insights and information to address specific requirements or solve problems.

The scenario serves as a practical demonstration of my SQL skills, showcasing my ability to manipulate data, apply filters, and analyze datasets to uncover patterns, anomalies, or other meaningful information. It showcases my competence in utilizing SQL as a versatile tool for querying and analyzing data, enabling me to extract valuable insights and draw informed conclusions.

Overall, this scenario is designed to validate my proficiency in SQL and showcase my ability to leverage its capabilities in various data analysis scenarios, irrespective of the specific details of the scenario itself.

## Scenario

In this scenario, I encountered a potential security incident that took place after business hours. The incident prompted me to initiate an investigation to identify the root cause and assess the impact. To gain deeper insights into the situation, I needed to query the ``log_in_attempts`` table and focus on reviewing the login activity that occurred after the designated closing time of 6 PM.

I used the following query:

```
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = 0;
```
<details close>
  <summary>The Results:</summary>
![SQLQUERY](https://github.com/AmiliaSalva/Security-Incident-Investigation-After-Hours-Failed-Login-Attempts-Analysis-Using-SQL/assets/132176058/c452a1d3-519e-4e6c-a20c-875160576533)
</details>

This query retrieves all columns from the log_in_attempts table where the login time is after 18:00 and the login attempt is unsuccessful (denoted by a value of 0 in the success column). It provides a way to filter and focus on failed login attempts that occurred after the specified time, allowing for further investigation into potential security incidents or anomalies.
