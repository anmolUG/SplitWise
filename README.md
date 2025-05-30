

# SplitWise Java Expense Sharing App

A command-line Java application to manage and split group expenses, inspired by the SplitWise platform.

## Features

* Add expenses and split them:

  * Equally
  * By exact amounts
  * By percentage
* View all balances or individual user balances
* Input and output handled via files
* Robust input validation and error handling


## Input Format

* `SHOW` — Show all balances.
* `SHOW <user_id>` — Show balance for a specific user.
* `EXPENSE <user_id> <amount> <num_users> <user_list> <EQUAL|EXACT|PERCENT> [values]`

**Example:**

```
EXPENSE u1 1000 4 u1 u2 u3 u4 EQUAL
EXPENSE u1 1250 2 u3 u5 EXACT 370 880
EXPENSE u4 1200 4 u1 u2 u3 u4 PERCENT 40 20 20 20
```

---

## Example

### Sample input (`input.txt`)

```
SHOW
EXPENSE u1 1000 4 u1 u2 u3 u4 EQUAL
SHOW u1
```

### Sample output (`output.txt`)

```
u2 owes u1: 250.0
u3 owes u1: 250.0
u4 owes u1: 250.0
```

---

## Technologies Used

* Java
* Collections Framework
* File I/O




