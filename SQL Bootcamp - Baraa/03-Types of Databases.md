## Types of Databases

The most common type of databases are relational databases. They store data just like spreadsheets store them, using tables made up of rows and columns. These tables act like separate entities and can be linked together, forming relationships among data—hence the name "relational database."

>[!NOTE]
**Example**: A user from the users table can have multiple purchases in the orders table of an e-commerce store's database.

**NoSQL Databases**
All databases except relational databases are called NoSQL databases, which means "Not Only SQL." Relational databases are called SQL databases because they only accept data stored in columns and data is accessed through SQL.

**Key-Value Databases**
Key-value pairs are another type of database that resembles how a dictionary works. Each key has its own value, like how each word in a dictionary has its definition and meaning.

**Column-Based Databases**
Column-based databases are an advanced type of database used to store large amounts of data. As the name suggests, they store data in columns only.

**Graph-Based Databases**
Graph-based databases connect every data point through similar properties and values.

**Document-Based Databases**
Document-based databases are used where the structure of the data isn't important, but fitting related information about an entity on a single document is.

| Database Type   | Database Name              |
| --------------- | -------------------------- |
| SQL Based       | MySQL, Postgres, MSSQL     |
| Graph Based     | Neo4j                      |
| Key-Value Based | Redis, DynamoDB            |
| Column Based    | Apache Cassandra, Redshift |
| Document Based  | MongoDB                    |
![[database_types.png]]

