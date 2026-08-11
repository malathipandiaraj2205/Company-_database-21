# Company-_database-21
## Company database using SQL:


## Company Database Introduction

● A Company Database is used to store and manage company-related information.

● It organizes data in a structured format using tables.

● It helps maintain employee, department, project, customer, and order records.

● It reduces manual paperwork and improves data accuracy.

● It allows quick retrieval and updating of information.

● It supports multiple users accessing data simultaneously.

● It ensures data security, integrity, and consistency.

● It helps generate reports for business analysis and decision-making.

● It improves productivity and operational efficiency.

● It is widely used in HR, Finance, Sales, Marketing, and Project Management departments.

● The database consists of related tables connected through primary keys and foreign keys.



## Key Objectives of Company Database

1.Centralize Company Data – Store employee, department, customer, project, and order information in a single database.

2.Manage Employee Records – Maintain employee details such as personal information, job roles, salaries, and department assignments.

3.Organize Departments and Projects – Track department information and manage project allocation for employees.

4.Manage Customer and Order Details – Store customer information and monitor order transactions efficiently.

5.Improve Data Accuracy and Security – Reduce data redundancy, maintain data integrity, and ensure secure access to company information.

6.Generate Reports and Business Insights – Provide reports on employee performance, departmental activities, project status, sales, and customer orders to support decision-making.


## Uses of Company Database Project

1.Employee Management – Stores and manages employee details, job roles, salaries, and department information.

2.Department Management – Organizes departments and tracks employees assigned to each department.

3.Project Management – Maintains project details and monitors employee project assignments.

4.Customer Management – Stores customer information, contact details, and business records.

5.Order Management – Tracks customer orders, order dates, and transaction details.

6.Report Generation – Generates reports on employees, departments, projects, customers, and orders.

7.Data Analysis – Helps management analyze business performance and make informed decisions.

8.Data Security – Ensures secure storage and controlled access to company information.

9.Improved Efficiency – Reduces manual record-keeping and increases operational efficiency.

10.Decision Support – Provides accurate and up-to-date information for business planning and management.


## QUERIES CLASSIFICATION:

1.## Simple Queries:
  
 	    	 SELECT, WHERE, ORDER BY
     
2.## Intermediate Queries: 

	      	GROUP BY, HAVING, LIMITS, JOINS
    
3.## Advanced Queries: 

		     CTE, Sub query, Window function ,
		     Functions , Store procedures, Views

			 
	## SCHEMA- STAR SCHEMA –COMPANY DATABASE:			
                    +------------------+
                    |   Departments    |
                    +------------------+
                    | DepartmentID (PK)|
                    | DepartmentName   |
                    +------------------+
                            |
                            |
                            v

+------------------+   +------------------+   +------------------+
|    Customers     |   |    Employees     |   |     Projects     |
+------------------+   +------------------+   +------------------+
| CustomerID (PK)  |   | EmployeeID (PK)  |   | ProjectID (PK)   |
| CustomerName     |   | FirstName        |   | ProjectName      |
| City             |   | LastName         |   | StartDate        |
| Phone            |   | Salary           |   | EndDate          |
+------------------+   | DepartmentID(FK)|   +------------------+
          |            +------------------+            |
          |                     |                       |
          |                     |                       |
          v                     v                       v

                  +--------------------------------+
                  |      FACT_COMPANY_DATA         |
                  +--------------------------------+
                  | EmployeeID (FK)               |
                  | DepartmentID (FK)             |
                  | CustomerID (FK)               |
                  | ProjectID (FK)                |
                  | OrderID                       |
                  | OrderAmount                   |
                  | Salary                        |
                  +--------------------------------+
                               ^
                               |
                               |

                     +------------------+
                     |      Orders      |
                     +------------------+
                     | OrderID (PK)     |
                     | CustomerID (FK)  |
                     | OrderDate        |
                     | OrderAmount      |
                     +------------------+
			 

