# Storing Data

These are the different types of data structures and their details:

| Feature              | Structured Data                                                  | Semi-Structured Data                                                                     | Unstructured Data                                                                        |
| :------------------- | :--------------------------------------------------------------- | :--------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------- |
| **Definition**       | Highly organized; follows a rigid, predefined model/schema.      | Has some organizational properties but allows for more flexibility than structured data. | Does not follow a predefined data model or schema; not organized in a predefined manner. |
| **Structure**        | Fixed columns and rows; tabular format.                          | Contains tags or markers to identify elements; variable nature; data can be nested.      | No predefined format; cannot be contained in rows/columns.                               |
| **Search/Organize**  | Easy to search and organize.                                     | Relatively easy to organize and search.                                                  | Difficult to search and organize.                                                        |
| **Relations**        | Easy to form relations; organized in relational databases.       | Can be grouped to form relations, but less straightforward.                              | Not directly applicable to forming relations in a traditional sense.                     |
| **Prevalence**       | About 20% of data.                                               | Increasingly common.                                                                     | Most of the data generated (around 90%).                                                 |
| **Storage**          | Relational databases (e.g., SQL databases, spreadsheets).        | NoSQL databases.                                                                         | Data lakes; can also appear in data warehouses or databases.                             |
| **Query Language**   | SQL (Structured Query Language).                                 | Specialized tools, often leverages JSON/XML capabilities of NoSQL databases.             | Machine learning and AI algorithms for extraction.                                       |
| **Common Formats**   | Tables with rows and columns.                                    | JSON, XML, YAML.                                                                         | Text, sound, pictures, videos, PDFs.                                                     |
| **Example**          | Spotflix employee table (fixed columns like team, role, salary). | Spotflix favorite artists (JSON with varying number of artists per user).                | Spotflix lyrics, songs, album/artist profile pictures, music videos.                     |
| **Value Extraction** | Straightforward.                                                 | Relatively straightforward.                                                              | Challenging until recent advancements in ML/AI.                                          |

---
## SQL Databases

SQL, or Structured Query Language, is the dominant language for interacting with RDBMS (Relational Database Management Systems).  Some common usecases include:

- Access to data in batches
- Grouping, filtering, and aggregating data

Data engineers use SQL for the creation and maintenance of databases, including defining their structure and updating records. Data scientists, on the other hand, primarily use SQL to query (request information from) existing databases for analysis.

```sql
CREATE TABLE employees (
    employee_id INT,               
    first_name VARCHAR(255), 
    last_name VARCHAR(255),       
    role VARCHAR(255),         
    team VARCHAR(255),         
    full_time BOOLEAN,      
    office VARCHAR(255) );
```

Data scientists use SQL to extract specific information. For example, if a data scientist  wants the first and last names of employees whose roles contain the word "data," he would use:

```sql
SELECT first_name, last_name
FROM employees
WHERE role LIKE '%Data%';
```

Databases are composed of multiple interconnected tables, and the database schema defines these relationships. This interconnectedness is why they are called "relational" databases.

---
## Data Warehouses and Lakes

The data pipeline typically involves different storage solutions at various stages. Two key components are data lakes and data warehouses, each serving distinct purposes:

| Feature           | Data Lake                                                  | Data Warehouse                                               |
| :---------------- | :--------------------------------------------------------- | :----------------------------------------------------------- |
| **Data Type**     | Stores all collected **raw data** (structured, semi-structured, unstructured). | Stores **specific, processed data** for a particular use case. |
| **Processing**    | Unprocessed and messy.                                     | Optimized for analytics.                                     |
| **Volume**        | Can store petabytes of data (very large).                  | Relatively smaller (on the scale of big data), stores processed insights. |
| **Schema**        | **No model enforced** on data storage (schema-on-read).    | **Enforces a structured format** (schema-on-write).          |
| **Cost**          | Cost-effective due to lack of enforced structure.          | More costly to manipulate due to structured format.          |
| **Analysis**      | Very difficult to analyze directly. Requires advanced techniques like deep learning for hidden patterns. | Optimized for analytics to drive business decisions.         |
| **Primary Users** | Data scientists (for real-time analytics on big data).     | Analysts (for ad-hoc, read-only queries like aggregation and summarization). |

Given the lack of enforced structure and the ability to store any data type in a data lake, a data catalog becomes essential. It acts as a "source of truth" to compensate for this flexibility, preventing the data lake from becoming a data swamp. A data catalog typically tracks:

*   The origin of the data.
*   How the data is used.
*   Who is responsible for its maintenance.
*   How frequently the data is updated.

Implementing a data catalog is considered good practice for data governance, ensuring data availability, usability, integrity, and security. It also guarantees the reproducibility of processes and analyses, reduces reliance on "tribal knowledge", and makes working with data more scalable by streamlining the process from finding data to preparing it.

---