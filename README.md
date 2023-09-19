# oracle emp,dept,salgrade table  to mysql emp,dept,salgrade table convert

## Create dept table
```
CREATE TABLE dept (
  deptno DECIMAL(2,0),
  dname VARCHAR(14),
  loc VARCHAR(13),
  PRIMARY KEY (deptno)
);
```
## Insert data in dept table

```

INSERT INTO dept
VALUES(10, 'ACCOUNTING', 'NEW YORK');
INSERT INTO dept
VALUES(20, 'RESEARCH', 'DALLAS');
INSERT INTO dept
VALUES(30, 'SALES', 'CHICAGO');
INSERT INTO dept
VALUES(40, 'OPERATIONS', 'BOSTON');
```

## Create emp table

```
CREATE TABLE emp (
  empno DECIMAL(4,0),
  ename VARCHAR(10),
  job VARCHAR(9),
  mgr DECIMAL(4,0),
  hiredate DATE,
  sal DECIMAL(7,2),
  comm DECIMAL(7,2),
  deptno DECIMAL(2,0),
  PRIMARY KEY (empno),
  FOREIGN KEY (deptno) REFERENCES dept (deptno)
);
```
## Insert data in emp table
```
INSERT INTO emp
VALUES(
 7839, 'KING', 'PRESIDENT', NULL,
 '1981-11-17',
 5000, NULL, 10
);
INSERT INTO emp
VALUES(
 7698, 'BLAKE', 'MANAGER', 7839,
 '1981-05-01',
 2850, NULL, 30
);
INSERT INTO emp
VALUES(
 7782, 'CLARK', 'MANAGER', 7839,
 '1981-06-09',
 2450, NULL, 10
);
INSERT INTO emp
VALUES(
 7566, 'JONES', 'MANAGER', 7839,
 '1981-04-02',
 2975, NULL, 20
);
INSERT INTO emp
VALUES(
 7788, 'SCOTT', 'ANALYST', 7566,
 '1987-07-13' - INTERVAL 85 DAY,
 3000, NULL, 20
);
INSERT INTO emp
VALUES(
 7902, 'FORD', 'ANALYST', 7566,
 '1981-12-03',
 3000, NULL, 20
);
INSERT INTO emp
VALUES(
 7369, 'SMITH', 'CLERK', 7902,
 '1980-12-17',
 800, NULL, 20
);
INSERT INTO emp
VALUES(
 7499, 'ALLEN', 'SALESMAN', 7698,
 '1981-02-20',
 1600, 300, 30
);
INSERT INTO emp
VALUES(
 7521, 'WARD', 'SALESMAN', 7698,
 '1981-02-22',
 1250, 500, 30
);
INSERT INTO emp
VALUES(
 7654, 'MARTIN', 'SALESMAN', 7698,
 '1981-09-28',
 1250, 1400, 30
);
INSERT INTO emp
VALUES(
 7844, 'TURNER', 'SALESMAN', 7698,
 '1981-09-08',
 1500, 0, 30
);
INSERT INTO emp
VALUES(
 7876, 'ADAMS', 'CLERK', 7788,
 '1987-07-13' - INTERVAL 51 DAY,
 1100, NULL, 20
);
INSERT INTO emp
VALUES(
 7900, 'JAMES', 'CLERK', 7698,
 '1981-12-03',
 950, NULL, 30
);
INSERT INTO emp
VALUES(
 7934, 'MILLER', 'CLERK', 7782,
 '1982-01-23',
 1300, NULL, 10
);

COMMIT;

```
## Create salgrade table
```
CREATE TABLE salgrade (
  grade int,
  losal int,
  hisal int
);
```
## Insert data in salgrade table
```
INSERT INTO salgrade VALUES (1, 700, 1200); 
INSERT INTO salgrade VALUES (2, 1201, 1400);
INSERT INTO salgrade VALUES (3, 1401, 2000); 
INSERT INTO salgrade VALUES (4, 2001, 3000);
INSERT INTO salgrade VALUES (5, 3001, 9999); 
COMMIT;
```
