---
tags:
  - ExchangingData
---
---
# What is an Entity?

An entity is defined as an element in a database, it can be narrowed down to 

Some examples of entities include:
- Customer
- Guide or Product
- Subscription

Other entities that could be considered include: customer order, subject, author (of a revision guide). (In the case of the revision guide example).

# Entity Description Format

Consider a database system for managing subscriptions to a set of revision guides, the table for this database could be called RevisionSubs.

Each entity in the database has its respective attributes. The descriptions for these entities can be written in the following format: 

*Customer (<u>custID</u>, title, firstname, surname, email)*
*Product (<u>productID</u>, title, subject, level, price)*
*Subsription (<u>subID</u>, startDate)*

Each entity needs an *identifier* which uniquely identifies a particular record. In a relational database, the identifier is known as the primary key. It is *underlined* in the entity description.

If there is no natural attribute for a primary key, one should be introduced. 

# Keys 
## Composite Primary Key

Sometimes two or even more attributes are needed to uniquely defined a record. For example, in a customer order consisting of many different order lines, each order line may be uniquely identified by two attributes, *orderNumber* and *orderLine*.
OrderLine (<u>OrderNumber</u>, <u>OrderLine</u>, ProductID, ...)
<u>OrderNumber</u>, <u>OrderLine</u> is a *composite primary key*. 

## Secondary Key

The primary key field is automatically indexed so that any particular record can be found very quickly; in some databases, searches may often need to be made on other fields. In the product table, 
Product (<u>productID</u>, title, subject, level, price)
If searches often need to be made on title or subject, either or both of these fields could be defined as a *secondary key*.

These may also be indexed for faster queries. 

# Entity Relationship Diagrams

An entity relationship (E-R) diagram is a graphical way of representing the relationships between entities. 

```tikz
\usepackage{amsfonts}
\begin{document}
\begin{tikzpicture}[domain=0:4]

\draw[line width = 0.7mm] (-1, -2) rectangle (-5,0);
\draw[line width = 0.7mm] (1, -2) rectangle (5,0);

\draw[line width = 0.7mm] (-1,-1) -- (1,-1);


\draw[line width = 0.7mm] (-1, -5) rectangle (-5,-3);
\draw[line width = 0.7mm] (1, -5) rectangle (5,-3);
\draw[line width = 0.7mm] (-1,-4) -- (1,-4);

\draw[line width = 0.7mm] (0.5, -4) -- (1, -3.5);
\draw[line width = 0.7mm] (0.5, -4) -- (1, -4.5);

\draw[line width = 0.7mm] (-1, -8) rectangle (-5,-6);
\draw[line width = 0.7mm] (1, -8) rectangle (5,-6);
\draw[line width = 0.7mm] (-1,-7) -- (1,-7);

\draw[line width = 0.7mm] (0.5, -7) -- (1, -7.5);
\draw[line width = 0.7mm] (0.5, -7) -- (1, -6.5);

\draw[line width = 0.7mm] (-0.5, -7) -- (-1, -7.5);
\draw[line width = 0.7mm] (-0.5, -7) -- (-1, -6.5);

\node[anchor = south] at (0, 0) {One-One};
\node[anchor = south] at (0, -3) {One-Many};
\node[anchor = south] at (0, -6) {Many-Many};

\end{tikzpicture}
\end{document}
```
