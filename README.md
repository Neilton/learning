# learning
Repositorio de estudos sobre técnicas de programação. / Repository studies on programming techniques.

CREATE TABLE departments (
  ID           NUMBER(10)    NOT NULL,
  DESCRIPTION  VARCHAR2(50)  NOT NULL);

ALTER TABLE departments ADD (
  CONSTRAINT dept_pk PRIMARY KEY (ID));

CREATE SEQUENCE dept_seq START WITH 1;

https://github.com/LucaCanali/Oracle_DBA_scripts

https://github.com/gwenshap/Oracle-DBA-Scripts
