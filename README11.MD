
# READ 11

## 1. What is a Schema?
A database schema is a visual and logical architecture of a database created on a database management system.

## 2. Why do we use them?

It provides a graphical view of the entire database architecture and structure. It provides a means for logically grouping and displaying database objects such as tables, fields, functions and relations.

## 3. What do they look like?
![Schema](/images/schema.png)


## 4.What is a Primary Key?
A primary key is a field in a table which uniquely identifies each row/record in a database table. Primary keys must contain unique values. A primary key column cannot have NULL values.

A table can have only one primary key, which may consist of single or multiple fields. When multiple fields are used as a primary key, they are called a composite key.

If a table has a primary key defined on any field(s), then you cannot have two records having the same value of that field(s).

## 5.What is a Foreign Key?
A foreign key consists of a column that references another column in another table. This column that is being referred is most often a primary key of the referenced table. The purpose of the foreign key is to ensure referential integrity of the data. In other words, only values that are supposed to appear in the database are permitted.

## 6.What is a Composite Key?
A composite key, in the context of relational databases, is a combination of two or more columns in a table that can be used to uniquely identify each row in the table. Uniqueness is only guaranteed when the columns are combined; when taken individually the columns do not guarantee uniqueness.

## 7. How are they different? When do you use 1 over the others?

A composite key is a set of more than one key that, together, uniquely identifies each record. A foreign key, on the other hand, is a key in some table which uniquely identifies rows in another table – or, in other words, a key that tracks to a primary key in another table. An example would be a list of homes on a real estate market


## 8.What is a 1:1 relationship?
In relational database design, a one-to-one (1:1) relationship exists when zero or one instance of entity A can be associated with zero or one instance of entity B, and zero or one instance of entity B can be associated with zero or one instance of entity A. (abbreviated 1:1

## 9.What is a Many:Many relationship?
In relational database design, a many-to-many (M:N) relationship exists when, for one instance of entity A, there exists zero, one, or many instances of entity B; and for one instance of entity B, there exists zero, one, or many instances of entity A. (abbreviated M:N)

## 10.How about a 1: Many or a Many:1?

 In relational database design, a one-to-one (1:1) relationship exists when zero or one instance of entity A can be associated with zero or one instance of entity B, and zero or one instance of entity B can be associated with zero or one instance of entity A. (abbreviated 1:1)