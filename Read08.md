# Chapter 15: Layouts

Creating site layouts, different size screens, & 
position of elements using normal flow, relative/absolute positioning & floats.

learning the difference between fixed width & liquid layouts

how the design process can be blocked or mitigated as a result of different computer screens and devices

Learning jow designers make their pages look professional for their pages.

## Positioning of elements

Normal flow the paragraphs appear below each other example below

~
<body>
<h1> This is our header</h1>
<p> Here we have a normal paragraph that is just doing its own thing. Basically only putting 2 sentencees in here and nothing more. That's it.</p>
</body>

body {
  width: 550px;
  font-family: Arial, Verdana, sans-serif;
  color: #556544;}
  h1 {
    background-color: #efefef;
    padding: 10px;
  }
  p{
  width: 450px;}
  ~

### Paragraphs appear one after the other, vertically down the page

## Relative positioning
<h1> This is our header</h1>
<p> Here we have a normal paragraph that is just doing its own thing. Basically only putting 2 sentencees in here and nothing more. That's it.</p>
</body>

p.example {
  position: relative;
  top: 10px;
  left: 100px;}
### second paragraph has been pushed down and right from original normal flow


