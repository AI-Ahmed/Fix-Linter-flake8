# Fix Linter flake8

## Description:
* This's the solution for fixing the console problem which we're facing when we decide to install ***Linter-flake8*** for *Python3*. It has being tested in ***Linux*** and ***Debian***.

## Why ***Linter-flake8*** doesn't work after installation?
- ***Linter-flake8*** default installation meant to be for `python 2.7` beside if you read the description of the package, you will also find that their implementation was for `python 2.7` not for `python3`.
- Default installation package simulates directly with `python 2.7` not for `python3`. so, you have to install the package using the commands of `python3`.
- Even after inserting your **Executable PATH** will be only mere of spectacular. Because you need to install flake8 in terms of `python3`, not `python2`.

## So, What should I do?

1. Install ***Linter-flake8*** From **Atom** and then restart your IDE.
2. Check if it's actually being installed via your package manager by executing: `which flake8` in your terminal.
3. Reopen your IDE and click `Ctrl+Shift+P` to open the Search in **Atom**.
4. Search for *Application: Open the Init Script*.
5. Then, Write in the *init.coffee* this code:
    ```coffee
    process.env.PATH = ['usr/local/bin/', process.env.PATH].join(':')
    ```
6. Go To your ***Executable PATH** and paste this path `/usr/local/bin/`.
7. Then, open a new Terminal and execute these commands:
    1. First, enter your **root Mode** by `sudo su`.
    2. Second, go to `cd /usr/local/bin/`.
    3. Third, execute these commands:
        - `python3 -m pip install flake8`.
        - `ls`
        - `apm install linter-flake8`
        - `ls`
        - `python3 -m pip install flake8-docstring`
        - `python3 -m pip install hacking`
#### If you didn't install *pip* before, then you can install it by `sudo apt-get install pip` and then, you can move on to continue the installation of flake8.
8. close your **Atom** and open it.
9. If you want to disable The ***Max Line Lenght*** you can do that by `Default: 0`.
10. ***Smile!***

#### It will be a courtesy from you if you start following me :) <3


# References:
- [flake8 not found](https://github.com/AtomLinter/linter-flake8/issues/18)
- [linter-flake8](https://github.com/AtomLinter/linter-flake8)

# Signature:
![Dr. Xavier](https://user-images.githubusercontent.com/72295771/96151299-8e37a380-0f0b-11eb-8aef-615974b8ce1d.png?raw=true)
