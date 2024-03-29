# Navio.py

Simple API wrapper for Navio, the ETS/ATS job logger.

# Table of contents
- [Installation and setup](https://github.com/mrbean565/Navio-Integration/tree/main/navio#installation-and-setup)
- [Usage](https://github.com/mrbean565/Navio-Integration/tree/main/navio#usage)
- [Support](https://github.com/mrbean565/Navio-Integration/tree/main/navio#support)


## Installation and setup

**This module is compatible with Python v3+**

You can install this module via PyPI:
```bash
$ pip install navio.py
```

 
## Usage

To authenticate:

```py
from navio import Auth

navio_auth = Auth(navio_token)

# Returns a status code
print(navio_auth.authorise())

```

Practical use of authentication:

```py
from navio import Auth 

navio_auth = Auth(navio_token)

auth_status_code = navio_auth.authorise()

if auth_status_code == 200:
    # success
    print("Authorised!")
else:
    print(auth_status_code)    
```

Non Authentication:

```py
from navio import Navio

navio = Navio(navio_token)

# returns drivers information in json format
print(navio.drivers())
```

Available Methods (Auth):

```py
authorise() # Authorise                  
```

Available Methods (Navio):

```py
me() # Information about you (your company)
drivers() # Drivers information
add_driver() # Add driver
```


## Support

If you need help with anything, you should preferably contact BEAN#0001 on discord. If that is not possible, feel free to open a new issue. Note that if the issue is invalid, it may be closed.
