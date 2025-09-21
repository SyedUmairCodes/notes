You can create a new database using a simple SQL command:

```sql
CREATE DATABASE analysis;
```

This statement uses the keywords `CREATE` and `DATABASE`, followed by the desired database name (`analysis`).

> [!TIP]
> All PostgreSQL statements must end with a semicolon (`;`), adhering to the ANSI SQL standard, making it a good habit to form.

## Defining Table Structure

When creating a table, you must name each column and assign it a specific data type. This data type dictates the kind of values the column will accept. This is how SQL enforces data integrity. For example, a `date` column will reject non-date inputs like "peach," ensuring data consistency and accuracy.

Data stored in tables is then ready to be accessed, analyzed, and manipulated using SQL queries. You can sort, edit, view, and even alter the table's structure later if your data needs evolve.

```sql
CREATE TABLE teachers (
    id BIGSERIAL PRIMARY KEY,
    first_name VARCHAR(25) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    school VARCHAR(100) NOT NULL,
    hire_date DATE NOT NULL CHECK (hire_date <= CURRENT_DATE),
    salary NUMERIC(10, 2) NOT NULL CHECK (salary >= 0)
);
```

To add data into a table in SQL, you use the `INSERT INTO` statement. This statement allows you to specify which table you want to add data to, which columns you want to populate, and the values you want to insert into those columns.

```sql
INSERT INTO teachers (first_name, last_name, school, hire_date, salary)
VALUES ('Janet', 'Smith', 'F.D. Roosevelt HS', '2011-10-30', 36200);
```

## Working with existing databases

To grasp a new database, begin by examining its tables. Look at their names for clues about their content and inspect the column structures to see data types (text, numbers, or both). Note the number of rows to gauge data volume.

Each row in a table represents a record, while each column holds data of a specific type (e.g., numbers, text, dates). SQL is used to set up this structure, define how tables relate to each other, and, of course, retrieve information from them.

Next, observe the total number of tables. Simple databases might have just one, while complex applications can have hundreds. The table count indicates the amount of data to analyze and suggests the importance of exploring relationships between these tables.

> [!NOTE]
> Database designers commonly use separate tables for distinct "entities" (e.g., customers, products) to minimize redundant data.

## Clean SQL Statements

While SQL technically doesn't enforce any specific formatting for its code to execute, adopting a consistent and readable style is crucial for collaboration and long-term maintainability. Therefore, certain generally accepted conventions are highly recommended.

One key convention is to uppercase SQL keywords , such as `SELECT`, `FROM`, `WHERE`, `INSERT`, `CREATE`, and `TABLE`. Some developers also extend this practice to data type names like `TEXT` or `INTEGER`. The choice for data types is ultimately a matter of preference or team standard.

> [!NOTE]
> For naming database objects like tables and columns, it's best to avoid camel case and use lowercase characters separated by underscores.

It's standard practice to indent clauses and code blocks. This means using either two or four spaces to indent lines of code that are part of a larger statement or block. This visual hierarchy helps to quickly discern the structure and flow of a query.

---
