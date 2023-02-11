# UOCIS322 - Project 3 #

JQuery and asynchronous requests.

Worked on by Joshua Muzi, jmuzi04@gmail.com

Further details below

## Overview

The program is a simple anagram game designed for English-learning students in elementary and middle school. It presents a list of words to students and an anagram. The anagram is a jumble of some of the words, which are randomly chosen. Students attempt to type words that can be created from the jumble. When a matching word is typed, it is added to a list of solved words.

The vocabulary word list is fixed for one invocation of the server, so multiple students connected to the same server will see the same vocabulary list but may have different anagrams.

## How it works by Josh Muzi

* The vocab.html handles all changes to the webpage whether that be from any type of button pressed on the keyboard,
* using the keyup function the event key is check then ran through ajax interaction working with the flask_vocab.py file
* which takes the #attempt arguments and runs logic to check for all types of matches to then return a jsonified responses
* which the vocab.html file will take within function(response) to update the webpage or upon the game being over redirecting to the success page

*To run the docker/webpage:

* docker build -t myimage .  
* docker run -p 5001:5000 myimage 













## Grading Rubric

* If your code works as expected: 100 points. This includes:
	* AJAX in the frontend (`vocab.html`)
	* Logic in the backend (`flask_vocab.py`)
	* Frontend to backend interaction (with correct requests and responses) between `vocab.html` and `flask_vocab.py`.
	* Basically the webpage should handle validation WITHOUT any refreshes.
* If the game isn't fully functional as described, **40 point** will be docked.

* If messages are not displayed correctly in the webpage, 30 points will be docked. Expected behavior is notifying whether (a) the word typed is not in the vocabulary, or (b) the word cannot be made from the anagram; and in the case of a match, the word should be written somewhere along with the rest of the matched words.

* If none of the functionalities work, 30 will be assigned assuming
    * `credentials.ini` is submitted with the correct URL of your repo,
    * `Dockerfile` builds without any errors, and an instance runs without crashing.
    * `Dockerfile` and `README` are updated with your name and email.

* If the `Dockerfile` doesn't run, build or is missing, 5 will be assigned.

* If `credentials.ini` is not submitted or the repo is not found, 0 will be assigned.
	 

## Authors

Michal Young, Ram Durairajan. Updated by Ali Hassani.