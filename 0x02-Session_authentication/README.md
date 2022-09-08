<p align="center">
<img src="https://img.shields.io/badge/LINUX-darkgreen.svg"/>
<img src="https://img.shields.io/badge/Shell-ligthgreen.svg"/>
<img src="https://img.shields.io/badge/Vim-green.svg"/>
<img src="https://img.shields.io/badge/Python-blue.svg"/>
<img src="https://img.shields.io/badge/Markdown-black.svg"/><br>	
</p>

---

# 0x02. Session authentication

This project contains some tasks for learning how to  implement a *`Session Authentication`*.

<p align="center">
  <img width="260"
        src="https://www.cnet.com/a/img/73gmAv9Iu3BXf3oZ6cDQ2v3JxuU=/2017/04/21/5b8ac90a-9204-4050-b93c-36e304bdb77c/gif-password.gif"
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

In this project, you will implement a  Session Authentication . You are not allowed to install any other module.
In the industry, you should  not  implement your own Session authentication system and use a module or framework that doing it for you (like in Python-Flask:  **[Flask-HTTPAuth](https://intranet.hbtn.io/rltoken/3Q-d2k3A-L-AyrvAcUJzAg)**
 ). Here, for the learning purpose, we will walk through each step of this mechanism to understand it by doing.

## Resources :books:
Read or watch:
	
[![M](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Google_2015_logo.svg/80px-Google_2015_logo.svg.png)](https://www.google.com/search?q=session+authenticationa+api+python&oq=Session+authenticationa+api+py&aqs=chrome.1.69i57j33i10i160l2.15691j0j15&sourceid=chrome&ie=UTF-8)

[![M](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e1/Logo_of_YouTube_%282015-2017%29.svg/70px-Logo_of_YouTube_%282015-2017%29.svg.png)](https://www.youtube.com/results?search_query=session+authenticationa+api+python)

- **[REST API Authentication Mechanisms - Only the session auth part](https://intranet.hbtn.io/rltoken/iT3ar2nR1Ljhujo5Qyvfpg)** 
- **[HTTP Cookie](https://intranet.hbtn.io/rltoken/jvMahr6fVHaCtt-grGFM9A)** 
- **[Flask](https://intranet.hbtn.io/rltoken/s4vbno-huyUzOrgDXDgj3w)** 
- **[Flask Cookie](https://intranet.hbtn.io/rltoken/jk07WKFJylBJmvSuJce_qQ)** 
- What authentication means
- What session authentication means
- What Cookies are
- How to send Cookies
- How to parse Cookies

## Requirements
### General
* All files will be *` interpreted/compiled `* on *` Ubuntu 18.04 LTS `* using  *` python3 `*  (version 3.7)
* All files should end with a new line
* The first line of all files should be exactly  *` #!/usr/bin/env python3 `* 
* A  *` README.md `*  file, at the root of the folder of the project, is mandatory
* The code should use the  *` pycodestyle `*  style (version 2.5)
* All files must be executable
* The length of files will be tested using wc
* All modules should have a documentation ( *` python3 -c 'print(__import__("my_module").__doc__)' `* )
* All classes should have a documentation ( *` python3 -c 'print(__import__("my_module").MyClass.__doc__)' `* )
* All functions should have a documentation ( *` python3 -c 'print(__import__("my_module").my_function.__doc__)' `* and  <br>
*` python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)' `* )
* A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method <br>
	(the length of it will be verified)

### Installation :computer:
	
- Clone this repository: `https://github.com/Alexoat76/holbertonschool-backend-user-data.git`	
- Access to directory: `cd 0x02-Session_authentication`
- `Compile` accord to `instructions` of each task.

## Files :file_folder:

### Tests :heavy_check_mark:

+ **[tests](./tests)**: Folder of test files. *`Provided by Holberton School`*.
+ **[archive.zip](./archive.zip)**: File that contents SimpleAPI. *`Provided by Holberton School`*.
		
---

## Tasks

+ [x] 0\. **Et moi et moi et moi!**
+ **[api/v1/app.py](./api/v1/app.py)**
+ **[api/v1/views/users.py](./api/v1/views/users.py)**

Copy all your work of the  **[0x01. Basic authentication](https://intranet.hbtn.io/rltoken/tUmo1sDyeyKisCMqoWe-Pw)** 
  project in this new folder.
In this version, you implemented a  Basic authentication  for giving you access to all User endpoints:
-  *` GET /api/v1/users `* 
-  *` POST /api/v1/users `* 
-  *` GET /api/v1/users/<user_id> `* 
-  *` PUT /api/v1/users/<user_id> `* 
-  *` DELETE /api/v1/users/<user_id> `*
	
Now, you will add a new endpoint:   *` GET /users/me `*   to retrieve the authenticated   *` User `*   object.
* Copy folders  *` models `*  and  *` api `*  from the previous project  *` 0x06. Basic authentication `* 
* Please make sure all mandatory tasks of this previous project are done at 100% because this project (and the rest of this track) will be based on it.
* Update  *` @app.before_request `*  in  *` api/v1/app.py `* :
	* Assign the result of  *` auth.current_user(request) `*  to  *` request.current_user `* 
* Update method for the route  *` GET /api/v1/users/<user_id> `*  in  *` api/v1/views/users.py `* :
	* If  *` <user_id> `*  is equal to  *` me `*  and  *` request.current_user `*  is  *` None `* :  *` abort(404) `* 
	* If  *` <user_id> `*  is equal to  *` me `*  and  *` request.current_user `*  is not  *` None `* : return the authenticated  *` User `*  in a JSON response 		(like a normal case of  *` GET /api/v1/users/<user_id> `*  where  *` <user_id> `*  is a valid  *` User `*  ID)
	* Otherwise, keep the same behavior

In the first terminal:
```python3
#!/usr/bin/env python3
""" Main 0
"""
import base64
from api.v1.auth.basic_auth import BasicAuth
from models.user import User

""" Create a user test """
user_email = "bob@hbtn.io"
user_clear_pwd = "H0lbertonSchool98!"

user = User()
user.email = user_email
user.password = user_clear_pwd
print("New user: {}".format(user.id))
user.save()

basic_clear = "{}:{}".format(user_email, user_clear_pwd)
print("Basic Base64: {}".format(base64.b64encode(basic_clear.encode('utf-8')).decode("utf-8")))

```
```bash
$
$ API_HOST=0.0.0.0 API_PORT=5000 AUTH_TYPE=basic_auth ./main_0.py 
New user: 9375973a-68c7-46aa-b135-29f79e837495
Basic Base64: Ym9iQGhidG4uaW86SDBsYmVydG9uU2Nob29sOTgh
$
$ API_HOST=0.0.0.0 API_PORT=5000 AUTH_TYPE=basic_auth python3 -m api.v1.app
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

```
In a second terminal:

```bash
$ curl "http://0.0.0.0:5000/api/v1/status"
{
  "status": "OK"
}
$
$ curl "http://0.0.0.0:5000/api/v1/users"
{
  "error": "Unauthorized"
}
$ 
$ curl "http://0.0.0.0:5000/api/v1/users" -H "Authorization: Basic Ym9iQGhidG4uaW86SDBsYmVydG9uU2Nob29sOTgh"
[
  {
    "created_at": "2017-09-25 01:55:17", 
    "email": "bob@hbtn.io", 
    "first_name": null, 
    "id": "9375973a-68c7-46aa-b135-29f79e837495", 
    "last_name": null, 
    "updated_at": "2017-09-25 01:55:17"
  }
]
$
$ curl "http://0.0.0.0:5000/api/v1/users/me" -H "Authorization: Basic Ym9iQGhidG4uaW86SDBsYmVydG9uU2Nob29sOTgh"
{
  "created_at": "2017-09-25 01:55:17", 
  "email": "bob@hbtn.io", 
  "first_name": null, 
  "id": "9375973a-68c7-46aa-b135-29f79e837495", 
  "last_name": null, 
  "updated_at": "2017-09-25 01:55:17"
}
$

```

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
