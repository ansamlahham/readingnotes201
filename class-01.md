# How People Access the Web?
**1. Browsers**
People access websites using software called a web browser.
Popular examples include Firefox, Internet Explorer, Safari,
Chrome, and Opera.

**2.Web Servers**
When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a web server which hosts the website.

**3.Screen readers**
Screen readers are programs that read out the contents of a
computer screen to a user. They are commonly used by people
with visual impairments.

**4.Devices**
People are accessing websites on an increasing range of devices including desktop computers,
laptops, tablets, and mobile phones. It is important to
remember that various devices have different screen sizes and some have faster connections to the web than others.

## HTML Describes the Structure of Pages

![](https://csveda.com/wp-content/uploads/2020/02/Code1.png)

# A Closer Look at Tags

![](https://www.bluekatanasoft.com/wp-content/uploads/element-structure.png)

## Attributes Tell Us More About Elements

Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a name and a value,separated by an equals sign.

## Body, Head & Title


**<body>**
You met the <body> element in the first example we created.
Everything inside this element is shown inside the main browser window.

**<head>**
Before the <body> element you will often see a <head> element. This contains information about the page (rather than information that is shown within the main part of the browser window that is highlighted in blue on the opposite page). You will usually find a <title> element inside the <head>element.

**<title>**

The contents of the <title> element are either shown in the
top of the browser, above where you usually type in the URL of the page you want to visit, or on the tab for that page (if your browser uses tabs to allow you to view multiple pages at the same time).


DOCTYPES tell browsers which version of HTML you
are using.
X You can add comments to your code between the
<!-- and --> markers.
X The id and class attributes allow you to identify
particular elements.
X The <div> and <span> elements allow you to group
block-level and inline elements together.
X <iframes> cut windows into your web pages through
which other pages can be displayed.
X The <meta> tag allows you to supply all kinds of
information about your web page.
X Escape characters are used to include special
characters in your pages such as <, >, and ©.

### Traditional HTML Layouts
For a long time, web page authors used <div> elements to group together related elements on the page (such as the elements that form a header, an article, footer or sidebar). Authors used class or id attributes to indicate the role of the <div> element in the structure of the page.

#### Headers & Footers
##### <header> <footer>

The <header> and <footer>
elements can be used for:
* The main header or footer that appears at the top or
bottom of every page on the site.
* A header or footer for an individual <article> or
<section> within the page

#### Navigation
##### <nav>

The <nav> element is used to contain the major navigational
blocks on the site such as the primary site navigation.

#### Articles
##### <article>
The <article> element acts as a container for any section of a page that could stand alone and potentially be syndicated.


#### Article
##### <aside>
The <aside> element has two purposes, depending on whether
it is inside an <article> element or not.

#### Sections
##### <section>
The <section> element groups related content together, and
typically each section would have its own heading

#### Heading Groups
##### <hgroup>
The purpose of the <hgroup> element is to group together a
set of one or more <h1> through <h6> elements so that they are treated as one single heading.

#### Figures
##### <figure> <figcaption>

You already met the <figure> element in Chapter 5 when we
looked at images. It can be used to contain any content that is referenced from the main flow of an article (not just images).

#### Sectioning Elements
##### <div>

It may seem strange to follow these new elements by revisiting the <div> element again. (After all, the new elements are often going to be used in its place.)