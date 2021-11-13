# Project 1: Segment Analysis through SQL

# Overview
In this project, I designed and created a database similar to what a simplified corporate ERP might be. I wanted to segment customers by distribution channel and extrapolate business data.

With this project I wanted to demonstrate my ability to:
- Understand the logic of a database
- Use basic and intermediate commands to extract data from a database

The tools I used for the project are PostgresSQL and Excel.

# Objectives of the project

The two main goals I wanted to bring home with this project were:
- Create a structured database like what a corporate ERP can be
- Solve real questions that may be in an enterprise

More specifically, the database and the queries I have created should segment customers and report margins by customer, distribution channel and single product.

# Phases of the project

## 1. Thinking about the infostructure

Thinking about how to structure the database tables I wanted to replicate the back-end of an ERP software.

The tables I created are the following
- (i) Suppliers
- (ii) Raw materials
- (iii) Products
- (iv) Rows invoices
- (v) Invoices
- (vi) Clients
- (vii) Distribution channels

## 2. Create tables

The complex part in thinking about how to structure the database concerns the minimization of redundant data in the various tables and the effectiveness of the data in the database when it will be interrogated with queries.

## 3. Importing the data through csv file 

To be faster and to experiment with the import/export features of PostgreSQL, I first populated the tables in Excel sheets and then they were massively imported into the tables created earlier in PostgreSQL.

## 4. Thinking about business questions

Customer segmentation has always been the main purpose of the project, so the key question is: (a) what is the operating margin by distribution channel?
Then I went deeper and calculated the (b) marginality per customer and per (c) single product.

After the questions just mentioned I wanted to answer other questions such as:
(d) Calculate revenue per year
(e) Calculate the revenue per single month
(f) Calculate the ratio of active customers to total customers

## 5. Create view for each answer

To store the answers to the queries I have created views, so if the question will be recurrent it will be easy to access them

# Code

## Create tables

(i) Suppliers

,CREATE TABLE suppliers(
	s_id INTEGER PRIMARY KEY,
	s_name VARCHAR(100),
	s_telephone VARCHAR(50),
	s_country VARCHAR(50),
	s_active BOOLEAN
),

# Output of the code
