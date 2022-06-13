## [SOQL vs SQL: Best Practices to Query Salesforce Database](https://skyvia.com/blog/soql-vs-sql-best-practices-to-query-salesforce-database#:~:text=In%20SQL%2C%20the%20data%20is,like%20UPDATE%2C%20INSERT%2C%20etc.)  
`2022.06.13.`
### Main Differences Between SOQL and SQL  
1. In SQL, the data is stored in database tables whereas the data in Salesforce is stored in the form of objects.  
2. SOQL is used primarily for querying the Salesforce database and retrieving the records. It does not allow data modifying statements like `UPDATE`, `INSERT`, etc. To update or insert multiple records in the Salesforce database, it needs to be done using Salesforce's user interface or DML statements.
3. SOQL requires specific fields to be mentioned while querying the salesforce database. It does not permit fetching all the fields at once like `SELECT *` that we can use SQL. The reason behind the same is that the data fetched is stored in a multi-behind the same is that the data fetched is stored in a multi-tenant environment. Such data is generally accessed by and shared with everyone and queries like `SELECT *` are going to become a bottleneck for the environment and cause havoc for the other employees.
4. SOQL JOIN statements are different from those in SQL. in SQL, we can join any database and fields. SOQL does not support or allow arbitary joins. It can only join those objects that are related to each other.   

### Benefits of SOQL over SQL
1. SOQL helps in modeling the data better as the objects can be related to other objects and that can provide a better understanding of the data at hand using Workbench.  
2. SOQL is used to manage the Salesforce data that is accessed by multiple tenants. It allows the users to fetch the data in a non-tolerant manner and restricts the queries that can become a bottleneck to the entire environment.  

### Tips and Good Practices in SOQL
1. **Build selective queries.** A query is said to be selective when the filters used in a query are on an indexed field. This reduces the time and resource consumption to scan the database as it is on an indexed field.  
2. **Avoid the use of NULL keyword and wildcards.** When the null keyword is used in the query, it executes a full database scan. Also, avoid usage of wildcards like `%` as they do not make use of an index.  









