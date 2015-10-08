# Review

## AvoidingCommonMistakes

This is excellent. Do you feel that you understand these requirements? If you can follow them, your web applications and web sites will be a cut above most.

## index.html

This one needs some work, but is pretty good overall.

The most important issue is formatting. It is extremely important that you begin to develop code coding habits from Day One. If you develop poor habits, you will suffer throughout your career from them. The difference is literally huge. Even if poor habits cost you only half an hour a day, multiply that across a 20-year career and you're talking 2500 wasted hours! That's more than a *year* of wasted work time. You don't want that.

So take a look at your index.html file. Can you see that it's a mess? This is not a rhetorical question. Some people can see mess and for some people it's just invisible. What kinds of things are messy?

First, note that HTML elements are like boxes. We put smaller boxes into bigger boxes. So the `<head></head>` and the `<body></body>` boxes go *inside* the `<html></html>` box, right?

An easy way to make this clear is through indentation. You should always indent content of an HTML element two spaces, *unless that content fits on one, 80-character line.

See how `<head>` is aligned right under `<html>`? That makes it hard to read. So let's indent `<head>` and `</head>` two spaces. And then the content inside of the head element gets indented 4 spaces. And so on.

Next, see how you have multiple blank lines? This is a waste of space and just looks sloppy. Separate sections with a single blank line. Never more than one blank line. This takes some practice! It's a new way of looking at things so be patient with yourself. But if you look carefully, line by line, then you'll get this right.

Here's what the `<head>` section of your document should look like:

(Also, note that we shouldn't use `&` in our content as that symbol has special meaning in HTML. So instead we use `&amp;`&mdash;see below.)

```html
<head>
  <meta charset="utf-8">
  <meta name="viewport" conent="width=device-width, initial-scael=1">

  <title>Curries, Code &amp; Flatmates (goes in the tab on the browser)</title>

  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css">

  <script src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js"></script>
  <style type="text/css" media="all">
    body {
      background-color: #FAFAD2;
    }

    h1.WebsiteTitle {
      color: #6495ED;
      background-color: yellow;
      font-family: "comic sans";
      font-size: 50px;
      text-align: center;
    }

    nav.navbar {
      color: #00CED1;
      background-color: gold;
      font-size: 20px;
      min-height: 30px;
    }

    nav li {
      width: 28%;
      float: left;
    }

    footer {
      margin-top: 35px;
      border-top: 2px solid;
    }
  </style>
</head>
```

Note: For CSS class and ID names, use "train-case". That's all lower case with words separated by hyphens. So `website-title` not `WebsiteTitle`. You'll be learning many different styles for different uses (the style you used is called PascalCase or BumpyCase or sometimes UpperCamelCase). Each language has it's own rules. Joy, eh?

Can you see the difference? (Again, some people cannot, so let us know now if you can't.) Go back through your `index.html` file line by line and try cleaning it up.

Also, be very careful about what goes into what. The arrangement of HTML is always an `<html>` element split into a `<head>` element and a `<body>` element. Invisible code goes into the head (metadata). Visible code goes into the body. But everything goes into *either* the head or the body. Like this:

```
html
  head
    meta
    title
    link
    script
  body
    header
      h1
      nav
        ul
          li
            a
    main
      article
        header
          h2
        p
        p
        p
          a
      article
        header
          h2
        p
        p
        p
          a
    footer
      p
        a
        img
      p
```

Do you see how things fit inside each other? If you lay everything out with correct indentation, then you will quickly see what's wrong with your code.

This week we'll show you some more tricks for making your code cleaner and easier to read. Easy is good, no?

Notice above that there is only *one* html element with *one* head element and *one* body element. Check your code. Update it and resubmit. We're going to make this page a good reference for all future HTML you do. :-)

Here's an example article:

```html
<article>
  <header>
    <h2>A Bit About Curry</h2>
  </header>
  <p>
    Curry is the word used to describe a wide variety of dishes originating
    in parts of Asia. Curry is often characterised by an explosion of flavours
    created by a variety of different spices. Smoe common combinations include
    turmeric, cumin and chilli, or lime, coriander and chilli.
  </p>
  <p>
    At my flat, we commonly cook indian and thai curries-generally vegetarian.
    The favourite is a Palak Paneer, from scratch. This delicious curry is
    made from pureed spinach and a type of indian cottage cheese called
    Paneer. Paneer is relatively easy to make and tastes best when fresh.
  </p>
  <p>
    <a href="https://coconutcraze.files.wordpress.com/2013/02/1-pk-pner.jpg">
      <img width=400px
        src="https://coconutcraze.files.wordpress.com/2013/02/1-pk-pner.jpg"
        alt="a delicious Palak Paneer">
    </a>
  </p>
</article>
```
