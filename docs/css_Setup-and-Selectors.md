# **CSS Setup and Selectors**

  In this lesson you will learn how to set up a CSS file, and how to create CSS selectors, and how to set up CSS rule sets.
1. **Intro to CSS**
    * Cascading Style Sheets: is a language that web developers use to _style_ the HTML content on a web page.

1. **Inline Styles**
    ```html
    <p style="font-family: Arial;">I'm learning to code</p>
    ```

1. **The &lt;style&gt; Tag**
   ```CSS
   <style>
   p {
       color: red;
       font-size: 20px;
   }
   </style>
   ```

1. **The .css file**
    * To avoid mixing code by storing HTML and CSS code in separate files.

1. **Linking the CSS file**
     ```HTML
    <link href="./style.css" type="text/css" rel="stylesheet">
    ```
    * Use ```<link>``` element to link HTML and CSS diles togethor. Here are some arrtibutes:
      1. ```href```: like the anchor element, the value of this arrtibute must be the addresss, or path, to the CSS file.
      1. ```type```: The type of document that yout are linking to. The value of this attribute should be set to ```text/css```.
      1. ```rel```: describes the relationship between the HTML dile and the CSS file. the value should be set to ```stylesheet```.

1. **Tag Name**
       ```CSS
       p {

       }
       ```
    * CSS can select HTML elements by using and element's tag name.

1. **Class Name**
    * HTML
     ```HTML
     <p class="brand">
     ```
    * CSS
    ```CSS
    .brand {

    }
    ```
    It possible to select an element by its ```class```( . ) attribute.
1. **Multiple Classes**
    * HTML
    ```HTML
    <h1 class="title uppercase">
    ```
    * CSS
    ```CSS
    .title {
      color: teal;
    }
    .uppercase {
      text-transform: uppercase;
    }
    ```
    It is able to add more than one class name to an HTML element's ```class``` attribute.

1. **ID Name**
    * HTML
    ```HTML
    <h1 id="large-title">...</h1>
    ```
    * CSS
    ```CSS
    #large-title {

    }
    ```
    An element needs to be styled uniquely.

1. **Classes and IDs**
    1. Classes are meant to be used many times, an ID is meant to style only one element.
    1. IDs override the styles of tags and classes, So  they should be used sparingly and only on elements that need to always appear the same.
    * HTML
    ```HTML
    <h6 class="publish-time">Published: 2 Days Ago</h6>
    ```
    * CSS
    ```CSS
    color: gray;
    ```

1. **Specificity**
    1. Specificity is the order by which the browser decides which CSS styles will be displayed.
    1. In practice, using the lowest degree of specificity, so that if an element needs a new style, it is easy to override.
    1. tag &gt; class &gt; ID
    * HTML
    ``` HTML
    <h1 class="headline">Breaking News</h1>
    ```
    * CSS
    ```CSS
    h1 {
        color: red;
    }
    .headline {
        color: firevrickl;
    }
    ```

1. **Chaining Selectors**
    1. it's possible to require an HTML element to have two or more CSS selectors at the same time.  we will refer to as chaining.
    ```css
    h1.special {

    }
    ```

1. **Nested Elements**
    1. Nested elements can be selected by separating selectors with a space.
    * HTML
    ```HTML
    <ul class='main-list'>
      <li> ...</li>
      <li> ...</li>
    </ul>
    ```
    * CSS
    ```css
    .main-list li{

    }
    ```

1. **Chaing and Specificity**
    1. Instead of selecting all ```<p>``` elements, you selected only the ```<p>``` elements nested inside the ```.main``` elements.
    * CSS
    ```css
    p {
        color: blue;
    }
    .main p {
        color: red;
    }
    ```

## Supplement

1. **Important**
    1. The ```!important``` flag will override any style, however it should almost never be used, as it is extremely difficult to override.
    1. Once !important is used, it is very hard to override.
    1. As a result, it should almost never be used.
    ```css
    p {
        color: blue !omportant;
    }
    ```

1. **Mutiple Selectors**
   1. Multiple unrelated selectors can receive the same styles by separating the selector names with commas.
   * CSS
   ```css
   h1 {
       font-family: Georgia;
   }
   .menu {
       font-family: Georgia;
   }
   ```
   * CSS
   ```css
   h1,
   .menu {
       font-family: Georgia;
   }

   ```
