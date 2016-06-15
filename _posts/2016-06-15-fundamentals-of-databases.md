---
published: true
---
A **relational database** is a database using tables of related data that is only stored once. Instead of repeating data, numerical links are made between them so the data isn't repeated.

An **entity** is an individual thing about which data is stored.

An **attribute** is a piece of information about an entity stored as a field in a relational database. There are several kinds of attribute:

+ A **primary key** is a kind of attribute that uniquely identifies each individual record.
+ A **composite primary key** is a combination of attributes that uniquely identify each record.
+ A **foreign key** is a primary key from another table.

**Reference integrity** is how if a primary key appears in one table it must appear in another.

A normalised database will either have a one-to-one, or a one-to-many relationship. Normalising database creates 

# Representing relationships
Crow's feet are used to imply 'many' in this kind of diagram.

![Many to many](http://www.teach-ict.com/as_a2_ict_new/ocr/A2_G063/331_systems_cycle/analysis_tools/miniweb/images/er_many_to_many.gif)
![One to many](http://www.teach-ict.com/as_a2_ict_new/ocr/A2_G063/331_systems_cycle/analysis_tools/miniweb/images/er_one_to_many.gif)
![One to one](http://www.teach-ict.com/as_a2_ict_new/ocr/A2_G063/331_systems_cycle/analysis_tools/miniweb/images/er_one_to_one.gif)