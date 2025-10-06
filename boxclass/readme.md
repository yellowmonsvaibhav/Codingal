The CSS Box Model
In CSS, the term "box model" is used when talking about web design and layout.

The CSS box model is essentially a box that wraps around every HTML element.

Every box consists of four parts: content, padding, borders and margins.

The image below illustrates the CSS box model:


<img src="Screenshot 2025-10-06 at 8.30.31 PM.png" alt="Screenshot of my project" width="500"/>


<svg width="100%" height="300" xmlns="http://www.w3.org/2000/svg">
  <foreignObject width="100%" height="100%">
    <div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        .background {
          background-image: url(' css box model_2.webp ');
          background-size: cover;
          color: white; /* Optional: Adjust text color for contrast */
          padding: 20px;
          text-align: center;
          height: 100%;
        }
      </style>
      <div class="background">
        <h1>Your README Title Here</h1>
        <p>Your custom text content here.</p>
      </div>
    </div>
  </foreignObject>
</svg>





Explanation of the different parts (from innermost part to outermost part):

Content - The content of the box, where text and images appear
Padding - Clears an area around the content. The padding is transparent
Border - A border that goes around the padding and content
Margin - Clears an area outside the border. The margin is transparent
The box model allows us to add a border around elements, and to define space between elements.

Example
Demonstration of the box model:

div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}

Width and Height of an Element
In order to set the width and height of an element correctly in all browsers, you need to know how the box model works.

Important: When you set the width and height properties of an element with CSS, you just set the width and height of the content area. To calculate the total width and height of an element, you must also include the padding and borders.

Example
This <div> element will have a total width of 350px and a total height of 80px: 

div {
  width: 320px;
  height: 50px;
  padding: 10px;
  border: 5px solid gray;
  margin: 0;
}
Here is the calculation:

  320px (width of content area)
+ 20px (left padding + right padding)
+ 10px (left border + right border)
= 350px (total width)

  50px (height of content area)
+ 20px (top padding + bottom padding)
+ 10px (top border + bottom border)
= 80px (total height)
The total width of an element should be calculated like this:

Total element width = width + left padding + right padding + left border + right border

The total height of an element should be calculated like this:

Total element height = height + top padding + bottom padding + top border + bottom border

Note: The margin property also affects the total space that the box will take up on the page, but the margin is not included in the actual size of the box. The box's total width and height stops at the border.


