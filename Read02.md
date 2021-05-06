HTML Book Readings
Resource: Duckett HTML Book - Various parts cited from the resource

Chapter 2 - Text
Structural markup:
The elements that you can use to describe both deadings and paragraphs
Semantic markup:
Provides extra information; such as where emphasis is placed in a sentence, that something you have written is a quation (and who said it), the meaning of acronyms, and so on. Do not use them to format text but instead it provides better definition to other programs, screen readers and search engines. Use only CSS to format. Above quoted from Duckett HTML Book
<h1>, <h2>, <h3>, ,<h4>, <h5>, <h6> are all heading tags. They all display text in a larger font with <h1> being the largest down to <h6> being the smallest. These are block elemnts and require the closing tag. Structural.
<p> Paragraph tag. Block element. Requires closing tag </p>. Used to create a paragraph. Structural.
<b> <i> Bold text tag and italic tag. Both are Semantic, inline and require the closing tag of </b> </i>.
<sup> <sub> Superscript & Subscript. Both are Semantic, inline and require the closing tag </sup> </sub>.
HTML is considered white space collapsing meaing that the browser will remove spaces if there is 2 or more or blank lines. This helps to create a better readability of the code.
<br /> & <hr /> Inline elements that are self closing meaning no </br> or </hr> needed. <br /> used to force a line break and <hr /> used to force a line break adding a line. These are also known as empty elements that have no text between the open & close tags.
<strong> Semantic tag used inside others, mostly a <p>. Requires a closing tag of </strong> with the text between the tags. Places strong importance on the text between the tags. By default, browsers will mark this tag and bold.
<em> Semantic tag used inside others, mostly a <p>. Requries a closing tag of </em> The text to emphasis is between the tags. By default, browsers will show this as italic.
<blockquote> Block element. Semantic tag. Requries a closing tag of </blockquote>. Also needs an attribute passed of cite="http://website/page??? and then the text to quote between the open & closing tags usually wrapped in a <p>. Browsers tend to indent this text. Example:
 <blockquote> cite="website address/page">
    <p>some text that is quoted</p>
 </blockquote>
<q> Semantic tag. Inline usage. Used for shorter quotes and places "" around the elements between the open & close tag. Requires a closing tag of </q>.
<abbr> Semantic tag. Inline usage. To define an abbreviation or an acronym. Requires a title attribute to be passed and the abbrevation/acronym between the tags. Requires a closing tag </abbr> This tag normally placed inside a wrapping <p>
 <p><abbr title="Her Majesties Service">HMS</abbr>Her Majesties Service.</p>
<cite> Semantic tag. Inline usage. Used to cite a book, film, paper or some type of publication. Requries a closing tag </cite>. Browsers will show the text between the tags as italic.
<dfn> Semantic tag. Inline usage. Used to mark the text between the tags as defining instance. Requires a closing tag </dfn>. Some browsers will display as italic but some will not change the appreance. Mainly for screen readers & other programs/services.
<address> Semantic tag. Used to define the contact details for the author of the page. Can contain an address, email or phone. Browsers often dislay at italic. Requires a closing tag </address> and containers others tags to define the information to display. Could be an <a> or <p>.
<ins></ins> & <del></del> Semantic tags. Inline usage. INS marks a word as inserted by underlining it. DEL makrs a word as deleted by putting a line through it.
<s></s> Semantic tag. Inline usage. The content between the tags will be displayed with a line through it. This to mark an item no longer accurate or relevent but should not be deleted.
Chapter 10 - Introducing CSS
Resource: Duckett HTML Book - Various parts cited from the resource CSS is used to style and layout your web pages to make them more arrtactive, controlling the design of them using CSS.

This is accomplished by changing the font type, font size, color of text, color of background, applying the rules to certain tag elements and many more options to assign the style.

Imagine that CSS places a box around every HTML element and by using CSS, you can style that box and all the content inside the box.

Example of styles that can be applied to boxes are:

Width & Height
Borders (color, width & style)
Background color and images
Positioning in the browser window
Example of styles for text that can be applied are:

Typeface
Size
Color
Istalics, bold, upercase, lowercae, small-caps
Lits, tables and forms can also get specific and specialied sytling from CSS

CSS syntax contains two parts. A selector and a decloration. The decloration is usually in {} brackets. Declarations are split into 2 parts seperated by a : where item on the left is the property and item on the right is the value and the line ends with a ;. The most basic form of a selector is the HTML tag name and these can be combined with a , between them.

CSS can be placed in the same HTML between the <style></style> tags in the <head></head> section. They can also be specified inline right behind the HTML tag.

The best way is to use an external CSS file and then linking it to your HTML file using the <link /> self closing tag in the <head></head> section of your HTML file. The <link /> requires 3 attributes:

href = specifies the path and filename to be imported and has an extension of “CSS”
type = Specifies the type of document being linkted to. Value must be “text/css”
rel = Specifies the relationship between the file and the HTML page. The value must be “stylesheet” when linking to a CSS file. NOTE: all 3 of these values must be in "" and all lowercase.
There are many ways to use the selector for CSS and the following are the most common:

* () - Universal - Applies to all elements in the document. This is a global selector.
h1, h2 {} - Type Selector - Matches element names.
.note {} - Class Selector - Selects the elements that have a class value set that matches the value after the “.”. Values can be combined example h1.note () will select the H1 element that has a class value set to “note”.
#idName {} - ID Selector - Selects the element that as an ID set matches the value after the “#”. Reminder that ID are unique so if you have the same ID applied to a few elemnts, the CSS style will be applied to all of those.
li>a {} - Child Selector - Targets only <a> elements that are children of a <li> element. Will not target other <a> elements.
p a {} = Descendant Selector - Targets any <a> element that sit inside a <o> element. Other elemnts between has no impact. The element being targeted does not have to be a direct child of the parent element.
h1+p {} - Adjacent Sibling - Targets the first <p> element direclty after any <h1> element but only direct sibling. Will not target other childred.
h1~p {} - General Sibling - Targets all <p> elements taht are directly after the <h1>. It matches an element that i a sibling of another. Does not have to be the directly preceding element.
CSS Rules cascade and a rule further down in the file could make changes to the rule listed before.

Last Rule - If two selectors are identical, the latter of the two will take priority.
Specificity - If one selector is more specific than the others, the more specific rule will take precedence.
Important - You can apply !important directly after the value to indicate that it should be considered more important than other rules that apply to the same element.
This cascading method helps you write simpler CSS styles so you can apply the generic rules first at the top of the file and then specify the more restrictive at the bottom and override the properties on individual elements that need to appear different.

Some CSS properties are inherited automatically by their children of the parent where the property is set. font-family is one of these properties. You can also force a property to inherit the value of it’s parent by specifying the property name then the “;” and the inherit value assigned to the property. This will then force the element to inherit the value set to its parent above.

Using a seperate style sheet (CSS file) has many benefits

All pages or certain can share the same CSS file.
Has a clear seperation between the different parts of the web page being HTML & CSS.
Easier to maintain, edit and debug.
JavaScript Reading
Chapter 2 - Basic JavaScript Instructions
Resource: Duckett HTML Book - Various parts cited from the resource

Statements - A script (JavaScript File) is a series of instructions that a computer can follow line by line. Each individual instruction or step is known as a statement ending with a ;.
JavaScript is a case sensitive language. myName is different then MyName and both are different then myname or MYNAME.
Statements usually being a new line and statements can be organized into code blocks where the start/end of the code block are the { statements inside to form a code block }.
Comments can be single line starting with a // or multi line starting with a /* and ending with a */
Variable is an item you create in the code as a satement that will be assigned a name that you can use to refer to the item and a value which is the data that the item will store. Varibales are key to any program to remember and process data.
The data or value assigned to a variable can change over time.
Variables are declared with the let keyword in JS (JavaScript) then a space and the name you are assigning to this variable. You can opptionally leave the variable with no value at this time or assign it a value with a space after the name then the “=” where the “=” means assignment operator and then the value to the right of the “=” sign.
Data types are strings, numbers or boolean (true/false).
Strings are enclosed in ' ' where numberic and boolean values are not. Numbers are just tpyed and boolean is just assigned true or false.
changing the value of a varibale that is already declared with the let keyboard doe not require the use of the word let again. Just type the variable name on the left of the “=” and the new value on the right of the “=”.
Array is a special type of varibale that stores a list of values instead of just one value.
Array are defined the same way but with a [ 10, 1, 13, 8 ] on the right of the “=” sign for numeric values or the same way but replacing the numbers with string values inside single quotes like [ 'name1', 'name2', 'name3' ]
Values position in an array are maintained by an index numberic value starting at 0 for the first item, 1 for the second item and so on.
You access the value by using the array name then [] with the index numeric value of the value needed. Example myArray[2] will get you the 3rd value in an array called “myArray”.
Variables have a lot of extra methods that are automatically available to them. One for an array is called length. This will return a value of the number of items in the array. Example: let numMyArray = myArray.length will return a number and store it in the numMyArray variable. If the array has 3 values defined, the number returned would be 3.
The value in an array can be changed. You have an array that has 3 items and you want to change the last item you can do so by accessing the array with the index number in [ ] and then assiging it the new value. Example:
let myArray = [1, 2, 3]
myArray[2] = 4
console.log(myArray)
will return myArray showing [1, 2, 4].

Operators are used heavily in JS
= - assignment.
`+’ - combining for strings and addition for numbers.
Mathematical operators are:
”+” addition, “-“ substraction, “*” multiplication, “/” division, “++” increment by 1
”–” decrement by 1, “%” modulus (return the remainder of division of 2 numbers)
Order of execution follows the set defined rules of mathematics.
There is only 1 string operator and that is the “+” used to join strings together.
When you place ' ' around a number you just made that number a string and you can’t perform mathematic operations with it (unles you convert it back to a number).
If you also try to combine a number with a string using the “+”, JS will convert the number to a string and join it to the string.
If you try to use math operators on strings, you will get get a return value of NaN which means “Not a Number”.
Chapter 4 - Decisions Statements (part of the chapter)
Resource: Duckett HTML Book - Various parts cited from the resource

There are two parts to a decision.
Expression is evaluated which returns a value.
Conditional statement says what to do in a given situation.
Various operators are available for the condition evaluation. There are == is equal, != is not equal, === strict equal, !== strict not equal. Strict comparison checks the value and data type while is equal just checks the value.
There are a few other operators which are: > greater than, < less than, >= greater than or equal to, <= less than or equal to.
Coompasison operators are enclosed in ( ) and containers two operands and one operator. The operator is between the two operands. (myAge >= yourAge) this checks if myAge variable containing a number is greater than or equal to yourAge container a number. It will return a true or false depending on the value of the two variables.
An operand can be an expression as each expression evalyates into a single value.
Locgial operators allow you to compare the results of more than one comparison operator. The expressions are on each side of the logical operator and are enclosed in ( ) depending on the type of locial operator used, the 2nd and more expressions may not get checked.
Logical operators are: &&logical AND, || logical OR, ! logical NOT.
if then else statement is one of the most used statements for decision making in any language.
If statement checks a condition and if true will run the first set of code in the ` { } block. If the statement evaluates to false, it will skip the block and go to code after the block or if the statement has an else block, it will run that set of stements and then resume the code after the complete if` statement.
Evaulation is done by comparing one value in the script to what you expect it might be. The result will be a boolean being true or false.
