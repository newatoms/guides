> **The goal of this guide:** You will learn how to extract information from certain web pages using [developer tools](guides/fixing-errors/readme.md), [node.js](http://blog.modulus.io/absolute-beginners-guide-to-nodejs) and [X-Ray](https://www.npmjs.com/package/x-ray).

# Web scraping with [node.js](http://blog.modulus.io/absolute-beginners-guide-to-nodejs) an [x-ray](https://www.npmjs.com/package/x-ray)

You can of course start here at [hackertyper](http://hackertyper.com/) and do your swordfish magic! 🤓

Web scraping enables you to extract information from the web and put it in a more workable format (*.json*, *.csv*, *excel*, *google spreadsheets*).     

## First things first

1. Create a file ```'filename'.js``` in your designated folder. In this file you will write your code. Then, create a folder where your information will be displayed ```results.json```.

* Open the [Terminal](http://www.macworld.co.uk/feature/mac-software/get-more-out-of-os-x-terminal-3608274/) application on your mac, go to the folder where you created your files by typing ```cd 'path to your folder'``` enter.

* Install node.js: ```npm install node``` and enter. Then you need X-Ray: ```npm install x-ray``` enter.

## Lets start scraping

In this example we extract the 'experience' information from a certain LinkedIn profile. Important is that you don't log in! Or else the html code is different from this example.

### Open Chromes Developer tools

In the Chrome web browser open the devtools with ```cmd-alt-i``` and click on the parent element:

<img src="../images/devtools-web-scraping.png" width="800">

> With scraping you need to get comfortable with developer tools and with reading html code.

We search 🕵 from top to bottom to find what we want:

* We want all the information of experience. ```class='positions'```
* We want the title of each experience: 'Content developer'. ```class='item-title'```.
* We also want the organisation of each title: 'New Atoms'. ```class='item-subtitle'```.
* finally, we want the date and time the person was active under that title and organisation: ```class='.date-range'```

This ↓ is all the code we need. Not very scary, aint it?

    var x = new require('x-ray')()

    x(
      'https://linkedin.com/in/some-person',
      {
        items: x(
          '.position',
          [ {
            title: '.item-title',
            organisation: '.item-subtitle',        
            time: '.date-range'
          } ]
        )
      }
    ).write('results.json')

1. Create a variable that will execute your x-ray. ```var x = new require('x-ray')()```
* Now ```x``` will look at a certain Linkedin url.
* Next, the code will run the containing information of the called classes.
* With ```.write('results.json')``` the scraped information will print out the information in your ```results.json``` file on your computer.
* To actually see 👀 your scraped information in your results.json file go to your terminal and call the code with typing: ```node 'filename'.js```. Voila! There it is! 🎉      

## Results in your .json file:

You can convert these .json files into .csv files to eventually import it in spreadsheet programs or [Open Refine](http://openrefine.org/).

    {
      "items": [
        {
          "title": "Content Developer",
          "organisation": "New Atoms",
          "time": "juni 2015 – heden (10 maanden)"
        },
        {
          "title": "Minor Research- and Datajournalism",
          "organisation": "Hogeschool Windesheim",
          "time": "januari 2015 – heden (1 jaar 3 maanden)"
        },
        {
          "title": "News and Media",
          "organisation": "Hogeschool van Amsterdam",
          "time": "september 2012 – heden (3 jaar 7 maanden)"
        },
        {
          "title": "Service Staff",
          "organisation": "Bar Brouw",
          "time": "juli 2014 – heden (1 jaar 9 maanden)"
        },
        {
          "title": "News Editor",
          "organisation": "MeerRadio & MeerTelevisie",
          "time": "april 2014 – juli 2014 (4 maanden)"
        },
        {
          "title": "Service Staff",
          "organisation": "KHL",
          "time": "juli 2011 – juli 2014 (3 jaar 1 maand)"
        },
        {
          "title": "News Reporter",
          "organisation": "MeerRadio & MeerTelevisie",
          "time": "januari 2014 – april 2014 (4 maanden)"
        }
      ]
    }
