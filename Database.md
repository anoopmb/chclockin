# Database #



So, I'm working on the database, and wanted to get some feedback on the layout since my DB experience is rather limited.

### Users ###
| **userName** | **name** | **ss#** | **payRate** | **role** | **password** | **supervisorId** |
|:-------------|:---------|:--------|:------------|:---------|:-------------|:-----------------|
| PK - String  |String    |Numeric  |Numeric      |String    |Hashed String |FK - String       |

First stab SQL:
create table users (username VARCHAR(20) PRIMARY KEY NOT NULL, name VARCHAR(50) NOT NULL, ssn INT(9) NOT NULL, pay\_rate DOUBLE, role VARCHAR(20), password VARCHAR(100), supervisor\_username VARCHAR(20));

### TimeEntry ###
| **id** | **userId** | **action** | **time** | **method** | **approvedByUserId** |
|:-------|:-----------|:-----------|:---------|:-----------|:---------------------|
|PK - Numeric|FK - String |String      |TimeStamp |String      |FK - String           |

First stab SQL:
create table time\_entry (id INT PRIMARY KEY NOT NULL AUTO\_INCREMENT, username VARCHAR(20), action VARCHAR(20), time TIMESTAMP, method VARCHAR(20), approved\_by\_username VARCHAR(20));