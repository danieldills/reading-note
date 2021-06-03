# Mongo and Mongoose

[source](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)

## SQL

1. SQL databases are primarily called as Relational Databases (RDBMS).

1. SQL databases are table based databases whereas NoSQL databases are document based, key-value pairs, graph databases or wide-column stores. This means that SQL databases represent data in form of tables which consists of n number of rows of data

1. SQL databases have predefined schema

1. SQL databases are vertically scalable whereas the NoSQL databases are horizontally scalable. SQL databases are scaled by increasing the horse-power of the hardware

## NoSQL

1. Whereas NoSQL database are primarily called as non-relational or distributed database.

1. Whereas NoSQL databases are the collection of key-value pair, documents, graph databases or wide-column stores which do not have standard schema definitions which it needs to adhered to

1. Whereas NoSQL databases have dynamic schema for unstructured data

1. NoSQL databases are scaled by increasing the databases servers in the pool of resources to reduce the load.

### SQL vs NoSQL Questions

1. What does SQL stand for?
 Structured Query Language

2. What is a realational database?
A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables. In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points. [source](https://www.oracle.com/in/database/what-is-a-relational-database/)

3. What type of structure does a relational database work with?
The relational model means that the logical data structures—the data tables, views, and indexes—are separate from the physical storage structures. This separation means that database administrators can manage physical data storage without affecting access to that data as a logical structure. [source](https://www.oracle.com/database/what-is-a-relational-database/#:~:text=The%20relational%20model%20means%20that,data%20as%20a%20logical%20structure.)

4. What is a ‘schema’?
A Schema in SQL is a collection of database objects associated with a database. The username of a database is called a Schema owner (owner of logically grouped structures of data). Schema always belong to a single database whereas a database can have single or multiple schemas. [source](https://www.edureka.co/blog/schema-in-sql/#schema)

5. What is a NoSQL database?
NoSQL databases (aka "not only SQL") are non tabular, and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph. They provide flexible schemas and scale easily with large amounts of data and high user loads. [source](https://www.mongodb.com/nosql-explained)

6. How does it work?
One way of understanding the appeal of NoSQL databases from a design perspective is to look at how the data models of a SQL and a NoSQL database might look in an oversimplified example using address data. [source](https://www.mongodb.com/nosql-explained)

7. What is inside of a Mongo database?
In MongoDB, data is stored as documents. These documents are stored in MongoDB in JSON (JavaScript Object Notation) format. JSON documents support embedded fields, so related data and lists of data can be stored with the document instead of an external table. [source](https://docs.mongodb.com/guides/server/introduction/)

8. Which is more flexible - SQL or MongoDB? and why.
The core differences between these two database systems are significant. Choosing which one to use is really a question of approach rather than purely a technical decision.

MySQL is a mature relational database system, offering a familiar database environment for experienced IT professionals.

MongoDB is a well-established, non-relational database system offering improved flexibility and horizontal scalability, but at the cost of some safety features of relational databases, such as referential integrity. [source](https://www.mongodb.com/compare/mongodb-mysql)

9. What is the disadvantage of a NoSQL database?

- NoSQL databases don’t have the reliability functions which Relational Databases have (basically don’t support ACID).
  - This also means that NoSQL databases offer consistency in performance and scalability. [source](https://dev.to/lmolivera/everything-you-need-to-know-about-nosql-databases-3o3h#:~:text=separate%20caching%20layer.-,Disadvantages,consistency%20in%20performance%20and%20scalability.)

[<== Back](README.md)
