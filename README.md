# week-5
## wehelp

```

CREATE DATABASE website;
SHOW DATABASES;
USE website;

CREATE TABLE member(
   id BIGINT PRIMARY KEY AUTO_INCREMENT,
   name VARCHAR(255) NOT NULL,
   username VARCHAR(255) NOT NULL,
   password VARCHAR(255) NOT NULL,
   follower_count INT UNSIGNED NOT NULL DEFAULT 0,
   time datetime NOT NULL DEFAULT NOW()
   );
   
SHOW TABLES;

```
### 要求三:SQL CRUD 
利用要求二建立的資料庫和資料表，寫出能夠滿足以下要求的 SQL 指令:

● 使用 INSERT 指令新增一筆資料到 member 資料表中，這筆資料的 username 和 password 欄位必須是 test。接著繼續新增至少 4 筆隨意的資料。
指令:
```
INSERT INTO member(name, username, password, follower_count)
    VALUES('Helen', 'test', 'test', 1000);
```
    
    <img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-1.png'></img>
```
    INSERT INTO member(name, username, password, follower_count)
    VALUES('Joyce', 'test1', 'test1', 2000);
    
    INSERT INTO member(name, username, password, follower_count)
    VALUES('John', 'test2', 'test2', 3000);
    
    INSERT INTO member(name, username, password, follower_count)
    VALUES('Emily', 'test3', 'test3', 4000);
```
    
    <img src='[https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-1.png](https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-1-2.png)'></img>

● 使用 SELECT 指令取得所有在 member 資料表中的會員資料。
指令: 
```
SELECT*FROM member; 
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-2.png'></img>

● 使用 SELECT 指令取得所有在 member 資料表中的會員資料，並按照 time 欄位，由
近到遠排序。
指令: 
```
SELECT * FROM member ORDER BY time DESC;
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-3.png'></img>

● 使用 SELECT 指令取得 member 資料表中第 2 ~ 4 共三筆資料，並按照 time 欄位，
由近到遠排序。( 並非編號 2、3、4 的資料，而是排序後的第 2 ~ 4 筆資料 )
指令: 
```
SELECT * FROM member WHERE 1=1 LIMIT 1,3;
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-4.png'></img>

● 使用 SELECT 指令取得欄位 username 是 test 的會員資料。
指令: 
```
SELECT * FROM member WHERE username ="test";
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-5.png'></img>

● 使用 SELECT 指令取得欄位 username 是 test、且欄位 password 也是 test 的資料。
指令:  
```
SELECT * FROM member WHERE username ="test" and password ="test";
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-6.png'></img>

● 使用 UPDATE 指令更新欄位 username 是 test 的會員資料，將資料中的 name 欄位改
成 test2。
指令: 
```
SELECT * FROM member WHERE username ="test" and password ="test";
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E4%B8%89-%EF%BC%97.png'></img>


### 要求四:SQL Aggregate Functions
利用要求二建立的資料庫和資料表，寫出能夠滿足以下要求的 SQL 指令:

● 取得 member 資料表中，總共有幾筆資料 ( 幾位會員 )。
指令: 
```
select count( * ) as 總共有幾筆資料 from member;
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E5%9B%9B-1.png'></img>

● 取得 member 資料表中，所有會員 follower_count 欄位的總和。
指令: 
```
select sum( follower_count) as 總和 from member;
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E5%9B%9B-2.png'></img>

● 取得 member 資料表中，所有會員 follower_count 欄位的平均數。
指令: 
```
select avg( follower_count) as 平均數 from member;
```

<img src='https://github.com/tian830426/week-5/blob/main/%E8%A6%81%E6%B1%82%E5%9B%9B-3.png'></img>
