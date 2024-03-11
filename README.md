### Read the diagram carefully and answer the below questions. ###

![ecommerce table](https://raw.githubusercontent.com/iAmritMalviya/DB-Assignment/main/product-management-ecommerce-table-.webp)

**Questions**

### 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram. ###

Ans. One to many.

### 2. How could you ensure that each product in the "Product" table has a valid category assigned to it? ###
1. Define forign key constraint.
2. Set forign key Constraint.
3. Ensures inserts and updates comply.
4. Handle Deletions Appropriately.
   
-------

### 3. Create schema in any Database script or any ORM (Object Relational Mapping). ###

Ans.

----- Create Product_Category table
CREATE TABLE Product_Category (
    category_id INT PRIMARY KEY,
    category_name VARCHAR(50) NOT NULL
);

-- Create Product table
CREATE TABLE Product (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100) NOT NULL,
    description TEXT,
    price DECIMAL(10, 2) NOT NULL,
    category_id INT,
    FOREIGN KEY (category_id) REFERENCES Product_Category(category_id)
);
----



Steps: 
1. create the new public repository called DB-Assignment and make a file called Answers.md
   <br> for help: [How to create the repository in gitgub](https://www.geeksforgeeks.org/creating-repository-in-github/)
2. Answers to the 1st and 2nd questions will go to the Answer.md
3. The answer to the 3rd question will go to the schema.<language_extenstion> eg(schema.js, schema.java, schema.py, schema.sql etc)
4. upload it to the GitHub.
5. insert the link in the form.

