[CHEAT SHEET](https://github.com/dsteven12/WGU-Data-Mgmt-and-Applications---SQL)


 ```
CREATE TABLE COFFEE_SHOP (
  shop_id INTEGER,
  shop_name VARCHAR(50),
  city VARCHAR(50),
  state CHAR(2),
  PRIMARY KEY (shop_id)
  );
CREATE TABLE EMPLOYEE (
  employee_id INTEGER,
  first_name VARCHAR(30),
  last_name VARCHAR(30),
  hire_date DATE,
  job_title VARCHAR(30),
  PRIMARY KEY(employee_id),
  shop_id INTEGER,
  FOREIGN KEY (shop_id) REFERENCES COFFEE_SHOP(shop_id)
  );

CREATE TABLE SUPPLIER (
  supplier_id INTEGER,
  company_name VARCHAR(30),
  country VARCHAR(30),
  sales_contact_name VARCHAR(60),
  email VARCHAR(50) NOT NULL,
  PRIMARY KEY (supplier_id)
  );

 CREATE TABLE COFFEE (
   coffee_id INTEGER,
   shop_id INTEGER,
   supplier_id INTEGER,
   coffee_name VARCHAR(30),
   price_per_pound NUMERIC(5,2),
   PRIMARY KEY (coffee_id),
   FOREIGN KEY (shop_id) REFERENCES COFFEE_SHOP(shop_id),
   FOREIGN KEY (supplier_id) REFERENCES SUPPLIER(supplier_id)
   );

INSERT INTO COFFEE_SHOP
VALUES
(1, 'Coava', 'San Diego', 'CA'),
(2, 'Three Ships', 'Virginia Beach', 'VA'),
(3, 'Ritual', 'San Fransisco', 'CA');

INSERT INTO EMPLOYEE
VALUES
(1, 'John', 'Doe', '2000-07-31', 'CEO', 1),
(2, 'Smith', 'Doe', '1998-07-22', 'CTO', 2),
(3, 'James', 'Ware', '2000-06-05', 'CFO', 3);

INSERT INTO SUPPLIER
VALUES
(1, 'Company 1', 'Columbia', 'John Doe', 'Jdoe@gmail.com'),
(2, 'Company 2', 'Mexico', 'Smith Doe', 'SDoe@yahoo.com'),
(3, 'Company 3', 'Paraguay', 'James Ware', 'Jware@aol.com');

INSERT INTO COFFEE
VALUES
(1, 1, 1, 'Coffee 1', 50.03),
(2, 2, 2, 'Coffee 2', 60.40),
(3, 3, 3, 'Coffee 3', 70.30);
```

```

CREATE VIEW CONCATEMPLOYEE AS
SELECT employee_id, CONCAT_WS(' ', first_name, last_name) AS full_name, hire_date, job_title, shop_id
FROM EMPLOYEE;

CREATE INDEX COFFEENAME
ON COFFEE (coffee_name);
```

```
SHOW CREATE VIEW CONCATEMPLOYEE;
SHOW INDEX FROM COFFEE;

SELECT * FROM COFFEE_SHOP;
SELECT * FROM EMPLOYEE;
SELECT * FROM COFFEE;
SELECT * FROM SUPPLIER;

SELECT S.*, C.*, P.*
FROM COFFEE_SHOP S
INNER JOIN
COFFEE C ON S.shop_id = C.shop_id
INNER JOIN
SUPPLIER P ON P.supplier_id= C.supplier_id;
```
