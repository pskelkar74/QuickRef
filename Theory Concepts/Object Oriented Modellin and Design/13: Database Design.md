# Database Design

- Implementing structure
  - Implement classes = create tables
  - Implement associations = create tables that are related by primary key, foreign key pairs
  - Implement generalisation = create tables that are related by primary key, foreign key pairs
  - Implement identity = ensure suitable PK identifiers in tables

- Key functionality
  - Coupling a programming language to a database
    - Preprocessor and Postprocessor
      - Take a view and process
    - Script file
    - Embedded DBMS commands
    - API
    - Stored Procedures
    - Fourth Generation Language (4GL)
    - Generic Layer
    - Metadata-Driven system
  - Converting data
    - Data cleaning
    - Handling missing data
    - Moving Data
    - Merging Data
    - Changing Data structure
  - Encapsulation vs Query Optimization
    - How to process data
    - Single query is allowed to access any field, but encapsulation should not allow this
  - Use of SQL code
    - Write a pure OO frotnend
    - Preserves encapsulation