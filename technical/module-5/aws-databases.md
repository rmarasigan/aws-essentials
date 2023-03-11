# Databases on AWS

### History behind enterprise databases
Choosing a database used to be a straightforward decision. Customers had only a few options to choose among. Typically, they would consider a few vendors and then inevitably chose one for all their applications. Businesses often selected a database technology before they fully understood their use case. Since the 1970s, the database type most commonly selected by businesses was a relational database.

## Relational databases
A **relational database** organizes data into tables. Data in one table can be linked to data in other tables to create relationships – hence, the relational part of the name.

A table stores data in rows and columns. A row, often called a record, contains all information about a specific entry. Columns describe attributes of an entry. Here’s an example of three tables in a relational database.

![databases-aws](../assets/img/databases-aws.png)

This shows a table for books, a table for sales, and a table for authors. In the books table, each row includes the book ISBN, title, author, and format. Each of these attributes is stored in its own column. The books table has something in common with the other two tables – the author attribute. That common column creates a relationship between the tables.

The tables, rows, columns, and relationships between them is referred to as a logical schema. With relational databases, a schema is fixed. Once the database is operational, it becomes difficult to change the schema. This requires most of the data modeling to be done upfront before the database is active.

### Relational database management system
A **relational database management system (RDBMS)** lets you create, update, and administer a relational database. Here are some common examples of relational database management systems:
* MySQL
* PostgresQL
* Oracle
* SQL server
* Amazon Aurora

You communicate with an RDBMS by using *Structured Query Language (SQL)* queries, similar to the following example:

```sql
SELECT * FROM table_name.
```

This query selects all the data from a particular table. However, the real power of SQL queries is in creating more complex queries that help you pull data from several tables to piece together patterns and answers to business problems. For example, querying the sales table and the book table together to see sales in relation to an author’s books. This is made possible by a join.

### Relational database benefits
Relational database offer a number of benefits, including the following:
* **Joins**: You can join tables, enabling you to better understand relationships between your data.
* **Reduced redundancy**: You can store data in one table and reference it from other tables instead of saving the same data in different places.
* **Familiarity**: Relational databases have been a popular choice since the 1970s. Due to this popularity, technical professionals often have familiarity and experience with this type of database.
* **Accuracy**: Relational databases ensure that your data is persisted with high integrity and adheres to the atomicity, consistency, isolation, durability (ACID) principle.

### Relational database use cases
Much of the world runs on relational databases. In fact, they’re at the core of many mission-critical applications, some of which you might use in your day-to-day life. Here are some common use cases for relational databases.
* Applications that have a solid schema that doesn’t change often, such as lift-and-shift applications that lift an app from on-premises and shifts it to the cloud, with little or no modifications.
* Applications that need persistent storage that follow the ACID principle, such as:
  * Enterprise resource planning (ERP) applications
  * Customer relationship management (CRM) applications
  * Commerce and financial applications

## Choose between unmanaged and managed databases
If you want to run a relational database on AWS, you first need to select how you want to run it – managed or unmanaged. The paradigm of managed versus unmanaged services is similar to the shared responsibility model. The shared responsibility model distinguishes between AWS security responsibilities and the customer’s security responsibilities. Similarly, managed versus unmanaged can be understood as a tradeoff between convenience and control.

### On-premises database
If you operate a relational database on-premises (in your own data center), you are responsible for all aspects of operation, including the data center's security and electricity, the host machine's management, database management, query optimization, and customer data management. You are responsible for absolutely everything, which means you have control over absolutely everything.

### Unmanaged database

![unmanaged-database](../assets/img/unmanaged-database.png)

Now, suppose you want to shift some of the work to AWS by running your relational database on Amazon EC2. If you host a database on Amazon EC2, AWS takes care of implementing and maintaining the physical infrastructure and hardware, and installing the operating system of the EC2 instance. However, you would still be responsible for managing the EC2 instance, managing the database on that host, optimizing queries, and managing customer data.

This is referred to as an unmanaged database option. In this option, AWS is responsible for and has control over the hardware and underlying infrastructure, and you are responsible and have control over management of the host and database.

### Managed database

![managed-database](../assets/img/managed-database.jpg)

To shift more of the work to AWS, you can use a managed database service. These services provide the setup of both the EC2 instance and the database, and they provide systems for high availability, scalability, patching, and backups. However, in this model, you’re still responsible for database tuning, query optimization, and of course, ensuring that your customer data is secure. This option provides the ultimate convenience but the least amount of control compared to the two previous options.

## Resources 
* [What Is a Relational Database?](https://aws.amazon.com/relational-database/)
* [Databases on AWS](https://aws.amazon.com/products/databases/)