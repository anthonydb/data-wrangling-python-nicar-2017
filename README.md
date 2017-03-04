# Data Wrangling With Python: NICAR 2017
This repository contains materials for "Data Wrangling With Python," a hands-on session presented at the 2017 Investigative Reporters and Editors NICAR conference in Jacksonville, Fla.

The code covers basic import, transformation, and export of data from CSV files. Output formats include JSON and SQL table creation statements.

## What You'll Need
This code was written and taught on MacOS Sierra using Python 3.6; it should work fine on Python 2.7 as well as Python 3.5+. It's not been tested on Windows. I recommend setting up a [virtual environment](http://docs.python-guide.org/en/latest/dev/virtualenvs/) and then installing the following dependencies:
- [Jupyter Notebook](http://jupyter.readthedocs.io/en/latest/install.html)
- [Requests](http://docs.python-requests.org/en/master/user/install/)
- [agate](http://agate.readthedocs.io/)
- [csvkit](https://csvkit.readthedocs.io)

Here are the steps:

## Setup for Jupyter Notebook Exercises

 1. Open your terminal and navigate to the Desktop:

 `cd ~/Desktop`

 2. Clone this repository:

 `git clone https://github.com/anthonydb/data-wrangling-python-nicar-2017.git`

 3. Change to the project directory you just cloned:

 `cd data-wrangling-python-nicar-2017/`

 4. Set up your virtual environment. We'll call it 'nicar':

 ``virtualenv nicar``

 ``source nicar/bin/activate``

 5. Install your dependencies:

 `pip install agate csvkit requests jupyter`

 6. Now you can run Jupyter Notebook:

 ``jupyter notebook``

 7. Jupyter Notebook will open in your default browser on ``localhost:``, and you will see a list of files in the directory. The most important file for this exercise is the Census 2010 data contained in `us_counties_2010.csv`.

 8. Next, using the "New" menu at the top right of the Jupyter Notebook app, create a new notebook matching the version of Python on your system.

 9. Now, you can paste in the code found in the .ipynb file in this repository and run it to follow the tutorial.

 10. When you're done, run ``ctrl+c`` in the terminal to close Jupyter Notebook. Then ``deactivate`` to exit your virtual environment.

## Trying csvkit Commands

You can run the commands in the file [csvkit-notes.md](https://github.com/anthonydb/data-wrangling-python-nicar-2017/blob/master/csvkit-notes.md) in your terminal. Make sure the virtual environment is activated.

## Notes and Further Reading

This NICAR 2017 hands-on class was loosely inspired by the structure of a [NICAR 2016 class](https://github.com/aepton/python-data-wrangling) taught by Jacqueline Kazil and Abraham Epton.

Suggested resources to learn more about Python and data:

- [CSV File Reading and Writing: Python docs](https://docs.python.org/3/library/csv.html)
- [JSON encoder and decoder: Python docs](https://docs.python.org/3/library/json.html)
- [The Hickhiker's Guide to Python](http://docs.python-guide.org/en/latest/)
- [Data Wrangling With Python](http://shop.oreilly.com/product/0636920032861.do) by Jacqueline Kazil and Katharine Jarmul
