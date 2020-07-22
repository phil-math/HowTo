# CSS: Cascading Style Sheets

   **CSS** is a stylesheet language usede to describe the presentaion of a document written in HTML or XML, describes how  elements should be rendered on screen. 


### Applaying CSS to HTML

Exist thee methods of applying CSS to a document.

+  #### External stylesheet
   
   You reference an external CSS stylesheet from an HTML **`<link>`** element.

   >```HTML
   ><html>
   >  <head>
   >     ...
   >     <link rel="stylesheet" href="styles.css">
   >     ...
   >  </head>
   >  <body>
   >     ...       
   >  </body>
   ></html>
   >```

+  #### Internal stylesheet
   
   You place CSS inside a **`<style>`** element contained inside the HTML **`<head>`**.
   
   >```HTML
   ><html>
   >  <head>
   >     ...
   >     <style>
   >        ...
   >        h1 {
   >           color: blue;
   >           background-color: yellow;
   >           border: 1px solid black;
   >        }
   >        ...
   >     </style>
   >     ...
   >  </head>
   >     <body>
   >        ...       
   >     </body>
   > </html>
   >```

+  #### Inline styles
   
   You place CSS effects in a **_style_** _attribute_ of a single HTML element.
  
   >```HTML
   ><html>
   >  ...
   >  <body>
   >     ...
   >     <h1 style="color: blue;background-color: yellow;border: 1px solid black;">
   >        Hello World!
   >     </h1>
   >     ...       
   >  </body>
   ></html>
   >```
   


---

### Selectors

|Selector|Example|Example description|
|:---|:---|:---|
|*|`*{}`|Selects all elements|
|element|`p{}`|Selects all `<p>` elements|
|.class|`.box{}`|Select all elements with class ="box"|
|#id|`#firstname{}`|Select all elements with id="firstname"|
|[attribute]|`a[target]{}`|Selecet every `<a>` element with a target attribute|
|:pseudo-class|`p:first-child{}`|Selects every `<p>` element that is the first child of its parent|
|::pseudo-element|`p::first-letter{}`|Selects the first letter of every `<p>` element|

#### Selectors combinators

|Type|Example|Description|
|:---|:---|:---|
|Descendant combinator|`article p {}`|Select all `<p>` element inside `<article>` element|
|Child combinator| `article > p {}`|Selects all `<p>` element where the parent is a `<article>` element|
|Adjacent sibiling combinator|`h1 + p {}`|Selects all `<p>` elements that are placed immediately after `<h1>` elements|
|General sibiling combinator|`h1 ~ p {}`|Selects every `<p>` elements that are preceded by a `<h1>` element with the same parent|
|Specify element|`p.especial{}`|By default the first thing in a selector is the type of the element, when omitting the type is * (universal)|
|List selectos|`h3, .special, article p:first-child {}`|It doesn't really combine selectors, it actually groups selectors separated by commas |