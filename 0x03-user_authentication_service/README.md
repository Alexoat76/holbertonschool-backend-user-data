<p align="center">
<img src="https://img.shields.io/badge/LINUX-darkgreen.svg"/>
<img src="https://img.shields.io/badge/Shell-ligthgreen.svg"/>
<img src="https://img.shields.io/badge/Vim-green.svg"/>
<img src="https://img.shields.io/badge/Python-blue.svg"/>
<img src="https://img.shields.io/badge/Markdown-black.svg"/><br>	
</p>

---

# 0x03. User authentication service

This project contains some tasks for learning how to implement a *`User authentication service`*.

<p align="center">
  <img width="300"
        src="https://files.realpython.com/media/Building-a-Simple-Web-App-With-Bottle-SQLAlchemy-and-the-Twitter-API_Watermarked.93f687b7b47c.jpg"
  >
</p>

# Getting Started :running:	
<div style="text-align: justify">

## Table of Contents
* [About](#about)
* [Resources](#resources-books)
* [Requirements](#requirements)
* [Files](#files-file_folder)
* [Tasks](#tasks)
* [Credits](#credits)

## About

In the industry, you should  **not**  implement your own authentication system and use a module or framework that doing it for you (like in Python-Flask:  **[Flask-User](https://intranet.hbtn.io/rltoken/r1XmxzZ-clc7laax6Tm7WQ)** ). Here, for the learning purpose, we will walk through each step of this mechanism to understand it by doing.

## Resources :books:
Read or watch:
	
[![M](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/80px-Google_2015_logo.svg.png)](https://www.google.com/search?q=user+authentication+service+python+flask&oq=User+authentication+service+python&aqs=chrome.1.69i57j33i160l2j33i22i29i30l4.149956j0j15&sourceid=chrome&ie=UTF-8)

[![M](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Logo_of_YouTube_%282015-2017%29.svg/70px-Logo_of_YouTube_%282015-2017%29.svg.png)](https://www.youtube.com/results?search_query=user+authentication+service+python+flask)

- **[Flask documentation](https://intranet.hbtn.io/rltoken/LSFQS3aarknJpMZVr9Je1Q)** 
- **[Requests module](https://intranet.hbtn.io/rltoken/PqxwI-hQOe4b4Hhah4fbVg)** 
- **[HTTP status codes](https://intranet.hbtn.io/rltoken/QoqUvOM9taMBOVaeB_g06g)**
- How to declare API routes in a Flask app
- How to get and set cookies
- How to retrieve request form data
- How to return various HTTP status codes

## Requirements
### General
* All files will be *` interpreted/compiled `* on *` Ubuntu 18.04 LTS `* using  *` python3 `*  (version 3.7)
* All files should end with a new line
* The first line of all files should be exactly  *` #!/usr/bin/env python3 `* 
* A  *` README.md `*  file, at the root of the folder of the project, is mandatory
* The code should use the  *` pycodestyle `*  style (version 2.5)
* You should use  *` SQLAlchemy `* 1.3.x
* All files must be executable
* The length of files will be tested using wc
* All modules should have a documentation ( *` python3 -c 'print(__import__("my_module").__doc__)' `* )
* All classes should have a documentation ( *` python3 -c 'print(__import__("my_module").MyClass.__doc__)' `* )
* All functions should have a documentation ( *` python3 -c 'print(__import__("my_module").my_function.__doc__)' `* and  <br>
*` python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)' `* )
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method <br>
	(the length of it will be verified)
* All your functions should be type annotated
* The flask app should only interact with  *` Auth `*  and never with  *` DB `*  directly.
* Only public methods of  *` Auth `*  and  *` DB `*  should be used outside these classes.

## Setup
You will need to install   *` bcrypt ` *
``` pip3 install bcrypt ```

### Installation :computer:
	
- Clone this repository: `https://github.com/Alexoat76/holbertonschool-backend-user-data.git`	
- Access to directory: `cd 0x03-user_authentication_service`
- `Compile` accord to `instructions` of each task.

## Files :file_folder:

### Tests :heavy_check_mark:

+ **[tests](./tests)**: Folder of test files. *`Provided by Holberton School`*.

---

## Tasks

+ [x] 0\. **User model**
+ **[user.py](./user.py)**

In this task you will create a SQLAlchemy model named   *` User `*   for a database table named   *` users `*   (by using the  **[mapping declaration](https://intranet.hbtn.io/rltoken/IF5xw2va364LrJEntCXLlg)**
  of SQLAlchemy). 
The model will have the following attributes:
*  *` id `* , the integer primary key
*  *` email `* , a non-nullable string
*  *` hashed_password `* , a non-nullable string
*  *` session_id `* , a nullable string
*  *` reset_token `* , a nullable string

```python
#!/usr/bin/env python3
"""
Main file
"""
from user import User

print(User.__tablename__)

for column in User.__table__.columns:
    print("{}: {}".format(column, column.type))

```
```bash
$ python3 main.py
users
users.id: INTEGER
users.email: VARCHAR(250)
users.hashed_password: VARCHAR(250)
users.session_id: VARCHAR(250)
users.reset_token: VARCHAR(250)
$ 

```
---


---

## Credits

## Author(s):blue_book:

Work is owned and maintained by 
	**`Alex Orland Arévalo Tribaldos`**  and credits for `group projects` are displayed in the respective `README.md` files.

<3915@holbertonstudents.com>
	
[![M](https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/Octicons-mark-github.svg/25px-Octicons-mark-github.svg.png)](https://github.com/Alexoat76)
[![M](https://upload.wikimedia.org/wikipedia/fr/thumb/c/c8/Twitter_Bird.svg/25px-Twitter_Bird.svg.png)](https://twitter.com/aoarevalot)
[![M](https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/25px-LinkedIn_logo_initials.png)](https://www.linkedin.com/in/Alexoat76/)

## Acknowledgments :mega: 

### **`Holberton School`** (*providing guidance*)
	
This program was written as part of the curriculum for Holberton School.
Holberton School is a campus-based full-stack software engineering program
that prepares students for careers in the tech industry using project-based
peer learning. For more information,  please visit [this link](https://www.holbertonschool.com/).
![Brand](https://assets.website-files.com/6105315644a26f77912a1ada/610540e8b4cd6969794fe673_Holberton_School_logo-04-04.svg)
