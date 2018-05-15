# SteemMillionaire
A Steem version of -who wants to be a millionaire-
# Usage

To "install" this game, you will need a simple webserver that can serve static files (Apache will do). You simply upload this git repository into a folder on the web server, and access index.html in your browser.


The game loads a question bank (default questions.json) which will be in the same root directory as index.html. This file contains the game-seperated question sets described in the next section but not randomized just yet.

# Scraping / Question bank

To make question harvesting easier, I am testing a python script in /util that will scrapes sites like indiabix.com for questions until i create a website that houses more questions.

The root directory has questions.json which is the main question file, and another question set stored in questions2.json. The program only reads questions.json.

# Question format

The question bank is simply an array of "games". You can have as many "games" as you like but i am still checking and will be updating more relevant questions that will educating and entertaining at the same time. You select them at the beginning of loading index.html.

	{
		"games" : [
			{
				"questions" : [ ... ]
			},
			{
				"questions" : [ ... ]
			}, ...
		]
	}

Each array of questions has the following format.

1.	The question prompt text is located in the key "question"
2.  "content" is the key for the possible answer texts. "content" must have a length of 4 (4 multiple choices).
3.	The zero-based index of the value in "content" that is the correct answer is located in the key "correct"



	    {
	        "question" : "What is Aurora Borealis commonly known as?",
	        "content" : [
	            "Fairy Dust",
	            "Northern Lights",
	            "Book of ages",
	            "a Game of Thrones main character"
	        ],
	        "correct" : 1
	    }


# SteemMillionaire
