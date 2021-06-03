---


---

<h1 id="string-methods-in-javascript">String Methods in JavaScript</h1>
<p>Here is a rundown of some useful string methods in JavaScript.<br>
Each method listed below will include the following:</p>
<ul>
</ul><li>A description of what it does</li>
<li>Brief explanation of how it works</li>
<li>Time complexity (if appropriate)</li>
<li>Three code examples</li>

<p>Here is a list of all the methods I will cover, in case you want to jump to a particular section!</p>
<h3 id="list-of-string-methods">List of string Methods</h3>
<p><a href="#charAt">charAt</a><br>
<a href="#charCodeAt">charCodeAt</a><br>
<a href="#concat">concat</a><br>
<a href="#includes">includes</a><br>
<a href="#indexOf">indexOf</a><br>
<a href="#match">match</a><br>
<a href="#repeat">repeat</a><br>
<a href="#replace">replace</a><br>
<a href="#search">search</a><br>
<a href="#slice">slice</a><br>
<a href="#split">split</a><br>
<a href="#substr">substr</a><br>
<a href="#toLowerCase">toLowerCase</a><br>
<a href="#toUpperCase">toUpperCase</a><br>
<a href="#trim">trim</a></p>
<h2 id="charAt">charAt</h2>
<p><code>String.prototype.charAt()</code> takes in an index number, and returns the character at that position. If there is nothing there, it gives back an empty string <code>""</code>.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>charAt() accepts one parameter:</p>
<ul>
</ul><li>index</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.charAt(index)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const str = "Hello world"
str.charAt(2)  

//returns: "l"
</code></pre>
<pre><code>const str = "Hello world"
str.charAt()  

//returns: "H" because the default is 0
</code></pre>
<pre><code>const str = "Hello world"
str.charAt(99)  

//returns: ""
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="charCodeAt">charCodeAt</h2>
<p><code>String.prototype.charCodeAt()</code> takes in an index and returns the Unicode number of the character at that index. This will always be a number between 0 and 65535. If the index is out of the range for the string, <code>.charCodeAt()</code> will return <code>NaN</code></p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>charCodeAt() takes in one parameter:</p>
<ul>
</ul><li>index</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.charCodeAt(index)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const str = "Hello World"
str.charCodeAt(2)  

//returns: 108, which is where lowercase l is in the ASCII table
</code></pre>
<pre><code>const str = "Hello World"
str.charCodeAt()  

//returns: 72
</code></pre>
<pre><code>const str = "Hello World"
str.charCodeAt(99)  

//returns: NaN
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="concat">concat</h2>
<p><code>String.prototype.concat()</code> concatenates (or joins together) the calling string with any strings passed in as arguments. Strings are joined together as-is, so be mindful of spaces!</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><li>one or more strings</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.concat(string, string, string…)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const place = 'World'
console.log('Hello'.concat(" ", place))

//prints "Hello World"
</code></pre>
<pre><code>''.concat('Hello', ', ', 'How are you?')  

//returns:  "Hello, How are you?"
</code></pre>
<pre><code>
//using the spread operator to spread an array into .concat()
const greeting = ["Well ", "hello", " ", "there", "!"]
console.log("".concat(...greeting))

//prints "Well hello there!"
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="includes">includes</h2>
<p><code>String.prototype.includes()</code> checks if the calling string contains the string that is passed into it. You can pass in an optional position to tell it when to start searching. <code>.includes()</code> returns a boolean (<code>true</code> or <code>false</code>). It is case-sensitive!</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>This method can take two parameters:</p>
<ul>
</ul><li>search string (required)</li>
<li>index to start search (the default is 0)</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.includes(‘string’, index)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const drinks = "We have Coffee, Tea, and Soda"
drinks.includes("Coffee")

// returns true
</code></pre>
<pre><code>const drinks = "We have Coffee, Tea, and Soda"
drinks.includes("coffee")

// returns false!!
</code></pre>
<pre><code>const sentence = 'How now brown cow?'
sentence.includes('How', 1)  

// returns false because it started searching at position 1!
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="indexOf">indexOf</h2>
<p><code>String.prototype.indexOf()</code> is a really handy method that takes in a string (the search value),  and returns the index of the first instance of the search value within the calling string. If it isn’t found, <code>.indexOf()</code> will return <code>-1</code>. It’s case sensitive!</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>.indexOf() takes in two parameters:</p>
<ul>
</ul><li>search value (required)</li>
<li>position/index to start search (default is 0)</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.indexOf(‘searchString’, index)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const sentence = "The Antarctic blue whale is the largest animal on Earth."
sentence.indexOf('blue')  

// returns 14
</code></pre>
<pre><code>const sentence = "It is also the loudest animal on Earth, with a call that can reach 188 decibels."
sentence.indexOf('earth')  

// returns -1
</code></pre>
<pre><code>const sentence = "For context, a jet at take-off is about 150 decibels"
sentence.indexOf('context', 5)  

// returns -1 because it started searching at position 5!
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="match">match</h2>
<p><code>String.prototype.match()</code> takes in a Regular Expression, and returns an Array based on what matches the Regular Expression.<br>
It will return only the first match if the <code>g</code> flag is not used.<br>
Anything passed into it will be converted into a regular expression object.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><p></p><li>a regular expression object</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.match(regExp)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const sentence = "Cheesy pizza is totally tubular. I love pizza!"
sentence.match(/PIZZA/i)

//returns  ["pizza", index: 7, input: "Cheesy pizza is totally tubular", groups: undefined]
</code></pre>
<pre><code>const sentence = "Cheesy pizza is totally tubular. I love pizza!"
sentence.match(/PIZZA/gi)

//returns  ["pizza", "pizza"]
</code></pre>
<pre><code>const sentence = "One, two, three"
//searching for a digit
sentence.match(/\d/gi)
// returns null    (no match is found)

sentence.match()
//returns ["", index: 0, input: "One, two, three", groups: undefined]
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="repeat">repeat</h2>
<p><code>String.prototype.repeat()</code> copies a string a number of times and concatenates the result. It copies the string it was called upon. It’s pretty straightforward with some examples!</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><p></p><li>an integer between 0 and `+Infinity`</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.repeat(num)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>'hello!'.repeat(3)
//returns "hello!hello!hello!"
</code></pre>
<pre><code>const sentence = 'Look at the exclamation points'
console.log(sentence + '!'.repeat(10))
// prints  "Look at the exclamation points!!!!!!!!!!"
</code></pre>
<pre><code>'.'.repeat(Number("3"))
//returns "..."
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="replace">replace</h2>
<p><code>String.prototype.replace()</code> is pretty powerful. It returns a string that has had parts of it replaced (based on what was passed in). If you pass in a string, it will only replace the first instance of the match!<br>
You can get it to behave more like <code>String.replaceAll()</code> by using a regular expression with a global flag, <code>g</code></p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p><code>.replace()</code> takes two parameters:</p>
<ul>
</ul><li>a string or a regular expression</li>
<li>a replacement string or a callback function</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.replace(matchThis, replaceWithThis)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const fruits = "Apples, Cookie, Cookie, Kiwis, Bananas, Cookie"
//replaces only first match:
fruits.replace("Cookie", "Plum")
//returns  "Apples, Plum, Cookie, Kiwis, Bananas, Cookie"  

//replaces all, and is case-insensitive!
fruits.replace(/cookie/gi, "Mango")  
//returns  "Apples, Mango, Mango, Kiwis, Bananas, Mango"
</code></pre>
<pre><code>const ducks = "duck, duck, goose, duck, gopher, goose"  
ducks.replace(/goose|gopher/g, match =&gt; { return (match === 'gopher') ? 'Found-A-Gopher' : 'Found-A-Goose' })  

//returns
"duck, duck, Found-A-Goose, duck, Found-A-Gopher, Found-A-Goose"
</code></pre>
<pre><code>const s = "6 All the11 digits sh8ould be remo0ved 8 fr1om this s7tr0ing"
const digits = []
const digitsRemoved = s.replace(/\d/g, match =&gt; {
	digits.push(match)
	return ""
})

console.log(digitsRemoved, digits)

//prints
"All the digits should be removed from this string"
[ "6", "1", "1", "8", "0", "8", "1", "7", "0" ]
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="search">search</h2>
<p><code>String.prototype.search()</code> checks a string for a match. It matches using a regular expression. If there’s a match, the index will be returned, otherwise <code>-1</code> is the return value.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><li>a regular expression object</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.search(regexp)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const colors = "blue Grey yellow GrEy orange GREY grey pink purple"
colors.search(/grey/gi)

// returns 5
//notice only one index is returned. .search() returns only the index of the first match
</code></pre>
<pre><code>const expression = new RegExp(/[a-z]/gi) 
const lettersNums = "82738000c09a78c7s" 
lettersNums.search(expression)  

// returns 8
</code></pre>
<pre><code>const threeNums = new RegExp(/\d{3}/i) 
const fourNums = new RegExp(/\d{4}/i)
const str = "23ab fc333 az zza22" 

str.search(threeNums)  
// returns 7

str.search(fourNums)
// returns -1
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="slice">slice</h2>
<p><code>String.prototype.slice()</code> returns a “slice” of a string. It commonly takes in two arguments - the index of where to start the slice, and the index after the end of the slice. It doesn’t affect the original string.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p><code>.slice()</code> can take two parameters:</p>
<ul>
</ul><li>the start index (required)</li>
<li>the end index</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someStr.slice(startIndex, endIndex)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const pizzaString = "This string has pizza in it!"
const word = pizzaString.slice(16, 21) 
console.log(word)  

//prints "pizza"
</code></pre>
<pre><code>//without the 2nd argument
const str = "Get the second half!"
const secondHalf = str.slice(str.length/2) 
console.log(secondHalf)  

//prints  "cond half!"
</code></pre>
<pre><code>const str = "Get the last three characters!" 
const lastThree = str.slice(-3)
console.log(lastThree)  

//prints  "rs!"
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="split">split</h2>
<p><code>String.prototype.split()</code> does just that. It “splits” a string apart - however it doesn’t affect the original string. <code>.split()</code> returns an array of substrings.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p><code>.split()</code> can take two parameters:</p>
<ul>
</ul><li>a separator</li>
<li>a limit</li>
<p>Note: The limit tells <code>.split()</code> the maximum number of entries that can be in the array of substrings.<br>
If no separator is passed in, It will return an array containing the string it was called on.</p>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.split(separator)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const words = "one Two Three"
console.log(words.split(" ")) //prints [ "one", "Two", "Three" ]
console.log(words.split())    //prints [ "one Two Three" ]
</code></pre>
<pre><code>const phone = "123-456-7890"
const newPhone = phone.split("-").join(".")
console.log(newPhone)  

//prints 123.456.7890
</code></pre>
<pre><code>const str = "letters &amp; spaces &amp; things"
const splitStr = str.split("", 9)
console.log(splitStr)  

//prints [ "l", "e", "t", "t", "e", "r", "s", " ", "&amp;" ]
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="substr">substr</h2>
<p><code>String.prototype.substr()</code> is a lot like <a href="#slice"><code>.slice()</code></a>, in that it returns a substring of the string it is called on. It takes in two values:  where to start the substring, and how many characters the substring should be.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><li>startIndex</li>
<li>length</li>
<p>Note: The length value is capped at the string’s length, so +length or -length. It will count backwards from the end of the string for negative values like we’ve seen before.</p>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someStr.substr(startIndex, number)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const str = "hello there"
const word = str.substr(0, 5)
console.log(word)  

//prints "hello"
</code></pre>
<pre><code>const str = "hello there"
const word = str.substr(-5)
console.log(word)  

//prints "there"
</code></pre>
<pre><code>const str = "hello there"
const words = str.substr(-99)
console.log(words)  

//prints "hello there"
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="toLowerCase">toLowerCase</h2>
<p><code>String.prototype.toLowerCase()</code> returns a lowercase version of the string it’s called on.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><li>none!</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.toLowerCase()</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const yell = "I'm NOT YELLING!"
const noYell = yell.toLowerCase()
console.log(noYell)  

//prints "i'm not yelling!"
</code></pre>
<pre><code>'make THIS all Lowercase'.toLowerCase("Ignore this")

//prints "make this all lowercase", even with the unneeded argument
</code></pre>
<pre><code>//useful for when you need to avoid case
const words = ["Banana", "BANANA", "Apple", "Grape", "Banana"]

const noBananas = words.filter(word =&gt; word === "banana")
const bananas = words.filter(word =&gt; word.toLowerCase() === "banana") 

console.log(noBananas, bananas)  

//prints
Array []
Array(3) [ "Banana", "BANANA", "Banana" ]
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="toUpperCase">toUpperCase</h2>
<p><code>String.prototype.toUpperCase()</code>, you guessed it, behaves pretty much like <a href="#toLowerCase"><code>.toLowerCase()</code></a>, except it makes everything uppercase.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><li>None needed!</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.toUpperCase()</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const string = "abc123def456"
const upper = string.toUpperCase()
console.log(upper)  

//prints "ABC123DEF456"
</code></pre>
<pre><code>true.toString().toUpperCase()  

//returns "TRUE"
</code></pre>
<pre><code>//useful for searches
const pasta = ["gnocchi", "Bucatini", "Spaghetti", "linguine", "spaghetti pasta"] const spaghetti = 
pasta.filter(words =&gt; words.toUpperCase().includes("SPAGHETTI")) console.log(spaghetti)  

//prints [ "Spaghetti", "spaghetti pasta" ]

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="trim">trim</h2>
<p><code>String.prototype.trim()</code> trims whitespace off of both the beginning and end of a string. That’s all it does! It’s pretty awesome.</p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><ul>
</ul><li>none!</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.trim()</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>const words = "   Get that whitespace outta here "
console.log(words.trim())  

//prints "Get that whitespace outta here"
</code></pre>
<pre><code>const words = "  but the space in   between stays   "
console.log(words.trim())  

//prints "but the space in   between stays"
</code></pre>
<pre><code>const spacey = [" Clean ", " up", " the ", " spaces!! "]
const noSpacey = spacey.map(el =&gt; el.trim()) 
console.log(noSpacey)  

//prints [ "Clean", "up", "the", "spaces!!" ]
</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="section"></h2>
<p><strong>That’s it!</strong></p>
<p>Thanks for taking the time to check out my little reference manual on string Methods.<br>
</p><p>Go forth and use the aforementioned methods to your heart’s content ✨</p>
<p>The ultimate reference for JavaScript features can be found at the <a href="https://developer.mozilla.org/en-US/">MDN WebDocs</a></p>

