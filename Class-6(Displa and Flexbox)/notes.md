
# Class-5 CSS Flexbox and Media Queries

---
title: Agenda
description: 
duration: 1800
card_type: cue_card
---

The topics we are going to cover in today's session are:

- What is FlexBox
- Using Flexbox properties to Design Layouts
- Media Queries for Responsive Layout

So, let us start with the session.





---
title: Flex Box
description: 
duration: 1800
card_type: cue_card
---

Now let's talk about Flex box.

**Flex Box:**
* Flex box stands for flexible box
* liberty to align and Justify our Elements with just some line of code but you need to think graphically.
* It's a layout model in CSS that makes arranging elements a whole lot easier. 
* With flexbox, you have a container that holds your elements, and it's like your shelf. Inside this container, you can use the power of flexbox to control how your elements behave.

Flexbox is just a concept of CSS that makes your life very easy.

> **Note to instructor:** Now use the below boilercode to start with explaining flex.

Now, lets create some boxes again in HTML to start with flexbox.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox</title>
    <style>
        .container {
            background-color: tomato;
            border: 2px solid black;
            height: 500px;
            width: auto;
        }

        .box {
            height: 100px;
            width: 100px;
            background-color: dodgerblue;
            margin: 10px;
        }
        
    </style>
</head>

<body>
    <div class="container">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
        <div class="box">4</div>
    </div>
</body>

</html>
```

So this is the basic boxes that we made similar to above.

Now lets use the **display: flex;** property in the parent container

```css
.container {
    background-color: tomato;
    border: 2px solid black;
    height: 500px;
    width: auto;
    display: flex;
}
```

When you apply the CSS property display: flex; to an element, you're essentially creating a flex container. This container establishes a flex formatting context for its child elements, or "flex items." This means that the child elements within this container will follow the rules and behaviors defined by the flexbox layout model.

Default property of flex box is to arrange all the elements in the row as you can also see here.

You can also use many flex-direction property to arrange the elements in different ways.





> **Note to instructor:** Use different-different values with flex-direction property like row, column, row-reverse, column-reverse etc, to explain it better.

As mentioned, Flexbox is all about controlling the distribution of elements in a row or column. By default, items will stack side-by-side in a row, but we can flip to a column with the flex-direction property set to column

With flex-direction: row, the main axis runs horizontally, from left to right. When we flip to flex-direction: column, the main axis runs vertically, from top to bottom.

In Flexbox, everything is based on the main axis. The algorithm doesn't care about vertical/horizontal, or even rows/columns. All of the rules are structured around this primary axis, and the cross axis that runs perpendicularly.

> **Note to instructor:** Explain the axis using the below diagram. diagram refence: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

![](https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/050/073/original/upload_1ec9fd4a198aa44de652e4864bd69a53.png?1695317491)

**[Ask the learners]**
If I say, I want my flex direction is row, what will be my main axis?

- X axis

**[Ask the learners]**
And If I say, I want my flex direction is column, what will be my main axis?

- Y axis

---
title: Quiz 1
description: Quiz 1
duration: 90
card_type: quiz_card
---

# Question
What is the default value for the `flex-direction` property in a flex container?
# Choices

- [ ] `column`  
- [x] `row`
- [ ] `row-reverse` 
- [ ] `column-reverse`

---

---
title: Justify Content
description: 
duration: 1800
card_type: cue_card
---


 **justify-content**.

**justify-content:** Defines how flex items are distributed along the main axis (horizontal for row layout, vertical for column layout). 

So if we want to center all the row items, we can use **justify-content: center**

```css
.container {
    background-color: tomato;
    border: 2px solid black;
    height: 500px;
    width: auto;
    display: flex;
    justify-content: center;
}
```

The justify-content: center; property applied to a flex container in CSS aligns its child elements **horizontally** at the center of the container along the main axis. 



Now lets take more examples of **justify-content** property.

> **Note to Instructor:** Explain each of the values with examples.

* **justify-content: flex-start;**
    * Flex items are aligned at the beginning of the container (left for a row layout, top for a column layout).
* **justify-content: flex-end;**
    * Flex items are aligned at the end of the container (right for a row layout, bottom for a column layout).
* **justify-content: center;**
    * Flex items are centered along the container's main axis.
    * Equal space is added before the first item and after the last item, creating a balanced appearance.
* **justify-content: space-between;**
    * Flex items are evenly spaced along the main axis.
    * The first item aligns with the container's start, the last item aligns with the container's end, and equal space is added between the items.
* **justify-content: space-around;**
    * Flex items are evenly spaced along the main axis, with space distributed around them.
    * Space is added before the first item, after the last item, and between each pair of items.
* **justify-content: space-evenly;**
    * Flex items are evenly spaced along the main axis, with equal space added between them.
    * Equal space is added before the first item, between all items, and after the last item.

There are many options for this property, you can choose to play around with all of them.

---
title: Align Items
description: 
duration: 1800
card_type: cue_card
---

Now lets understand **align-items** property.

The **align-items property** lets you control how flex items are positioned on the cross axis within the container.

> **Note to Instructor:** Explain each of the values of align-items with examples.

* **align-items: flex-start;**
    * Flex items align at the start of the cross axis (top for row layout, left for column layout).
    * No additional space is added between items and the container's cross axis edge.
* **align-items: flex-end;**
    * Flex items align at the end of the cross axis (bottom for row layout, right for column layout).
    * No additional space is added between items and the container's cross axis edge.
* **align-items: center;**
    * Flex items are vertically centered along the cross axis.
    * Equal space is added above and below the items, creating a balanced appearance.
* **align-items: baseline;**
    * Flex items are aligned along their text baselines.
    * This value can be useful when items have varying font sizes or text content.
* **align-items: stretch;**
    * Flex items are stretched to fill the container's cross axis.
    * If no height is explicitly set on the items, they will take up the full height of the container.

---
title: Quiz 2
description: Quiz 2
duration: 90
card_type: quiz_card
---

# Question
In a flex container, what does the `align-items` property control?
# Choices

- [ ] The alignment of flex items along the main axis   
- [x]  The alignment of flex items along the cross axis 
- [ ] The order of flex items   
- [ ] The flexibility of flex items 

---



**[Ask the learners]**
If flex-direction if set to row and justify-content is center, which direction it will align?

- Horizontally

Now, we have covered two important properties, justify-content and align-items. Now we will move formward with some interesting properties.

---
title: Flex Box Responsive
description: 
duration: 1800
card_type: cue_card
---

**[Ask the learners]**
Do you know what is a responsive website?

- A responsive website is a website that can work of different screen size and can adapt to those different screen sizes. It responds and adjusts its layout, images, and content to fit the screen it's being viewed on, whether that's a desktop computer, tablet, or smartphone.

Lets take an example to scaler's website

> **Note to Instructor:** Navigate to https://www.scaler.com/ and show its responsiveness

If you minimize the screen, you can see that everything is changing according to the screen size. Design is not breaking and is adapting to the screen size whether it is mobile view or the desktop view.

> **Note to Instructor:** Now to explain screensize better, you can navigate to our HTML page and show different mobile and responsive views in inspect tab.

In inspect tab of our HTML website, we can check how our website will look in different dimensions and screen sizes.

If we decrease the screen size, we can see that the boxes are shrinking. That means it is not responsive, There are various properties in flex box that we can use to make our website responsive.

In the current scenario the boxes are getting shrinked but if I don't want it to shrink and I want them to adjust according to the screen size, for that we can use some CSS properties.

There is 1 property know as **flex-wrap**

**flex-wrap:** The flex-wrap property in flexbox controls whether flex items should wrap onto multiple lines within the flex container when there's not enough space to fit them all on a single line. 

So if we use the above code with flex-wrap property, we can see that the boxes are now responsive and not shrinking.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox</title>
    <style>
        .container {
            background-color: tomato;
            border: 2px solid black;
            height: 500px;
            width: auto;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;

        }

        .box {
            height: 200px;
            width: 200px;
            background-color: dodgerblue;
            margin: 10px;
        }
        
    </style>
</head>

<body>
    <div class="container">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
        <div class="box">4</div>
    </div>
</body>

</html>
```

> **Note to Instructor:** Now create more boxes to expain **flex-wrap** property better.


The flex-wrap property is especially useful when dealing with responsive layouts. It allows you to control how flex items reorganize when the available space changes. For example, if you have a row of cards and they don't fit on a smaller screen, setting flex-wrap: wrap; would cause them to stack vertically, creating a more readable layout.

Here's what each value of flex-wrap does:

* flex-wrap: nowrap;
    * This is the default value.
    * Flex items will stay on a single line, even if they cause overflow. They won't wrap to the next line.
* flex-wrap: wrap;
    * When there's not enough space for all items on a single line, flex items will wrap to the next line. They will stack vertically if needed.
* flex-wrap: wrap-reverse;
    * Similar to wrap, but the wrapping happens in reverse order. The last flex item becomes the first item on the new line, and so on.


Now we can discuss about item wise flex box,For now we were using flex box in container but now we will use flex box within the container items 

---
title: Flex Box for Children items
description: 
duration: 1200
card_type: cue_card
---

> **Note to Instructor:** Navigate to https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-properties-for-the-childrenflex-items and explain that we can use flex properties for children items.


There is 1 property called **order** that is used for ordering the items.

The **order** property in flexbox allows you to control the visual order in which flex items appear within a flex container, regardless of their order in the HTML markup. It's particularly useful for reordering items for different screen sizes or creating unique visual layouts. H

lets give the order property to box1, and see what happens:

```htmlembedded
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox</title>
    <style>
        .container {
            background-color: tomato;
            border: 2px solid black;
            height: 500px;
            width: auto;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;

        }

        .box {
            height: 200px;
            width: 200px;
            background-color: dodgerblue;
            margin: 10px;
        }

        .box1{
            order: 5;
        }
        
    </style>
</head>

<body>
    <div class="container">
        <div class="box box1">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
        <div class="box">4</div>
    </div>
</body>

</html>
```

Now you can see that the box1 is ordered at the last.

let's understand this with an example:

![](https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/050/074/original/upload_738cab0d87a85a216d67986e5105b3e4.png?1695317536)

Suppose, we gave order: 4 to box1 and order: 2 to box3.

> **Note to Instructor:** So the question is how will the boxes arrange themselves?

* box1 has the order 4, so it will go at last.
* box3 has order 2, so it will go at third.
* box 2 will be at 2nd position 
* box1 will be at first.

![](https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/050/075/original/upload_e5323381ac5d2c537cd4459693a88763.png?1695317559)

Now lets' understand flex-shrink property. 

The **flex-shrink** property in flexbox determines how flex items shrink when the container's available space is limited. It defines the ability of an item to shrink in relation to other items in the container when the container's size is reduced. 

let's understand this with an example:

We are providing flex-shrink property as 2 to box3.

```htmlembedded
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flexbox</title>
    <style>
        .container {
            background-color: tomato;
            border: 2px solid black;
            height: 500px;
            display: flex;
            flex-direction: row;
            justify-content: center;
            align-items: center;

        }

        .box {
            height: 200px;
            width: 200px;
            background-color: dodgerblue;
            margin: 10px;
        }

        .box3{
            flex-shrink: 2;
        }
        
    </style>
</head>

<body>
    <div class="container">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box box3">3</div>
        <div class="box">4</div>
    </div>
</body>

</html>
```

Now, whenever we are downsizing the screen box will be the first one to shrink the most.

Similarly there is a property called flex-grow

**flex-grow:** 
* This defines the ability for a flex item to grow if necessary. It accepts a unitless value that serves as a proportion. It dictates what amount of the available space inside the flex container the item should take up.

> **Note to Instructor:** Show the similar example as flex-shrink.

lets see a basic example:

```htmlembedded
.box3{
    flex-grow: 2;
}
```

Now the box3 will grow the most on increasing the screen size




