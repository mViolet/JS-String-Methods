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
<p>string.prototype.charAt() takes in an index number, and returns the character at that position. If there is nothing there, it gives back an empty string <code>""</code>.</p>
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
<p>string.prototype.charCodeAt() takes in an index and returns the Unicode number of the character at that index. This will always be a number between 0 and 65535. If the index is out of the range for the string, charCodeAt() will return <code>NaN</code></p>
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
<p>string.prototype.concat() concatenates (or joins together) the calling string with any strings passed in as arguments. Strings are joined together as-is, so be mindful of spaces!</p>
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
<p>string.prototype.includes() checks if the calling string contains the string that is passed into it. You can pass in an optional position to tell it when to start searching. .includes() returns a boolean (true or false). It is case-sensitive!
</p><p><em><strong>Parameters accepted:</strong></em><br>
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
<p>string.prototype.indexOf() is a really handy method that takes in a string (the search value),  and returns the index of the first instance of the search value within the calling string. If it isn't found, .indexOf() will return =1. </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>.indexOf() takes in two parameters:</p>
<ul>
</ul><li>search value (required)</li>
<li>position/index to start search (default is 0)</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>someString.includes(‘searchString’, index)</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="match">match</h2>
<p>string.prototype.match() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="repeat">repeat</h2>
<p>string.prototype.repeat() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="replace">replace</h2>
<p>string.prototype.replace() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="search">search</h2>
<p>string.prototype.search() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="slice">slice</h2>
<p>string.prototype.slice() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="split">split</h2>
<p>string.prototype.split() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="substr">substr</h2>
<p>string.prototype.substr() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="toLowerCase">toLowerCase</h2>
<p>string.prototype.toLowerCase() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="toUpperCase">toUpperCase</h2>
<p>string.prototype.toUpperCase() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="trim">trim</h2>
<p>string.prototype.trim() </p>
<p><em><strong>Parameters accepted:</strong></em><br>
</p><p>…:</p>
<ul>
</ul><li>stuff (required)</li>
<li>stuff</li>
<li>stuff</li>

<p><em><strong>Basic usage:</strong></em><br>
</p><p><code>//code</code></p>
<p><em><strong>Some examples:</strong></em></p>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<pre><code>//code

</code></pre>
<p><a href="#list-of-string-methods">Back to the list</a></p>
<h2 id="section"></h2>
<p><strong>That’s it!</strong></p>
<p>Thanks for taking the time to check out my little reference manual on string Methods.<br>
</p><p>Go forth and use the aforementioned methods to your heart’s content ✨</p>
<p>The ultimate reference for JavaScript features can be found at the <a href="https://developer.mozilla.org/en-US/">MDN WebDocs</a></p>

