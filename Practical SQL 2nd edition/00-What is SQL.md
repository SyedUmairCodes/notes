# Introduction
SQL (Structured Query Language) is a programming language used for managing data in database systems. It's particularly useful for relational databases, where data is organized into tables with rows and columns.

>[!NOTE]
>SQL allows users to collect, modify, explore, and summarize data.It enables tasks like storing, updating, deleting, searching, and retrieving information.

SQL serves two primary functions: it's a language for defining the structures that hold data (like tables and their relationships), and it's for extracting (querying) that data. The fundamental structure in a relational database is the table, a grid of rows and columns.

SQL is a mature language, developed in the 1970s, and remains one of the most widely used computer languages globally. First outlined as SEQUEL in a 1974 paper by IBM researchers, building on Edgar F. Codd's theoretical work. In 1979, Oracle (then Relational Software) was the first to use it commercially. Standardized by the American National Standards Institute (ANSI) in 1986 and the International Organization for Standardization (ISO) in 1987.

## SQL Standards and Dialects

Each database system (e.g., PostgreSQL, MySQL, Microsoft SQL Server) implements its own variant of SQL, leading to syntax differences. The ANSI/ISO SQL standard doesn't cover all aspects required for a database implementation (e.g., creating indexes), leaving vendors to implement features as they see fit.

>[!NOTE]
>Commercial vendors create nonstandard features for competitive advantage and to keep users within their ecosystem.
>

Transact-SQL or T-SQL is Microsoft's proprietary extension to SQL, used with SQL Server. Includes features not in the standard, such as syntax for declaring local variables, control-of-flow constructs (IF, WHILE), and enhanced DELETE and UPDATE statements. that make migrating code written in T-SQL to another database system challenging.

>[!IMPORTANT]
While there are variations, most SQL database programs support major commands ( e.g., SELECT, UPDATE, DELETE, INSERT, WHERE) in a similar manner to be ANSI compliant.

---
# Databases and Spreadsheets

While many users begin data analysis with tools like Microsoft Excel and Access, these often present significant limitations. Excel, for instance, has a hard limit of 1,048,576 rows per worksheet. Similarly, Access restricts database size to 2 gigabytes and table columns to 255. Datasets frequently surpass these constraints, and encountering such capacity issues when facing a deadline can be a major impediment.

SQL database systems offer substantial advantages. They can manage massive amounts of data, often in terabytes, and handle complex structures involving multiple related tables and thousands of columns. This provides fine-grained control over data structure, leading to improved efficiency, speed, and crucially, accuracy in data management.

SQL also serves as an excellent complement to programming languages widely used in data science, such as R and Python. Users can directly connect to SQL databases from these languages, and in some instances, even embed SQL syntax directly into their code, streamlining data interaction.

>[!NOTE]
>SQL extends far beyond mere data analysis. It forms the backend power for numerous online applications, including common web frameworks like Django, interactive mapping (GIS) applications, and content management systems such as WordPress.
