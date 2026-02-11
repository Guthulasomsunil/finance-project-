# finance-project-FinTrack is a simple command-line based Finance Tracker application built using Python and SQLAlchemy ORM with an SQLite database. The application allows users to manage expense categories, record expenses, set monthly budgets, and monitor their spending.

When the program starts, it connects to an SQLite database named fintrack.db. If the required tables do not already exist, they are automatically created using SQLAlchemy’s Base.metadata.create_all() method.

The project consists of three main database tables:

Category – Stores expense categories. Each category has an id and a name. One category can have multiple expenses (One-to-Many relationship).

Expense – Stores individual expense records. Each expense includes id, title, amount, date, and category_id. The category_id is a foreign key that links the expense to a specific category.

Budget – Stores monthly budget limits. Each record contains id, month (in YYYY-MM format), and limit.

The application runs inside a continuous menu loop. The user is presented with options such as adding a category, adding an expense, viewing expenses, setting a budget, checking the budget, or exiting the program. Based on the user’s choice, the corresponding function is executed.

When adding a category, the program takes the category name as input and saves it to the database.
When adding an expense, it collects the title, amount, date, and category ID, then stores the expense in the database linked to its category.
The show expenses option retrieves and displays all stored expenses.
The set budget option allows the user to define a monthly spending limit.
The check budget option calculates the total expenses for a given month and compares them with the stored budget limit. If the total exceeds the limit, it displays “Budget exceeded”; otherwise, it shows “Within budget.”

The project demonstrates key concepts such as SQLAlchemy ORM, One-to-Many relationships, foreign keys, session management, CRUD operations, query filtering, and aggregate calculations.
