# 4geeks academy project - a notebook style todo list with React and Bootstrap

![gif](https://github.com/vanesascode/blog-node-express-ejs-mdbatlas-mvc/assets/131259155/51fca67f-b662-4d91-8f95-159b35d6704b)

We were asked to add a handwritten notebook style, so it was a good CSS exercise. 

***

Since Bootstrap is quite limited for this, I added some useful styles it has, but I built the rest with CSS:

🔹 Made use of `relative` and `absolute` display properties, along with the `z-index` property, to create the notebook pages effect.

🔹 Another good learning for me was the one of more complex `selectors`:

``
.item-box:hover button {
 	 color: rgb(206, 200, 200);
}
``

In the previous example, I could hover over the list card and the button appeared. So, the CSS selector targets a button element within a hovered item-box element. When the item-box element is hovered over by the user, the color of the button text will be changed.

🔹 Other interesting ones that our Bootcamp teacher showed me was: 

``
.item-box:hover div > button {
color: rgb(206, 200, 200);
}
``

This is a CSS selector that targets a button element that is a `direct child of a div` element, which itself is a descendant of a hovered item-box element. When the item-box element is hovered over by the user, the color of the button text will be changed.

And you can add as many parents as you like! 

``
.item-box:hover div > div > button {
color: rgb(206, 200, 200);
}
``

Another tip, was to see how to add style to the placeholder: 

``
input::placeholder {
  color: rgb(206, 200, 200);
}
``

# UPDATES: 

In this updated code, the addTodo function now checks if the todoInput is not empty or just whitespace before adding a new item to the todos state. It uses the trim method to remove leading and trailing whitespace from the input string. If the input is not empty, the new item is added to the todos state array using the spread operator. If the input is empty, no item is added.

``
if (todoInput.trim() !== "") {
      setTodos([...todos, todoInput]);
      setTodoInput("");
    }
``

Also, to handle the pluralization of the word "item" based on the number of items in the list we use the following: 

``
  if (todoInput.trim() !== "") {
  ...
  }
``

