# DOM Fundamentals Quiz

## Your Name: _______________________ Your Score: ___________________


#### 1) What is the HTML tag used to include a JavaScript file? (1 point)

* a) `<link>`
* b) `<img>`
* c) `<source>`
* d) `<script>`
* e) None of the Above

#### 2) What is the HTML tag used to include a CSS stylesheet? (1 point)

* a) `<link>`
* b) `<img>`
* c) `<source>`
* d) `<script>`
* e) None of the Above

#### 3) What is the HTML tag used to include an image file? (1 point)

* a) `<link>`
* b) `<img>`
* c) `<source>`
* d) `<script>`
* e) None of the Above

#### 4) What is the HTML tag used to include an audio file? (1 point)

* a) `<link>`
* b) `<img>`
* c) `<source>`
* d) `<script>`
* e) None of the Above


**Consider the following code, then answer questions 5 through 7**

*HTML*

```html
<div class="container">
  <p id="title">Hello SEI!</p>
  <p id="subtitle">Welcome!</p>
</div>
```

*CSS*

```css
.container {
  color: blue;
  font-weight: bold;
  text-decoration: none;
}

#title {
  text-decoration: underline;
  color: purple;
}

#subtitle {
  font-size: 11px;
  color: chartreuse;
}
```

#### 5) The CSS above contains the `#` selector. What does it mean? (1 point)

* a) `#` is a hashtag that represents the main topics of the DOM
* b) `#` indicates that the name following it references a class
* c) `#` indicates that the name following it references an id
* d) `#` indicates that the name following it references a tag
* e) `#` indicates that the name following it references inline styling

#### 6) The CSS above contains the `.` selector. What does it mean? (1 point)

* a) `.` indicates a pseudo-class
* b) `.` indicates that the name following it references a class
* c) `.` indicates that the name following it references an id
* d) `.` indicates that the name following it references a tag
* e) `.` indicates that the name following it references inline styling

#### 7) What will the text `"Hello SEI!"` look like after the code is run? (1 point)

* a) It will be underlined, bold, and blue
* b) It will be bold and blue but not underlined
* c) It will be underlined, bold, and purple
* d) It will be underlined and purple but not bold 
* e) It will be black text not bold or underlined 


**Consider the following code and then answer questions 8 and 9**

```html
<div>
  <p id="red" class="blue" style="color:green">CSS - You'll Learn to Love It!</p>
</div>
```

```css
div {
  color: yellow;
}
```

#### 8) What color will the text be? (1 point)

* a) Red
* b) Yellow
* c) Blue
* d) Green
* e) Black

#### 9) The style attribute with CSS `style="color:green"` above is an example of: (1 point)

* a) Embedded Stylesheets
* b) Inline Styling
* c) Iframe Embedding
* d) The abbreviated `<font>` tag from HTML4
* e) Internal CSS

#### 10) How can JavaScript be used to dynamically alter the color of the following element: `<p id="paragraph">Hello</p>`? (1 point)

* a) var p.color = "red"
* b) document.p.styles.colors = "red"
* c) document.getElementById("color:red").styles = "paragraph"
* d) document.getElementById("paragraph").styles.color = "red"
* e) document.getElementById("paragraph") = "red"
