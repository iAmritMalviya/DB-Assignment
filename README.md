### Read the diagram carefully and answer the below questions. ###

![ecommerce table](https://raw.githubusercontent.com/iAmritMalviya/DB-Assignment/main/product-management-ecommerce-table-.webp)

**Questions**

### 1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram. ###
Based on the provided schema, it appears that there is a one-to-many relationship between the "product" and "product_category" entities. This means that each product can belong to only one category, but each category can have multiple products associated with it. 
The relationship is established through the "category_id" attribute in the "product" entity, which likely serves as a foreign key referencing the "id" attribute in the "product_category" entity. This allows products to be categorized under specific product categories
-------

### 2. How could you ensure that each product in the "Product" table has a valid category assigned to it? ###
To ensure that each product table has a valid category assigned to it, you can set up a foreign key constraint between the product table and the category table. This constraint will enforce referential integrity, meaning that every category assigned to a product must exist in the category table. Additionally, you can implement data validation checks within your application logic to ensure that only valid category IDs are assigned to products during creation or updates.
-------

### 3. Create schema in any Database script or any ORM (Object Relational Mapping). ###
CREATE TABLE product_category (
    id INT PRIMARY KEY,
    name VARCHAR,
    description TEXT,
    created_at TIMESTAMP,
    modified_at TIMESTAMP,
    deleted_at TIMESTAMP
);

CREATE TABLE product (
    id INT PRIMARY KEY,
    name VARCHAR,
    description TEXT,
    category_id INT,
    created_at TIMESTAMP,
    modified_at TIMESTAMP,
    deleted_at TIMESTAMP
);

CREATE TABLE product_inventory (
    id INT PRIMARY KEY,
    SKU VARCHAR,
    quantity INT,
    category_id INT,
    created_at TIMESTAMP,
    modified_at TIMESTAMP,
    price DECIMAL,
    deleted_at TIMESTAMP
);

CREATE TABLE discount (
    id INT PRIMARY KEY,
    name VARCHAR,
    description TEXT,
    discount_percent DECIMAL,
    active BOOLEAN,
    created_at TIMESTAMP,
    modified_at TIMESTAMP,
    deleted_at TIMESTAMP
);

CREATE TABLE product_discount (
    id INT PRIMARY KEY,
    product_id INT,
    discount_id INT,
    created_at TIMESTAMP,
    modified_at TIMESTAMP,
    deleted_at TIMESTAMP
);
-------



Steps: 
1. create the new public repository called DB-Assignment and make a file called Answers.md
   <br> for help: [How to create the repository in gitgub](https://www.geeksforgeeks.org/creating-repository-in-github/)
2. Answers to the 1st and 2nd questions will go to the Answer.md
3. The answer to the 3rd question will go to the schema.<language_extenstion> eg(schema.js, schema.java, schema.py, schema.sql etc)
4. upload it to the GitHub.
5. insert the link in the form.

