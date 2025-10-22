# Python

`Python` is a high-level programming language that is used for web development, data analysis, AI, automation, and more.

+ [Setup](#setup)
    + [Virtual Environment](#virtual-environment)
    + [Install Packages](#install-packages)
    + [Dependencies](#dependencies)
+ [Hello World](#hello-world)

## Setup
To check that `Python` is installed and also if the `Pip` package manage - `https://pypi.org/project/pip/` - is also installed:

```shell
$ python3 --version
$ pip3 --version
```

### Virtual Environment
A `Virtual Environment (venv)` is an isolated workspace in a `Python` project used to keep dependencies separate (recommended) - so libraries and versions don't conflict with another project. To create a `Virtual Environment` when creating a new project:

```shell
$ python3 -m venv venv
```

Once a `Virtual Environment` has been created, whenever a project is opened, this can be activated:

```shell
# macOS
$ source venv/bin/activate
# Windows
$ venv\Scripts\activate

# Terminal prompt once the Virtual Environment is activated:
(venv) $
```

When closing the project, after working, run the command to close the `Virtual Environment`:

```shell
$ deactivate
```

### Install Packages
Use `Pip` to install packages for a `Python` project.

```shell
$ pip3 install package-name-here
```

Check installed packages:

```shell
$ pip3 list
```

### Dependencies
When installing packages and libraries, these become dependencies. Save all dependencies to a file named `requirements.txt`:

```shell
$ pip3 freeze > requirements.txt
```

When opening a project, the same dependencies can be retrieved using:

```shell
$ pip3 install -r requirements.txt
```

## Hello World
The easiest program to create is the simple `Hello World` program. The `print()` function displays text or data on the screen (or in the terminal). Open a file named `hello.py` and add the following `Python` code:

```python
print("Hello, World")
```

To run the script:

```shell
$ python3 hello.py
```

```python
import requests

# Page URL
url = "https://frontify.com/test"

try:
    # Use HEAD to avoid downloading the BODY
    response = requests.head(url, allow_redirects=True)

    # Return the status codes for the page URL provided
    if response.status_code == 200 or response.status_code == 404:
        print(f"{url}: {response.status_code}")
    else:
        print(f"{url}: {response.status_code}")

except requests.exceptions.RequestException as e:
    print(f"Error checking URL: {e}")
```

```python
import requests

# Page URL
url = "https://frontify.com/"

try:
    # Use HEAD to avoid downloading the body
    response = requests.head(url, allow_redirects=True)

    # Return the status codes for the page URL provided
    if response.status_code in [200, 404]:
        print(f"{url}: {response.status_code}")
    else:
        print(f"{url}: {response.status_code}")

except requests.exceptions.RequestException as e:
    print(f"Error checking URL: {e}")
```
