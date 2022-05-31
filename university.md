# University

## Departments

- id:               PK NOTNULL UNIQUE INDEX AI
- name:             VARCHAR(50) NOTNULL
- address:          VARCHAR(50) NOTNULL
- email:            VARCHAR(50) NOTNULL
- telephone:        VARCHAR(11) NOTNULL


## Degree_Courses

- id:               PK NOTNULL UNIQUE INDEX AI
- name:             VARCHAR(25) NOTNULL
- duration:         VARCHAR(15) NOTNULL
- needed_cfu:       TINYINT NOTNULL
- price:            SMALLINT NOTNULL

## Courses

- id:               PK NOTNULL UNIQUE INDEX AI
- name:             VARCHAR(50) NOTNULL
- duration:         VARCHAR(15) NOTNULL
- cfu:              TINYINT NULL

## Teachers

- id:               PK NOTNULL UNIQUE INDEX AI
- name:             VARCHAR(50) NOTNULL 
- lastname:         VARCHAR(50) NOTNULL INDEX
- age:              TINYINT NULL
- telephone:        VARCHAR(11) NULL
- email:            VARCHAR(50) NOTNULL

## Students

- id:               PK NOTNULL UNIQUE INDEX AI
- name:             VARCHAR(50) NOTNULL
- lastname:         VARCHAR(50) NOTNULL INDEX
- age:              TINYINT NOTNULL
- telephone:        VARCHAR(11) NOTNULL
- email:            VARCHAR(50) NOTNULL

## Students_Vote:

- id:               PK NOTNULL UNIQUE INDEX AI
- vote:             TINYINT NOTNULL

## Exam Sessions

- id:               PK NOTNULL UNIQUE INDEX AI
- date:             DATETIME NOTNULL
- duration:         VARCHAR(10) NOTNULL
- seats:            SMALLINT NOTNULL
