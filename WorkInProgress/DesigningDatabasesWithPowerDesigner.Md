## Tutorial: Designing Databases with PowerDesigner

------

###### About this chapter 

SQL Anywhere Studio includes PowerDesigner Physical Architect, a module of Sybase's powerful database design tool, PowerDesigner. This module provides ways to generate and modify databases using a graphical representation of the database structure. You can optimize your database by customizing tables, columns, indexes, referential integrity, views, physical storage, triggers, and stored procedures.

------

[About PowerDesigner](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000071.htm)
[Lesson 1: Getting Started](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000072.htm)
[Lesson 2: Add a column](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000074.htm)
[Lesson 3: Check your work](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000075.htm)
[Lesson 4: Save changes and generate database](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000076.htm)
[Summary](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000077.htm)



### About PowerDesigner

------

The structure of your database, such as the tables, relationships, views and triggers, is called the database **schema**. You use SQL statements to create and arrange these elements to your liking, but doing so without a graphical tool can be confusing.

PowerDesigner gives you a graphical representation of the structure of your database. Better, you can modify the structure of the database or create an entirely new one simply by drawing new tables or entering information. Once your design is complete, PowerDesigner can generate a SQL script to generate your new database.

The following diagram, which displays the structure of the sample database, is easily created using PowerDesigner.

![The Adaptive Server Anywhere sample database schema.](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/gif/asademo.gif)

The performance of your database depends heavily on your design. In general, you should store information about different distinct types of objects, such as employees or products, in separate tables.

You can identify relationships between these tables using references, meaning that foreign keys in one table identify particular rows in another table. Many-to-one and one-to-many relationships can be represented by a reference. Many-to-many relationships require two references and another table.

For more information about database design, see [Designing Your Database](http://dev.cs.ovgu.de/db/sybase9/help/dbugen9/00000008.htm).

For more information about PowerDesigner, click Help in the toolbar of the PowerDesigner main window to access three books: *PowerDesigner General Features Guide*, *PowerDesigner PDM User's Guide*, and *PowerDesigner Report User's Guide*.

For more PowerDesigner tutorials, click Start > Programs > SQL Anywhere 9 > PowerDesigner 8 > PDM Getting Started. This accesses the book *Physical Data Model Getting Started*.



### Lesson 1: Getting Started

------

PowerDesigner can read the structure of a database from a script file that creates the database. However, it is generally easier to just connect to your database from PowerDesigner and let it extract the design directly with the reverse engineering feature.

The following tutorial uses the sample database as a starting point. The tutorial illustrates PowerDesigner by implementing a modification that improves the design of the sample database.

Currently, the price of each product is always read from the product table. As a result, updating the price effectively changes the sale price of that item on all previous orders. Adding a unit_price column to the sales_order_items table will correct this problem. The actual selling price to each customer can now be stored separately. The price in the product table records the current list price.

To start PowerDesigner

1. From the Start menu, choose Programs > SQL Anywhere 9 > PowerDesigner 8 > PowerDesigner.

   The PowerDesigner main window appears:

   

   The PowerDesigner main window includes an object browser docked to the left, and an output window docked at the bottom.

2. Choose File > New.

3. In the New Dialog, choose Physical Data Model and click OK.

   The Choose DBMS dialog appears.

4. From the dropdown list, choose Sybase AS Anywhere 9.

5. Ensure Link is selected and click OK.

   The model name MODL_1 appears in the browser and in the title bar.



### Lesson 2: Add a column

------

You are now ready to add the unit_price column to the sales_order_items table. You can accomplish this task by accessing the list of columns through the Table property sheet.

To add a column

1. Display the column properties:

   - Right-click the sales_order_items table and select Properties from the popup menu.

     The Table property sheet appears:

     

   - Click the Columns tab.

     The list of columns appears:

     

2. Add a new column to hold the unit price.

   - Click the Insert a Row tool.

     An arrow appears at the beginning of the line and a column with a default name (Column_6) appears.

   - Type **unit_price** in the name column. The name is automatically duplicated as the code.

   - From the Data dropdown list, choose Numeric. (The Data field may be too narrow to read. You can pull the sides of the column to expand it.)

   - The column properties P, F, and M stand for Primary Key, Foreign Key, and Mandatory, as follows:

     - Primary key designates a column whose values uniquely identify a row in the table.
     - Foreign key designates a column that depends on and migrates from a primary key column in another table.
     - Mandatory indicates a column that must be assigned a value.

   - Select Mandatory and click OK.

3. Examine the effect of your changes on the diagram of the database. The sales_order_items table now includes a new column called unit_price.



### Lesson 3: Check your work

------

PowerDesigner lets you quickly detect database design errors in your new model.

To check your new schema

1. Choose Tools > Check Model.

   The Check Model Parameters dialog appears. You can use the default parameters.

2. Click OK.

   The results of Check Model appear in the Results List.



### Lesson 4: Save changes and generate database

------

In PowerDesigner, models that depict the physical components of your database design, including tables and columns, are called **Physical Data Models** (**PDM**). PowerDesigner stores these in files with the extension *.PDM*.

To save the physical data model (PDM)

1. Choose File > Save As.
2. Type a file name with the extension *.PDM* and select a location.
3. Click OK.

You can use PowerDesigner to generate a SQL script that implements all the components of your model. You can then use the SQL script to generate a database.

To generate a SQL script to create your new database

1. Choose Database > Generate Database.

   The Database Generation dialog appears:

   

2. Type **NewDemo.SQL** in the File Name box and choose a convenient directory.

3. Ensure that Script Generation is selected.

4. Click the Database tab, and ensure that Create Database is selected.

   Explore the other tabs to observe options that give you control over many other properties of the generated script.

5. Click OK.

   When the script is created, the Result dialog appears.

6. Click Edit to view the script.

   Check that your changes are reflected in the script. For example, the definition of the new office table appears below.

   ```
   /* ========================================= */
   /*   Table: office                           */
   /* ========================================= */
   create table office
   (
      id            integer         not null
         default autoincrement
         check (
            id >= 100),
      name          char(15)        not null,
      street        char(30)        not null,
      city          char(20)        not null,
      state         char(2)         not null,
      zip           char(5)         not null,
      phone         char(10)                ,
      fax           char(10)                ,
      primary key (id)
   );
   ```

7. When you are finished, close the dialog: in the Result dialog, click Close.

You can now create your new database from Interactive SQL.

To create the new database

1. Start Interactive SQL.

2. Connect to the sample database. You can use the same ODBC connection.

3. Create an empty database:

   - Execute the following SQL statement, substituting any convenient directory.

     ```
     CREATE DATABASE 'c:\\My Scripts\\newdemo.db'
     ```

     Tip To execute a SQL statement in Interactive SQL, type or copy the statement in the SQL Statements pane, and then press F5, *or* choose SQL > Execute.

4. Close the connection to the sample database by clicking SQL > Disconnect.

5. Connect to the new database by clicking SQL > Connect.

   - Enter **DBA** as the User ID
   - Enter **SQL** as the Password
   - Click the Database tab, and in the Database File box, enter the full path and file name of the new database file.
   - Click OK.

6. Use the read statement. Remember that this statement demands that you enclose the file name in double quotes.

   - Execute the SQL statement:

     ```
     READ "c:\\My Scripts\\newdemo.SQL"
     ```

You can use these basic steps to modify other databases.



### Summary

------

This tutorial introduced only some of the basic features of PowerDesigner. In fact, it is capable of handling the complete design or modification of your database schema, including all tables, views, indexes, references, triggers, and procedures.

###### Domains 

Other features greatly simplify the task of designing larger databases. For example, you can specify specific **domains**. A domain holds a particular type of data, such as a phone number. It has a data type associated with it, but is more specific. For example, you can create a domain of identification numbers. Whenever you need an identification number in a table, you can associate that column with the identification number domain. All properties and checks associated with that domain are attached automatically.

Domains reduce repetitive definitions. In doing so, they not only reduce your work, but also reduce the chance that you will erroneously use a different type definition or check procedure. Rather than identify a column as simply an integer, you specify what specific type of data that column contains. All instances of that data type share a common definition.

###### Business rules 

A business rule is a written expression of the way a business operates. For example, *the order shipped date must be greater than or equal to the order date* is a business rule.

Business rules fall into four categories:

- **Definition**  Expresses inherent properties of an object. Definitions typically describe entities.
- **Fact**  Expresses certainty or existence. Facts typically describe relationships.
- **Validation**  A constraint on a value.
- **Formula**  Calculation used to produce values.

Business rules are particularly handy because they relate directly to the task that a customer requires that a database perform. By recording business rules and attaching them to particular objects, you can ensure that a database performs the required tasks.

------

[Where do I go from here?](http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000078.htm)



http://dev.cs.ovgu.de/db/sybase9/help/dbfgen9/00000070.htm