---
tags:
  - ExchangingData
---
---

# What is Relational Database Design?

In a relational database, data is held in tables, also known as relations. 
- One row in the table holds one record
-  Each column represents one attribute
- Each relation should hold data about a single *[[Entities in Databases|Entity]]*

## Example 
A database holds details of gym members and the classes they take.
A first attempt at designing the database might use a *flat file*, holding all the data in one table. 

| MemberID | MsurName | MFirstName | ClassID          | Cname                | Day                 |
| -------- | -------- | ---------- | ---------------- | -------------------- | ------------------- |
| M12      | Sharpe   | Norman     | C100, C103, C114 | Pilates, Zumba, Yoga | Monday, Monday, Wed |
| M13      | Bunn     | Martha     | C100, C115       | Pilates, Cycling     | Monday, Wednesday   |
| M16      | Jones    | Polly      | C103             | Zumba                | Monday              |
| M18      | Jolly    | Brian      | C114             | Yoga                 | Wed                 |

*Table 1: Flat File*

As we can see; this is not very good database design. 

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width=0.5mm] (-2.5,0) -- (2.5, 0);
\draw[line width=0.5mm] (-2,0) -- (-2,1) -- (-1,1) -- (-1,0) --cycle;
\draw[line width=0.5mm] (2,0) -- (2,1) -- (1,1) -- (1,0) --cycle;
\draw[line width=0.5mm, -stealth reversed] (-1, 0.5) -- (1, 0.5);
\draw[line width=0.5mm, -stealth reversed] (1, 0.5) -- (-1, 0.5);
\node[anchor = south] at (0, 0.5) {Enrols on};

\node at (-2.5, 1.5) {Member};
\node at (2.5, 1.5) {Class};

\end{tikzpicture}
\end{document}
```

# Normalisation

Normalisation is a process used to come up with the best possible design for a database. Tables should be organised so that the data *is not duplicated* in the same table, or different tables. 

The structure should allow for complex queries to be made. 

There are three stages in normalisation, called: First, Second and Third Normal form. (\[1-3]NF)

## First Normal Form (1NF)

A table is in first normal form if it contains no repeating attributes or groups of attributes. 

All attributes must be atomic, irreducible - a single attribute cannot consist of two data items such as first name and surname. As this would make it difficult or impossible to sort on surname. 

For instance, *Table 1* would *NOT* be in first normal form, as the table contains repeating groups of attributes. The problem here is that the entities Member and Class are linked in a *many-to-many* relationship. Denoted by the arrow below, that signifies a one to many bijection. 

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width=0.5mm] (0,0) -- (3, 0);
\draw[line width=0.5mm] (3,0.3) -- (2.5, 0);
\draw[line width=0.5mm] (3,-0.3) -- (2.5, 0);

\end{tikzpicture}
\end{document}
```

### Foreign Keys
Foreign Keys are keys that point to another column in another table. The existence of a foreign establishes a *Foreign Key Constraint* - a database rule that ensures that a value can be added or updated in a column; only if the same change is mirrored in the column it points too.

It can be concluded in a way that enrolment tables facilitate foreign keys; and the pointers between them.  Furthermore, the enrolment table consists of two foreign keys, leading to it being given a *"Composite Foreign Key*, which is the enjoinment of the two foreign keys present. 

*tblMember*

| MemberID | MSurname | MFirstName |
| -------- | -------- | ---------- |
| M12      | Sharpe   | Norman     |
| M13      | Bunn     | Martha     |

*tblEnrolment*

| MemberID | ClassID |
| -------- | ------- |
| M12      | C100    |
| M10      | C103    |

*tblClass*

| ClassID | CName   | Day |
| ------- | ------- | --- |
| C100    | Pilates | Mon |
| C103    | Zumba   | Mon |


## Second Normal Form (2NF)
A table is in second normal form (2NF) if it is first normal form and contains no partial dependencies. This can only occur if the primary key is a composite key. 
  
  is the only table with a composite key and it has no fields which are dependent on either part of the key. 

## Third Normal Form (3NF)
A table is in third normal form if it is in second normal form and contains no non-key dependencies. 

*"All attributes give info on the key, the whole key, and nothing but the key"* - *(So help me Cod)*

The advantages of normalisation are that:
 - It is easier to maintain and change a normalised database
 - There is not unnecessary duplication of data 
 - Data integrity is maintatined - if a person changes adress for example, the update needs to be made only once to a single table
 - Having smaller table with fewer fields means faster searches and savings in storage 