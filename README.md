# Programming challenge - for developer position

Please read this document from beginning to end, very carefully.
The intention of this test is to evaluate your tech knowledge in programming.
In this test you have to parse [this text file(CNAB)](https://github.com/ByCodersTec/challenge-dev/blob/main/CNAB.txt) and save its information (financial transactions) in a database at the candidate's discretion.
This challenge must be made by you in your house. Spend the time you need, but normally, you shouldn’t need more than a few hours.

# Challenge Delivery Instructions

1. First, fork this project to your Github account (create an account if you don’t have one).
2. After that, implement the project as described below, in your local clone.
3. Finally, send your project via email to your bycoders_ contact, with rh@bycoders.com.br cc’d.

# Project Description


You received a CNAB file with data regarding  financial transactions of several stores.
We need to create a way for this data to be imported to a database.


Your task is to create a web interface that accepts upload of [CNAB file](https://github.com/ByCodersTec/challenge-dev/blob/main/CNAB.txt), normalizes and stores the data in a relational database and displays this information on screen.


**Your web application must:**

1. Have a screen (via a form) to upload the file ( extra points if you don't use a popular CSS Framework )
2. Parse the received file, normalize the data, and correctly save the information in a relational database, **paying attention to the documentation** below
3. Display a list of transactions imported by stores, and this list should contain an account balance totalizer
4. Be written in your preferred programming language
5. Be simple to configure and run, running in a Unix-compatible environment (Linux or Mac OS X). It should only use free languages ​​and libraries
6. Git with well-described atomic commits
7. PostgreSQL, MySQL or SQL Server
8. Have automated tests
9. Docker compose (Extra points if used)
10. Readme file describing the project and its setup well
11. Include information describing how to consume the API endpoint

**Your web application doesn’t have to:**

1. Deal with authentication or authorization (extra points if it does, more extra points if authentication is done via OAuth).
2. Be written using some specific framework (but there's nothing wrong with using them too, use what you think best)
3. API documentation.(It will be a differential and extra points if you do)

# CNAB Documentation

| Field Description  | Start Point | End | Size | Commentary
| ------------- | ------------- | -----| ---- | ------
| Type  | 1  | 1 | 1 | Kind of transaction
| Date  | 2  | 9 | 8 | Date of occurrence
| Value | 10 | 19 | 10 | Movement value. *Obs.* The value found in the file needs to be divided by one hundred(value / 100.00) to normalize it.
| CPF <br>(Individual taxpayer identification) | 20 | 30 | 11 | Beneficiary's CPF (Individual taxpayer identification)
| Card | 31 | 42 | 12 | Card used in transaction 
| Time  | 43 | 48 | 6 | Time of occurrence according to UTC-3 timezone
| Store Owner | 49 | 62 | 14 | Store Representative’s Name
| Store Name | 63 | 81 | 19 | Store Name


# Documentation on transaction types

| Type | Description | Nature | Sign |
| ---- | -------- | --------- | ----- |
| 1 | Debit | Inflow | + |
| 2 | Banking billet | Outflow | - |
| 3 | Financing | Outflow | - |
| 4 | Credit | Inflow | + |
| 5 | Loan Receipt | Inflow | + |
| 6 | Sales | Inflow | + |
| 7 | TED transaction | Inflow | + |
| 8 | DOC transaction | Inflow | + |
| 9 | Rent | Outflow | - |

# Evaluation

Your project will be evaluated according to the following criteria.

1. Does your application meet the basic requirements?
2. Have you documented how to set up the environment and run your application?
3. Did you follow the challenge submission instructions?
4. Quality and coverage of unit tests.


Additionally, we will try to check your familiarity with the standard libraries (standard libs), as well as your experience with object-oriented programming from the structure of your project.

# Refer

This challenge was based on: https://github.com/lschallenges/data-engineering

---

Good Luck!
