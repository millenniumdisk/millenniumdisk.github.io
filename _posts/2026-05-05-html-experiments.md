---
layout: post
title: HTML Experiments
---

# Experiments

## Experiment 1
```html
<!-- p1 display heading and paragraph -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
    <link rel="stylesheet" type="text/css" href="style.css">
    <script defer type="module" src="script.js"></script>
		<title>Introduction to HTML</title>
  </head>
  <body> <!-- all visible parts are inside <body> -->
    <h1>Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

## Experiment 2
```html
<!-- p2 create links with anchor tags -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <!--
    css/style.css is a relative address or relative url because
    css is a folder that is in the same location of where index.html is
    a relative file path is similar since it won't have the
    root directory in the address and is also short
    -->
    <link rel="stylesheet" type="text/css" href="css/style.css">
    <script defer type="module" src="script.js"></script>
  </head>
  <body>
    <p title="This is a tooltip">The weather today is fair</p>
    <!--
    absolute address or absolute url is a long address
    and absolute file path is similar to it since the root directory
    is included in the address and is also long
    -->
    <a href="https://www.google.com/">Google Link</a>
    <a href="https://www.yahoo.com/" target="_blank">Yahoo Link</a>
    <a href="mailto:paulferringson@gmail.com">Send an email to the link</a>

    <!-- relative url: register.html can be written without .html but it is better to add .html -->
    <a href="register.html">Get Started</a>
  </body>
</html>
```


## Experiment 3
```html
<!-- p3 id class bookmark img bold tag-->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    <script defer type="module" src="script.js"></script>
  </head>
  <body>
    <h1 id="first-header">Programming Notes</h1>

    <h2>Programs Needed to Start Programming</h2>
    <p>Code editor is important</p>

    <h2 id="second-header">HTML</h2>
    <p>HTML is easy</p>

    <h2 class="header-group">CSS</h2>
    <p>CSS makes web pages beautiful</p>
    <!--
    an id and class can be both in the element at the same time
    multiple classes can be added by separating them with a space
    -->

    <!-- we don't need width and height attributes when css is used to modify the image size -->
    <img src="images/cat_pic1.jpg" alt="cat" width="200" height="100">

    <a href="#first-header">Go to the <b>first</b> header</a>
  </body>
</html>
```

## Experiment 4
```html
<!-- p4 lists -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <h1>Tasks</h1>

    <h2>To Buy Later</h2>
    <ul>
      <li>pasta</li>
    </ul>

    <h2>To Complete Now</h2>
    <ol>
      <li>read book about HTML</li>
      <li>create a summary of HTML topic in a notebook</li>
      <li>practice HTML</li>
    </ol>

    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 5
```html
<!-- p5 svg -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <h1>SVG</h1>

    <!--
    there are two ways of using svg
    1. inline svg
    2. img
    second is better because of separation of concern and performance
    -->
    
    <!--
    inline svg
    svg of html icon from https://ionic.io/ionicons
    even if svg file is not in the folder of website project where index.html is,
    svg will be working because inline svg is used
    -->
    <svg xmlns="http://www.w3.org/2000/svg" class="ionicon" viewBox="0 0 512 512">
      <path d="M64 32l34.94 403.21L255.77 480 413 435.15 448 32zm308 132H188l4 51h176l-13.51 151.39L256 394.48l-98.68-28-6.78-77.48h48.26l3.42 39.29L256 343.07l53.42-14.92L315 264H148l-12.59-149.59H376.2z"/>
    </svg>

    <!--
    img 
    svg file is needed to be in images folder with the filename logo.svg
    -->
    <img src="images/logo.svg" alt="logo">

    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 6
```html
<!-- p6 forms -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <!--
    forms collect and submit user data
    action is location where data will be sent
    method is HTTP method for data and it can be GET, POST, PUT, DELETE
    GET is to receive data
    -->
    <h1>Forms</h1>
    <form action=/api/v1/journals" method="post">
      <!-- form elements -->  
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 7
```html
<!-- p7 input -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <!--
    forms collect and submit user data
    action is location where data will be sent
    method is HTTP method for data and it can be GET, POST, PUT, DELETE
    GET is to receive data
    -->
    <form action=/api/v1/journals" method="post">
      <input type="text">

      <!-- name is needed when sending data to server -->
      <input type="text" name="title" placeholder="Enter Title">

      <!-- maxlength attribute could be used to limit the size of input -->
      <input type="text" name="description" placeholder="Enter short description" maxlength="30">

      <!--
      required ensures there is a value in the form field before submit
      disabled is used to prevent users from inputting and is useful when
      submitting and we don't want users to change data while submitting
      -->

      <input type="email">
      <input type="password">
      <input type="date">
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 8
```html
<!-- p8 labels -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <!--
    labels improve accessibility and useability of forms
    always use labels for helping people read UI,
    help people with screen readers, help people with mobile devices
    when clicking a label, cursor will automatically
    move to the input it is connected to
    -->
    <form action=/api/v1/journals" method="post">
      <!-- main-title is inside label and input so they are connected-->
      <label for="main-title">Journal Title</label>
      <input id="main-title" type="text" name="title" placeholder="Enter title">
      <!--
      it is ok for id and name to have the same values because they serve different purposes
      if the type is email, it is also ok to have the values of id, type and name to be all email
      -->

    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 9
```html
<!-- p9 text area -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <form action=/api/v1/journals" method="post">
      <!-- id, for and name can have the same value  -->
      <label for="journal-entry">Journal Entry</label>
      <!--
      rows and cols contain size in characters
      changing the position of textarea can be done in css
      if there is content in the middle of textarea, it will become actual text
      -->
      <textarea id="journal-entry" name="entry" rows="5" cols= "30"></textarea>
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 10
```html
<!-- p10 dropdown  -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <form action=/api/v1/journals" method="post">
      <label for="journal-category">Journal Category</label>

      <!--
      value is the data that will be sent to the server
      (ex. category="task" where task is a predefined value from the choices
      -->
      <select id="journal-category" name="category">
        <!-- value is needed and it is usually the same value as the choices but in lowercase  -->
        <option value="task">Task</option>
        <option value="note">Note</option>
        <option value="idea">Idea</option>
      </select>
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 11
```html
<!-- p11 buttons  -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <form action=/api/v1/journals" method="post">
      <!--
      type is not required but it is better to put it
      put a submit value to type when the button is used for submitting forms
      this is not needed when the button will be used for submitting forms
      but it is better to put submit to type
      the other value for type is reset which resets user-entered data
      -->
      <button type="submit">Submit</button>
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 12
```html
<!-- p12 checkbox  -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <form action=/food/pizza" method="post">
      <!-- value of name should be unique for each  -->
      <input id="topping-1" type="checkbox" name="pineapple">
      <label for="topping-1">Pineapple</label>

      <input id="topping-2" type="checkbox" name="corn">
      <label for="topping-2">Corn</label>

      <input id="topping-3" type="checkbox" name="olives">
      <label for="topping-3">Olives</label>

      <button type="submit">Submit</button>
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 13
```html
<!-- p13 radio button -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>

    <form action=/clothing/shirts" method="post">

      <!--
      value of name is the same for the radio buttons but different in value because only one button can be selected
      value is not needed in checkboxes unlike radio buttons because checkboxes are on / off in value
      -->
      <input id="small" type="radio" name="size" value="s">
      <label for="small">Small</label>

      <input id="medium" type="radio" name="size" value="m">
      <label for="medium">Medium</label>

      <input id="large" type="radio" name="size" value="l">
      <label for="large">Large</label>

      <button type="submit">Submit</button>
    </form>
    
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 14
```html
<!-- p14 block elements -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <!-- block elements  -->
    <h1>Heading</h1>
    <p>This is a paragraph</p>
    <ul>
      <li>List item 1</li>
      <li>List item 2</li>
      <li>List item 3</li>
    </ul>
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 15
```html
<!-- p15 inline elements -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <a href="https://www.google.com/">Google Link</a>
    <img src="images/cat_pic1.jpg" alt="cat" width="200" height="100">
    <br>
    <form action=/api/v1/journals" method="post">
      <input type="text">
    </form>
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 16
```html
<!-- p16 div -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <a href="https://github.com/">Link 1</a>
    <a href="https://www.python.org/">Link 2</a>
    <a href="https://www.drawio.com/">Link 3</a>
    <a href="https://www.gimp.org/">Link 4</a>

    <div>
      <a href="https://krita.org/en/">Link 5</a>
      <a href="https://git-scm.com/">Link 6</a>
    </div>
    
    <div>
      <a href="https://trello.com/">Link 7</a>
      <a href="https://www.todoist.com/">Link 8</a>
    </div>
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 17
```html
<!-- p17 span -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <h1>Create <span>Amazing</span> Journals</h1>
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 18
```html
<!-- p18 html that is semantic -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <header>
      <h1>My Blog</h1>
    </header>
    <main>
      <section>
        <h2>printf Function</h2>
        <p>printf is a function in C Programming that can be used to display messages based on the arguments passed to it</p>
      </section>
    </main>
    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 19
```html
<!-- p19 tables-->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <table>
      <thead>
        <tr>
          <th>Product ID</th>
          <th>Name</th>
          <th>Brand</th>
          <th>Price</th>
        </tr>
      </thead>
      
      <tbody>
        <tr>
          <td>1</td>
          <td>Vitamin C Adult Gummies</td>
          <td>Kirkland</td>
          <td>$25.94</td>
        </tr>
        <tr>
          <td>2</td>
          <td>Vienna Sausage 1 Pack</td>
          <td>Libby's</td>
          <td>$11.76</td>
        </tr>
        <tr>
          <td>3</td>
          <td>Tomato Ketchup</td>
          <td>Heinz</td>
          <td>$4.14</td>
        </tr>
        <tr>
          <td>4</td>
          <td>Crunch Chocolate Fun Size</td>
          <td>Nestle</td>
          <td>$5.97</td>
        </tr>
      </tbody>

      <tfoot>
        <tr>
          <td colspan="3">Total Price</td>
          <td>$47.81</td>
        </tr>
      </tfoot>
    </table>

    <script src="script.js"></script>
  </body>
</html>
```

## Experiment 20
```html
<!-- p20 superscript subscript and figure -->
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">

    <title>Introduction to HTML</title>
    
    <link rel="stylesheet" type="text/css" href="style.css">
    
  </head>
  <body>
    <p>This is a pa<sub>r</sub>agraph with a diffe<sup>r</sup>ent thing inside it</p>
    <figure>
      <!-- img tag with the picture of the figure  -->
      <figcaption>Pieces of potassium metal</figcaption>
    </figure>
    <script src="script.js"></script>
  </body>
</html>
```