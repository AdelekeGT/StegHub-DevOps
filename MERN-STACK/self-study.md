# SELF-STUDY

## Database Management Systems (DBMS)

Database Management Systems (DBMS) are essential for organizing, retrieving, and managing data in databases. They ensure data integrity, security, and efficiency in handling large volumes of data. There are several DBMS types, each suited for specific needs:

### Types of DBMS and Their Suitability

1. **Relational DBMS (RDBMS):**

   - **Description:** Utilizes a table-based structure where data is organized in rows and columns. Each table can have relationships with other tables via foreign keys.
   - **Use Cases:** Ideal for applications requiring complex queries, transactions, and data integrity, such as financial systems, customer relationship management (CRM) systems, and enterprise resource planning (ERP) software.
   - **Examples:** MySQL, PostgreSQL, Oracle Database, Microsoft SQL Server.

2. **NoSQL DBMS:**
   - **Description:** Encompasses a variety of database types designed for specific data models. Includes key-value stores, document databases, column-family stores, and graph databases.
   - **Use Cases:** Suitable for applications with unstructured or semi-structured data, high scalability needs, and agile development, such as social networks, real-time analytics, and content management.
   - **Examples:** MongoDB (document-based), Cassandra (column-family store), Redis (key-value store), Neo4j (graph database).

### Relational DBMS vs. NoSQL

- **Data Structure:**

  - **RDBMS:** Tables with predefined schemas.
  - **NoSQL:** Flexible schemas; includes key-value pairs, documents, graph structures, or wide-column stores.

- **Scalability:**

  - **RDBMS:** Typically scales vertically (upgrading the same server).
  - **NoSQL:** Designed to scale horizontally (adding more servers).

- **Query Language:**

  - **RDBMS:** Structured Query Language (SQL).
  - **NoSQL:** Varies by database (e.g., MongoDB uses a query language similar to JSON).

- **Transactions:**
  - **RDBMS:** Strong ACID (Atomicity, Consistency, Isolation, Durability) compliance.
  - **NoSQL:** Eventual consistency model is common, though some support ACID transactions.

## Web Application Frameworks

Web Application Frameworks simplify the process of building web applications by providing a structured environment, reusable components, and tools.

### Server-side Frameworks

- **Description:** Run on the server and handle business logic, database interactions, and server-side rendering of web pages before sending them to the client.
- **Examples & Use Cases:**
  - **Express.js (Node.js):** Lightweight, suitable for building RESTful APIs.
  - **Django (Python):** High-level, promotes rapid development and clean design.
  - **Ruby on Rails (Ruby):** Convention over configuration, suitable for database-backed web applications.

### Client-side Frameworks

- **Description:** Run in the browser and handle the user interface logic, improving the user experience by providing dynamic and interactive web pages.
- **Examples & Use Cases:**
  - **React (JavaScript):** Component-based, good for complex UIs.
  - **Angular (TypeScript):** Comprehensive, includes tools for building SPAs.
  - **Vue.js (JavaScript):** Progressive framework, easy to integrate into projects.

## RESTful API

### What is a RESTful API?

- **REST (Representational State Transfer):** Architectural style for designing networked applications.
- **API (Application Programming Interface):** Allows interaction between software applications.

### Usage in Web Development

- RESTful APIs use HTTP requests to perform CRUD (Create, Read, Update, Delete) operations on resources.
- They employ standard HTTP methods (GET, POST, PUT, DELETE, etc.).
- Commonly used to enable communication between the client and server in web applications, making it easier to interact with databases or third-party services.

## Cascading Style Sheets (CSS)

### What is CSS?

- **CSS:** A stylesheet language used for describing the presentation of a document written in HTML or XML.

### Usage

- **Styling Web Pages:** CSS controls layout, colors, fonts, and overall visual aesthetics.
- **Responsive Design:** Ensures web pages render well across different devices and screen sizes.
- **Separation of Concerns:** Keeps HTML structure and CSS styling separate, making code easier to manage and maintain.
