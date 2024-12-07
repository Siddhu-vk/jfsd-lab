# jfsd-lab
Hibernate Criteria Query Language (HCQL) is a programmatic, object-oriented way to query a database in Hibernate. It allows developers to build complex queries dynamically using a fluent API, eliminating the need to write SQL. HCQL supports features like filtering, projections,  and joins while maintaining database independence and type safety.

Here’s a *README* text for your "Customer Hibernate Criteria Query Language" workspace:  

---

# Customer Hibernate Criteria Query Language Workspace  

This workspace demonstrates the use of *Hibernate Criteria Query Language (HQL)* for managing customer-related data. It includes various examples of how to create dynamic, type-safe queries to interact with the database and perform CRUD operations.  

## Features  
- Retrieve customer records with filtering conditions.  
- Perform sorting and projections on customer data.  
- Handle complex queries using logical expressions.  
- Dynamic query creation without writing raw SQL.  

## Prerequisites  
- *Java Development Kit (JDK) 8 or later*  
- *Hibernate ORM Framework*  
- *Database Setup* (e.g., MySQL, PostgreSQL)  
- *Maven/Gradle* for dependency management  

## Setup Instructions  
1. Clone the repository:  
   bash  
   git clone <repository-url>  
   cd customer-hql-workspace  
     
2. Configure the hibernate.cfg.xml file with your database connection details.  
3. Build the project using Maven or Gradle:  
   bash  
   mvn clean install  
     
4. Run the application:  
   bash  
   java -jar target/customer-hql.jar  
     

 Example Queries  
 Retrieve All Customers:  
java  
CriteriaBuilder cb = session.getCriteriaBuilder();  
CriteriaQuery<Customer> query = cb.createQuery(Customer.class);  
Root<Customer> root = query.from(Customer.class);  
query.select(root);  
List<Customer> customers = session.createQuery(query).getResultList();  
  

 Filter Customers by Name:  
java  
query.where(cb.equal(root.get("name"), "John Doe"));  
  

 Sort Customers by Registration Date:  
java  
query.orderBy(cb.desc(root.get("registrationDate")));  
  

 Contributions  
Feel free to fork the repository and contribute to improve or add more query examples.  

 License  
This project is licensed under the MIT License.  

--- 

This can serve as a base for your workspace documentation. Let me know if you want to add anything specific!
