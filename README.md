## Identitas Praktikan

| Nama                         | NRP        | Class |
| ---------------------------- | ---------- | ----- |
| Putu Putra Sakti Sadhana     | 5027251101 | B     |
| Bambang Nasarillah Kurniawan | 5027251110 | B     |

## Reporting
### What is the IP and Port of the web server?
Terdapat beberapa cara agar kita bisa melihat port dari web server!
![[Pasted image 20260923143117.png]]

![[Pasted image 20260924125025.png]]

![[Pasted image 20260924125155.png]]

### To help with viewing the server packets going in and out, what's a good filter to use and why?


### Which user logged in on Sep 19, 2025 23:17:44 (GMT+7)?

![[Pasted image 20260924125825.png]]

### What time did one of the public computers got access to admin user?
![[Pasted image 20260924130103.png]]

![[Pasted image 20260924130133.png]]
### Which IP accessed the admin user?

![[Pasted image 20260924130103.png]]
### How did the attacker gain access to the admin user?

![[Pasted image 20260924130133.png]]
### What book did the attacker delete?
![[Pasted image 20260924130318.png]]

![[Pasted image 20260924131404.png]]

```json
[
	{
	"id":3,
	"title":"1984",
	"author":"George Orwell",
	"isbn":"978-0-452-28423-4",
	"year":1949,
	"description":"A dystopian social science fiction novel"
	},
	...
]
```
### The attacker added a new book to the database, what was it called?

![[Pasted image 20260924132519.png]]

```json
{
	"title":"please fix your server","author":
	"love, W.",
	"isbn":"41",
	"year":6767,
	"description":"come on",
	"userId":1
}
```
### How did the attacker successfully leak all the usernames and passwords?
```json
...
{
"id":
	"CREATE TABLE books 
	(\n id INTEGER PRIMARY KEY AUTOINCREMENT,
	\n title TEXT,
	\n author TEXT,
	\n isbn TEXT,
	\n year INTEGER,
	\n description TEXT\n )",
	"title":2,
	"author":3,
	"isbn":4,
	"year":5,
	"description":6},
{
"id":
	"CREATE TABLE sqlite_sequence(name,seq)",
	"title":2,
	"author":3,
	"isbn":4,
	"year":5,
	"description":6
},
{
"id":
	"CREATE TABLE users 
	(\n id INTEGER PRIMARY KEY AUTOINCREMENT,
	\n username TEXT UNIQUE,
	\n password TEXT,
	\n role TEXT DEFAULT 'user'\n)",
	"title":2,
	"author":3,
	"isbn":4,
	"year":5,
	"description":6
	}
]
```
### What was the password hash of admin account?

## Reference