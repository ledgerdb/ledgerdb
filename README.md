# ledgerdb
Blockchain based database

### Architecture

In blockchain content is created by users only, so practically every user has public/private key pair that is their credentials and criptographic functions that are using for singnature and hashing blocks, PoW (proof of work); that are all is using to create content in database.

This blockchain database can have only a single table, that formally can be represented as a key-value store.
Where the key is the address of the user (practically public key or hash of public key).
Value is some blob content in format understandable by all instances and information have to be enough to perform transactions with another users.

So, blockchain database is focused on user-user transactions recording rather than storing different kind of information like a general database.

We do not need SQL queries, because it is only one table of state, all other information is mutations under this table.

#### Why bitcoin does not have this table? 

The answer is that it has, this table could be fully computable in bitcoin implementation. It computes value in this table by looking to all transactions in a past, and may be locally stores it in cache. 

#### How to achieve 1000TPS (transactions per second)

This is a good question. Now bitcoin processes 3TPS and it looks like a limit of the architecture. For really distributed system it must not be a limit.
The solution here is well known in computer science: divide and rule.

How to achieve this in a single chain? Very simple answer is always in question, why single?






