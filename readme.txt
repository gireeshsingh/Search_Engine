Program flow:
1. Add all URLs in data/websites.txt
2. Save websites.txt
3. Add words to be ignored to data/discardedWords.txt
4. Save discardedWords.txt
5. Run the SearchEngineRunner.java file
6. It will inform user before creating Trie
7. User will then have the option to add new URLs to the trie
8. The contents of the new URL will be added to the old trie
9. User can add as many additional URLs as they desire
10. User can now search a word or a set of words in the trie
11. Program will generate a ranking of webpages that contain at least 1 occurrence of any of the input words
12. A output file is also created and stored in the "/output" folder with a lot more details containing INPUT, OUTPUT, TRIE SIZE, RANKING, etc
13. You can run the program as many times as you like
14. Press ESC key to terminate the program

Page Ranking Logic:
1. The page that has the most number of occurrences of all the words combined is ranked the highest or the first
2. The page containing 2nd highest number of occurrences has the 2nd rank and so on
3. Each Trie Node that marks the end of the word has a HashMap stored in it
4. This hashmap contains the list of pages that contain the word
5. With URL as keys and the number of occurrences in those URLs as values

For example: The trie node of APPLE will have the following hashmap entries
		//			(URL	containing Apple)	:	(Occurences of Apple in that URL)
		{	"https://www.fitnessclub.com/" 		:	3,
			"https://www.onlinegrocery.com/"	:	24,
			"https://www.healthyrecipes.com/"	:	15
		}

Technology Used:
	-Java
	-Swing
	-Jsoup
	
Algorithm: Sorting to rank the webpages by the number of occurrences of words

Data Structure: Trie