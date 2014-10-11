HTML5-Demo
==========

Demo for HTML5, CSS

Positioning in CSS

Positioning is a very critical concept in **CSS**. In order to make complex layouts, it is important to use **position** property of css. Elements can be positioned using **top**, **bottom**, **left** , **right** properties of CSS but before using them it is mandatory to set the positioning property.

There are four types of positioning methods in CSS, these are:

**1. Static**

 This is the default positioning of any **HTML** element. An element that is static positioned, is positioned according to the normal flow of the document. **Left** , **Right**, **Top** and **Bottom** properties do not work when position property of element is set as static.

 Let's catch hold of this property with the help of this small snippet:

```HTML```

<!DOCTYPE html>
<html>
<head>
    <title>Positioning Demo</title>
    <style>

        #list1{
            border: thick solid #69b;
            position: relative;
            margin: 70px;
        }

        #head1 {
            border: thin solid #69b;
            position: static;
        }

    </style>

</head>
<body>
<div id="list1">
    <h2 id="head1">List:My position is static.</h2>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
</body>
</html>

```HTML```

In the above code heading "head1" is positioned as static. "head1" is contained inside a div "list1" which is positioned as **relative**. So what is **relative** position? But before moving into that, do remember that an element positioned as static is actually said to be not positioned!

**2. Relative**

We had said above that div "list1" is positioned **relative**. Let us understand what does it exactly it means?

A **relative** element is positioned according to its **normal** or **static** position. One can use **top** , **bottom** , **left** and **right** properties to move the element from the position where it would normally occur on a **webpage**.

Let's see another useful piece of code that would help in making this concept more clear:

```HTML```

<!DOCTYPE html>
<html>
<head>
    <title>Positioning Demo</title>
    <style>

        #list2 {
            border: thick solid #69b;
            position: relative;
            margin: 70px;
        }

        #head2 {
            border: thin solid #69b;
            position: relative;
            top: 20px;
            left: 50px;
        }

    </style>

</head>
<body>

<div id="list2">
    <h3 id="head2">List:My position is relative.</h3>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
</body>
</html>

```HTML```

In the above code you must have seen we have used properties **top** and **left**, these have been used to move the element "head2" from its normal position.

When you would run the snippets given above in your browser, you would easily feel the difference!

**3. absolute**

Third in the kitty is **absolute** positioning, this can be a little tricky to understand, but we shall succeed I believe!

An element positioned as **absolute** is positioned relative to the first parent element that is not positioned as static. In case there is no positioned ancestor, it positions itself according to the page **body**.

Keep Calm and See the following Code:

```HTML```
<!DOCTYPE html>
<html>
<head>
    <title>Positioning Demo</title>
    <style>

        #list3 {
            border: thick solid #69b;
            position: relative;
            margin: 70px;
        }

        #list4 {
            border: thick solid #69b;
            margin: 50px;
        }


        #head3 {
            border: thin solid #69b;
            position: absolute;
            top: 20px;
            left: 50px;
        }

        #head4 {
            border: thin solid #69b;
            position: absolute;
            top: 20px;
            left: 50px;
        }
    </style>


</head>
<body>
<div id="list3">
    <h3 id="head3">List:My position is absolute.</h3>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
<div id="list4">
    <h3 id="head4">List:My position is absolute but my ancestor doesn't has a position.</h3>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
</body>
</html>

```HTML```

In the above code both "head3" and "head4" are positioned as **absolute**, yet there is difference in their positioning. If we closely look at the above code, "list3" which is the parent element of "head3" is positioned as relative, while "list4" which is the parent element of "head4" is not at all positioned, hence there is a huge difference in there position on the browser. "head4" uses the **body** of the document to position itself.

**Remember : Behaviour would have been same, had "head4" been statically positioned, as **static position** is actually **no position**.

**Caution : Elements which are absolutely positioned can overlap with other elements.**

So to sum up, an absolutely positioned element is positioned relative to its parent element.

**4. Fixed position**

**Fixed** position means that an element is positioned **relative** to its **browser window** which means that this element won't move even on scrolling. Like elements which are **absolute** positioned, **fixed** positioned elements can also overlap with other elements.

Let's see some live action here:

```HTML```
<!DOCTYPE html>
<html>
<head>
    <title>Positioning Demo</title>
    <style>

        #list1, #list2, #list3 {
            border: thick solid #69b;
            position: relative;
            margin: 70px;
        }

        #firsthead {
            border: thin solid #69b;
            position: fixed;
            top: 1px;
            left: 30px;
            background-color: limegreen;
        }

        #head1 {
            border: thin solid #69b;
            position: static;
            top: 20px;
            left: 50px;
        }

        #head2 {
            border: thin solid #69b;
            position: relative;
            top: 20px;
            left: 50px;
        }

        #head3 {
            border: thin solid #69b;
            position: absolute;
            top: 20px;
            left: 50px;
        }

    </style>


</head>
<body>
<h2 id="firsthead"> This is a list, my position is fixed!</h2>
<div id="list1">
    <h2 id="head1">List:My position is static.</h2>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
<div id="list2">
    <h3 id="head2">List:My position is relative.</h3>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
<div id="list3">
    <h3 id="head3">List:My position is absolute.</h3>
    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
        <li>Item 5</li>
    </ul>
</div>
</body>
</html>

```HTML```

Try the above code on your browser and you will notice that heading "This is a list, my position is fixed!" will remain there even when you scroll the page.
As you can see in the above code that heading "firsthead" has been positioned **fixed**, therefore even scrolling doesn't takes this heading out of sight!

Well..in this blog we have seen one of the most critical concepts of css, however the picture would become clearer only when we use these positioning methods in various situations in order to achieve the desired results.

To check out the full working code please see my github repository.