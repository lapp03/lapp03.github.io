---
title: "Tips for Using SQL"
output:
  html_document:  
    keep_md: true
    toc: true
    toc_float: true
    code_folding: hide
    fig_height: 6
    fig_width: 12
    fig_align: 'center'
    theme: 'journal'
    css: styles.css
---

During my senior project, I had to remember and brush up some concepts of SQL. I want to use this blog entry as way to summarize the tricks I learned and as way to consolidate my learning of SQL. I hope it helps you learn or remember a few key concepts as well!

<center>

![](post5-1.jpg)

</center>

## Use Appropriate Names 

As data scientists who know how to program, we must get used to correctly naming each variable, method, class, and of course tables and other database elements. It could be a good practice to prefix everything we name in the database. It can be like this:

tbl for tables. Example, tblProducts.
vw for views. Example, vwProducts.
fn for functions. Example, fnProducts.
sp for stored procedures. Example, spProductos.
ix for indices. Example, ixProducts.

## ISNULL

ISNULL is a very useful function whose purpose is to substitute the value of a field when it is null. For example, suppose we are going to look in a table for the information of the products of an online store. The price of the product must always be numerical. But what happens when a value has not yet been assigned to the price of the product? The value it would return would be NULL. If we do not have code that is prepared to receive this type of data, it will cause our system to explode and generate exceptions. The ISNULL function is useful for this.

## Filter Using Aggregated Functions 

There are occasions where we need to filter the results of a query by the result of an aggregate function (count, sum, max, min, avg, etc). For this we can use the HAVING clause.

## Case When

The case when clause can be compared to if-then-else or switches in other programming languages. It is one of the ways to put conditionals in the queries that we write


