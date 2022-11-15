```YAML
  - DBMS:
    - MYSQL AND POSTGRESQL ARE DATABASE MAANAGEMENT SYSTEMS
    - SQL IS THE DATABASE
    - SQL HAS SPECIFICATIONS AND DBMS implements them.
    - They have almost identical syntax
  - CONSTRAINT:
    - a primary key
    - DROP: ALTER TABLE table-name DROP CONTRAINT key-name;
    - INSERT: ALTER TABLE table-name ADD PRIMARY KEY (id);
  - UNIQUE CONTRAINT: 
    - ALTER TABLE table-name ADD CONTRAINT unique_name_name UNIQUE (col-name)
  - CHECK-CONSTRAINT: permet de faire des enum
    - ALTER TABLE table-name ADD_CONTRAINT contraint_name CHECK (col = "this" OR col = 'that' )
    - example -> un produit doit valoir au moins 1 euro
  - WHEN EVER WE DELETE OR UPDATE WE MUST INCLUDE WHERE -> else it will delete the entire TABLE.
  - DELETE:
    -  DELETE FROM table-name WHERE email = 'jiad@gmail.com' AND name = 'tusher';
  - UPDATE:
    - UPDATE table-name SET email = 'test@test.com' WHERE id = 1;
  - ON CONFLICT:
    - ON CONFLICT (id -> must be a unique column) DO NOTHING
    - allows to not raise error
    - allows us to update during conflict
  - ONE_TO_ONE RELATIONSHIP:
    - table_id BIGINT REFERENCES table_to_reference (id), UNIQUE(table_to_join_id)
  - INNER JOIN:
    - allows to make a query and retreive data from FOREIGN_KEY
    - SELECT * FROM table JOIN ref_table ON table.fkey_id = ref_table.id; 
  - LEFT JOIN:
    - gives back all the records who have a FOREIGN_KEY and it's data AND all the records who doesn't have FOREIGN_KEY DATA
    - SELECT * FROM tabe-le LEFT JOIN ref_table ref_table.id = table.fkey_id
  - CASCADE: ?
  - ILIKE:
    - IN POSTGRESQL as Case insensitive result
  - As: 
    - change column name in SELECT
  - COALESCE:
    -  allows us to have a default value incase the first one si not present.
  - NULLIF:
    - takes two arguments : handle division by zero
  - NOW():
    - gives the current time NOW()::Date NOW()::Time etc...
  - INTERVAL: for addition and substraction with date
    - SELECT NOW() - INTERVAL "10 day|year"
    - SELECT NOW() + INTERVAL "10 day|year"
  - EXTRACT:
    - SELECT EXTRACT(MONTH FROM NOW())
    - SELECT EXTRACT(DAY FROM NOW())
    - SELECT EXTRACT(CENTURY FROM NOW())
    - SELECT EXTRACT(DOW FROM NOW())
  - AGE:
    - permet de calculer l'age
    - SELECT name, country, date_of_birth, AGE(NOW(), date_of_birth) as age  FROM human;


  - EXTENSIONS
    - SEE EXTENSIONS:
      - SELECT * FROM pg_available_extension;
    - DOWNLOAD EXTENSIONS:
      - CREATE EXTENSION IF NOT EXISTS "uuid-ossp";
    - \df to see functions


  - SEE: INDEXES, FUNCTIONS, VIEWS, ADVANCED QUERIES, TRIGGERS, COMMON TABLE EXPRESSIONS

```
