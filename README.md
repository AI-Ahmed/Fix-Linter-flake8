# Fix Linter flake8

## Description:
* This's The solution for fixing the console problem which we're facing when we decide to install ***Linter-flake8*** for *Python*.

## Why ***Linter-flake8*** doesn't work after installation?
-***Linter-flake8*** default installation for `python 2.7` and if you read the description of the package, you will find that their implementation was for `python 2.7` and not for `python3`.
-Default installation package simulate directly with `python 2.7` and not for `python3` so, you have to install the package using the commands of `python3`.
-Even Entering your **Executable PATH** ONLY will be only mere. Because like I said, you need to install flake8 in terms on `python3`, not `python2`.

## So, What should I do?

1. Install ***Linter-flake8*** From **Atom** IDE and then restart your Program.
2. Check if it actually being installed via your package manager by: `which flake8` in your terminal.
3. Click `Ctrl+Shift+P` to open the Search in **Atom**.
4. search for *Application: Open the Init Script*.
5. Then, Write in the *init.coffee* this code:
    ```coffee
    process.env.PATH = ['usr/local/bin/', process.env.PATH].join(':')
    ```
6. Go To your ***Executable PATH** and paste this path `/usr/local/bin/`.
7. Then, open a new Terminal and execute these couple of commands:
  1. First, enter your **root Mode** by `sudo su`.
  2. Second, go to `cd /usr/local/bin/`.
  3. Third, execute these commands:
    - `python3 -m pip install flake8`
    -`ls`
    -`apm install linter-flake8`
    -`'ls'
    -``python3 -m pip install flake8-docstring`
    -`python3 -m pip install hacking`
#### If you don't install pip, you can install it by `sudo apt-get install pip` Then, you can move on to continue the installation of flake8.
8. close your **Atom** and open it.
9. If you want to disable The ***Max Line Lenght*** you can do that by default it with **0**.
10. ***Smile!***

#### It will be a courtesy from you if you followed me :) <3


# References:
-[flake8 not found](https://github.com/AtomLinter/linter-flake8/issues/18)
-[linter--flake8](https://github.com/AtomLinter/linter-flake8)

# Signature:
![Dr. Xavier](https://user-images.githubusercontent.com/72295771/96151299-8e37a380-0f0b-11eb-8aef-615974b8ce1d.png)
