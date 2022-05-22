# functionalWhiteboarding

// Functional White Boarding

// Erin McCulley

// Prompt # 1

URLs cannot have spaces. Instead, all spaces in a string are replaced with %20. Write an algorithm that replaces all spaces in a string with %20.
You may not use the replace() method or regular expressions to solve this problem. Solve the problem with and without recursion.
Example
Input: "Jasmine Ann Jones"
Output: "Jasmine%20Ann%20Jones"

// Language - Javascript

// Pseudo Code

Get a string, see if string has spaces
	if no spaces, go ahead and return
	if yes spaces, find a way to split string
		replace space with ’%20’
	if !=String
		return “eyyy give me a string here”

// Code Code

// Recursive version of this

	const urlify = (string) => {
		//if(string!=String) return “eyyy give me a string here”
		if(string.includes(“ “)) {
			return urlify(string.slice(0, string.indexOf(“ “)) + “%20” + string.slice(string.indexOf(“ “) + 1))
			} else {
				return string;
			}
		}

// Version without recursion 

	const urlify = (string) => string.split(‘ ‘).join(‘%20’); 

// Version with error handling from jsFiddle trial

const urlify = (string) => {
    if(typeof(string) != "string") {
    	return "yo, this isn't a string";
     }
     if(string.includes(" ")) {
			return urlify(string.slice(0, string.indexOf(" ")) + "%20" + string.slice(string.indexOf(" ") + 1))
			} else {
				return string;
			}
   }
    
    console.log(urlify(5));

	output =  “yo, this isn’t a string”

		
