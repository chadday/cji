# cji
A repo for Columbia Journalism Investigations workshop


## Web scraping with Python

 Welcome to a short tutorial on webscraping with Python presented for CJI's fellows in December 2021. This tutorial aims to provide beginner familiarity with web scraping, with basic Python syntax and some common packages. 

## Why are we doing this

Python is a versatile language that can save you time and help you tell better stories whether by automating tasks, wrangling large datasets or simply putting your analysis all in one reproducable place. It is also a great tool to gather data to use for stories.

A lot of revelatory data doesn't come in a nice, clean format. Many times we have to compile it ourselves. With web scraping, we can do that and more as you'll see.

## Overview

We'll be using:

 - A terminal window
 - The Python interpreter
 - A Python package installer
 - A Jupyter notebook

## Installation

First things first, we're going to do some setup on our computers before we can start writing Python. We will be using Python 3 (preferably 3.6 or higher).

 - Install Python, if not already
 - Install `pip3`
 - Install Jupyter notebooks


## If you're familiar with `git` and already have Python and `pip3`

Clone this repo and then run the code below to install the required packages.

```bash
pip3 install -r requirements.txt

```

You can also install `git` following these [instructions]() and then run the command above. Hint on a Mac, typing `git --version` will likely prompt an install wizard if you have the XCode tools installed.


#### Check your python install

On a Mac, open a Terminal window and type `python3`. (You can find the Terminal by using the spotlight and searching for "Terminal.") If you see something like this:

```
Python 3.6.8 (v3.6.8:3c6b436a57, Dec 24 2018, 02:04:31)
[GCC 4.2.1 Compatible Apple LLVM 6.0 (clang-600.0.57)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

You're in business.

On a Windows machine, if you installed the Microsoft store version, open a command prompt and type `python3` or you can find it in the Start menu.


#### If not installed, install Python

[Mac installer instructions](https://www.python.org/downloads/)

If Windows, I would suggest using the [Microsoft store version](https://www.microsoft.com/en-us/p/python-38/9mssztt1n39l?activetab=pivot:overviewtab) if you're looking to learn. You can also do the full install using the [Windows installer instructions](https://www.python.org/downloads/windows/). Note: Make sure to check the box during the install process to add Python to your path.


#### Install pip3

Short for "Pip Installs Packages," pip is just what it sounds like. It's a package manager that installs python packages. We're going to use it for installing a series of Python packages that we'll use in our tutorial and our scraper.

On Windows, if you installed from the Microsoft store, it should be included.

On Mac, to install pip, open the Terminal. Then copy and paste the commands below into your terminal window. We'll be installing just to our user profile, instead of the machine itself, so we won't run into problems with not being the administrator on the computers.

```
curl https://bootstrap.pypa.io/get-pip.py -o ~/Downloads/get-pip.py
```
Once the file has downloaded and if it is in your Downloads folder, enter this:
```
python3 ~/Downloads/get-pip.py
```

After install, type `pip3` into your terminal and press Enter. A help menu should pop up. If not, make sure it's added to your path, try ```echo $PATH ``` and you should see it added to your PATH.

If you're still having trouble on Windows, this [walkthrough](https://datatofish.com/add-python-to-windows-path/) should help.

#### Install packages one at a time

Now that we have `pip3` installed, we can use it to install another tool we're going to use: Juypter notebooks. 

### What we're installing

[Jupyter notebooks](https://jupyter.org/install) are incredibly powerful, open source environment for Python scripting. We'll be using them to do some tutorials and data work but I use them every day in my job for all kinds of data work.

[requests](http://docs.python-requests.org/en/master/) is a package that allows us to make HTTP requests (i.e. follow urls and return their content) in Python. Now that we've install pip, the installation is easy.

BeautifulSoup is an html parser that will allow us to interact with html and pull the data we want out of it.

[lxml](https://lxml.de/) processes xml and html in Python and is used by BeautifulSoup to parse. 

pyOpenSSL is used by requests and you can read more about it [here](https://pyopenssl.org/en/stable/introduction.html). 

[pandas](https://pandas.pydata.org/) is a data science library for Python.

To install, copy and paste each of these lines into your terminal:

```
pip3 install notebook

pip3 install requests

pip3 install beautifulsoup4

pip3 install -U pyopenssl

pip3 install lxml

pip3 install pandas
```

Now, type:

```
jupyter notebook
```

If you're using a Mac that defaults to `zsh` in the terminal, type:

```
python3 -m notebook
```

A notebook session should pop up in your browser of choice.

Now we're ready to get started.