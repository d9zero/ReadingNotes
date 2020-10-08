# Class 14a - DATABASE NORMALIZATION


## Navigation ##
 - [class 01](class-01.md)
 - [class 02](class-02.md)
 - [class 03](class-03.md) 
 - [class 04](class-04.md)
 - [class 05](class-05.md)
 - [class 06](class-06.md)
 - [class 07](class-07.md)
 - [class 08](class-08.md)
 - [class 09](class-09.md) 
 - [class 10](class-10.md)
 - [class 11](class-11.md)
 - [class 12](class-12.md)
 - [class 13](class-13.md)
 - [class 14a](class-14a.md)
 - [class 14b](class-14b.md)
 - [class 15](class-15.md)
 - [class 16](class-16.md)
 - [class 17](class-17.md)
 - [class 18](class-18.md)

## Reading
[Essential: Database Normalization Explained in Simple English](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)

### Introduction to Database Normalization

### Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included. Take a spreadsheet containing the information as an example, where the data contains salespeople and customers serving several purposes:


        Identify salespeople in your organization
        List all customers your company calls upon to sell a product
        Identify which salespeople call on specific customers.


As you apply these rules, new tables are formed. The progression from unruly to optimized passes through several normal forms.


## Reasons for Database Normalization

The first is to minimize duplicate data

The second is to minimize or avoid data modification issues

The third is to simplify queries

## Data Duplication and Modification Anomalies

        It increases storage and decrease performance.
        It becomes more difficult to maintain data changes.

## Search and Sort Issues

      SELECT SalesOffice
      FROM SalesStaff
      WHERE Customer1 = ‘Ford’ OR
            Customer2 = ‘Ford’ OR
            Customer3 = ‘Ford’

