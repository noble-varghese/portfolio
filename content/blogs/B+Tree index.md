---
title: Unlock Faster Data Access with B+ Tree Indexing - A Beginner’s Guide.
type: page
## description: Click on me to see the content.
topic: career
author: Noble Varghese
---

![](https://noble-varghese.github.io/portfolio/images/b_tree_img1.jpeg)

If you’re someone who writes or have written SQL queries, then you would have heard of the term **“indexing”**. This is a standard technique used by the DBAs or Backend Engineers in order to improve the performance of a query operation.

Today, let us dive deeper into why & where B+ tree indexes are used, when to use a B+ tree index and how it improves the query performance.

## 🔎 What is a B+ tree index ?

![](https://noble-varghese.github.io/portfolio/images/Btree.jpeg)

It is a variation of the b-tree data structure. The leaf node in a B+ tree index store the pointers to the actual page values and internal nodes contain the page. Hence, the structure of the internal node is different from that of the leaf nodes. The leaf nodes are a doubly linked list and helps in the sequential search of values. Whereas the internal nodes are used to guide the search to the right node. Every internal node contains the pointer to the location of the next node and the key-value of the range that child node supports and the leaf nodes contain the pointer to the location of the value on the disk.

### Characteristics:

-   Data records are only stored in leaves.
-   Internal nodes store just keys and pointers to child nodes.
-   All the leaf nodes remain at the same height.
-   The leaf nodes are linked using a linked list.
-   B+ Tree can store a lot more data than a B-Tree.
-   These are self-balancing trees.

## 🔎 Why B+ Tree index ?

A B+ tree index speeds up the data access as the storage engine doesn’t have to scan the whole table to find the desired data. The concept behind the B+ Tree index is called multi-level indexing. It is a multiway tree with some rules as to how the tree is built. Binary tree for example is an implementation of a multiway tree with 2 child nodes for every node.

The root node in a B+ tree contains the pointer to the child nodes. The storage engine determines the right node by checking the values in the node pages which contain the upper and lower bounds of the values on the child nodes. Finally the storage engine either gets to the node page with the right value or concludes that the value doesn’t exist on the database.

## 🔎 Common scenarios of B+ Tree index

B+ Tree indexes work well in scenarios where lookups are done on full key value(exact match queries), prefix search(Starts with kind of queries) and key range search(lies between kind of queries).

-   **Full value match**: For example in scenarios where you search for a student named “Marcus Goldman” who was born on 01–09–1998.
-   **Prefix search:** Prefix search is useful only if the lookup uses a **leftmost prefix** of the index. For example, search for all students whose last name starts with “N” or all students with last name as “Robert”.
-   **Range query:** Find all the students with last names between “Albert” and “Zendaya”.
-   **Combination of prefix match and range query:** This is useful in cases where the first half of the query is a prefix match and second is a range query. For example, in order to find all the students with last name as “Marcus” and first name starts with “A”.

Since the tree is already sorted, it is useful for lookups described in the above scenarios as well as ordering of the results using an ORDER BY query.

## 🔎 Limitations of B+ Tree index

B+ Tree index is not useful if the lookup does not start from the leftmost side of the indexed columns, i.e

-   B+ tree index is not useful if the lookup is to find all the students’ named “Brian” or students born on a certain date or students whose last name is “Brownie”. This is an example of rightmost side of the indexed column search.
-   The storage engine can’t optimise accesses with any columns to the right of the first range condition. If your query is WHERE last_name=“Smith” AND first_name LIKE ‘J%’ AND dob=“1976–12–23”, the index access will use only the first two columns in the index, because the LIKE is a range condition (the server can use the rest of the columns for other purposes, though).

## 🔎 **Advantages of B+Trees**

-   B+ Tree index is incredibly fast for search operations as it stores more entries in its internal node when compared to the B-Tree index. This means more records for the same “n” levels of the tree. Hence, it can get to the results in a lesser number of hops (as each level is considered an I/O operation to the disk). To put it in perspective, it can store upto256 Terabytes of records in 3–4 levels assuming each node can store 4Kb of max data.
-   Data stored in B+ tree can be accessed both sequentially and directly. The B+ tree retains the rapid random access property of the B-tree while also allowing rapid sequential access.

## 🔎 B+ Tree Applications

-   Multilevel Indexing
-   Faster operations on the tree (insertion, deletion, search)
-   Database indexing