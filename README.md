# scalerts
A Python program that aggregates articles from provided RSS feeds, stores the articles in an SQLite database and creates a .xlsx file with only the latest articles in it. 

# Installation Instructions (For Windows)

#### Software required:
* `Python 3.0` and newer versions
* `SQLite3`
* Any Spreadsheet viewer that can open *.xlsx files.

#### Required Modules for Python:
You can easily use `pip install <module_name>` to install these modules.
* `feedparser` module
* `sqlite3` module
* `openpyxl` module

#### Open `Command Prompt` and do the following:
* Add python to your `PATH` variable.
* Migrate to folder containing the file `scalerts.py` by using `cd` command.
* Now you can use `python scalerts.py` to run the file.


#Technical Details

1. 
  * `scalerts.py` takes one RSS feed URL and parses it.
  * `scalertsgoogle.py` is merely an example on how `scalerts.py` can be modified to take multiple RSS feeds and parse them accordingly.

2. The `urllist[]` variable in `scalertsgoogle.py` contains various RSS feeds which were created using [Google Alerts](https://www.google.com/alerts). You can even also use prexisting dedicated RSS feeds like [this](http://www.metal.com/rss/aluminum) or [this](http://timesofindia.indiatimes.com/rssfeedstopstories.cms). 

3. You can find instructions on how to make dedicated RSS feeds for any topic [here](https://support.google.com/alerts/?hl=en#4815700).

4. The program utilises the feedparser module to parse the RSS feeds, the sqlite3 module to establish a connection with a database that stores the articles and the openpyxl module to create a new .xlsx file which contains only the latest articles provided by the feed.

5. On running the program for the first time, one will see the accompanying database file and excel file being created. Henceforth, the database file will be appended with new incoming content and keep increasing in size while the excel file will be overwritten with the new posts.

6. If user wants to use the generated excel file for a later time they must make a backup as the file will get overwritten. They may also access the database directly in such cases.
