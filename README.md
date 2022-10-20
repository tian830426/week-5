# week-5
wehelp

SHOW DATABASES;
USE website;
SHOW TABLES;
SELECT*FROM member;
CREATE DATABASE website;
USE website;
SHOW TABLES;
CREATE TABLE member(
id BIGINT PRIMARY KEY AUTO_INCREMENT,
name VARCHAR(255) NOT NULL,
usename VARCHAR(255) NOT NULL,
password VARCHAR(255) NOT NULL,
follower_count INT UNSIGNED NOT NULL DEFAULT 0,
time datetime NOT NULL DEFAULT 20221020120000
);
DROP TABLE member;
SHOW TABLES;

創建新資料表
CREATE TABLE member(
id BIGINT PRIMARY KEY AUTO_INCREMENT,
name VARCHAR(255) NOT NULL,
usename VARCHAR(255) NOT NULL,
password VARCHAR(255) NOT NULL,
follower_count INT UNSIGNED NOT NULL DEFAULT 0,
time datetime NOT NULL DEFAULT 20221020120000
);

####1.新增資料
INSERT INFO member (name, usename, password, follow_count, time)VALUES('Helen', 'test', 'test', '1000', '20221020120000'),
('John', 'test1', 'test1', '2000', '20221020120000'),('Joyce', 'test2', 'test2', '3000', '20221020120000'),('Emily', 'test3', 'test3', '4000', '20221020120000');

2.使用 SELECT 指令取得所有在 member 資料表中的會員資料。 

SELECT*FROM member;

3.使用 SELECT 指令取得所有在 member 資料表中的會員資料，並按照 time 欄位，由  近到遠排序。  
SELECT * FROM member ORDER BY time;


4.使用 SELECT 指令取得 member 資料表中第 2 ~ 4 共三筆資料，並按照 time 欄位，  由近到遠排序。( 並非編號 2、3、4 的資料，而是排序後的第 2 ~ 4 筆資料 ) 

SELECT * FROM member WHERE time >= 

SELECT * FROM member ORDER BY time;


5.使用 SELECT 指令取得欄位 username 是 test 的會員資料。  
SELECT ＊ FROM member WHERE username = ’test’;

6.使用 SELECT 指令取得欄位 username 是 test、且欄位 password 也是 test 的資料。  
SELECT ＊ FROM member WHERE username = ’test’ AND password = ‘test’;

7.使用 UPDATE 指令更新欄位 username 是 test 的會員資料，將資料中的 name 欄位改  成 test2  
UPDATA member SET name=test
WHERE username = ‘test’;
————

取得 member 資料表中，總共有幾筆資料 ( 幾位會員 )。 

select count( * ) as 總共有幾筆資料 from member

取得 member 資料表中，所有會員 follower_count 欄位的總和。 

select sum( follower_count) as 總和 from member 
取得 member 資料表中，所有會員 follower_count 欄位的平均數。  
select avg( follower_count) as 總和 from member 
 

