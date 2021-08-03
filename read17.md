# Web Scraping

## What is web scraping?

Web scraping is a technique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort. [source](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)

- Important information on web scraping:

  1. Read through the website’s Terms and Conditions to understand how you can legally use the data. Most sites prohibit you from using the data for commercial purposes.

  2. Make sure you are not downloading data at too rapid a rate because this may break the website. You may potentially be blocked from the site as well.

## Inspecting the Website

1. The first thing that we need to do is to figure out where we can locate the links to the files we want to download inside the multiple levels of HTML tags. Simply put, there is a lot of code on a website page and we want to find the relevant pieces of code that contains our data. If you are not familiar with HTML tags, refer to W3Schools Tutorials. It is important to understand the basics of HTML in order to successfully web scrape.

2. On the website, right click and click on “Inspect”. This allows you to see the raw code behind the site.

3. Notice that on the top left of the console, there is an arrow symbol.

4. If you click on this arrow and then click on an area of the site itself, the code for that particular item will be highlighted in the console. I’ve clicked on the very first data file, Saturday, September 22, 2018 and the console has highlighted in blue the link to that particular file.

5. Notice that all the .txt files are inside the ```<a>``` tag following the line above. As you do more web scraping, you will find that the ```<a>``` is used for hyperlinks.

## Python Code

1. Start by importing the following libraries:

```py
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```

2. Set the url to the website and access the site with our requests library.

```py
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```

3. If successful, you should see a ```<response [200]>```

4. Parse the html with BeautifulSoup so that we can work with a nicer, nested BeautifulSoup data structure.

```soup = BeautifulSoup(response.text, “html.parser”)```

5. We use the method .findAll to locate all of our <a> tags.

```soup.findAll('a')```
