# HTML5 Semantic Containers Code-along
# HTML5 Semantic Elements Lab

## Objectives
## Problem Statement

1. Surround existing content with HTML5 Semantic Elements
While there is some automatic styling that HTML provides, the purpose of the
language is to give meaning to content on a web page. HTML is used to both
describe the structure of a web page as well as provide information about the
content within.

## Introduction
In HTML5, there are many new tags that help us give that meaning to the content.
These are referred to as _semantic_ elements. In this lesson, we will be
introducing some of the most useful.

Building upon previous code alongs, in this exercise you will add HTML5
Semantic Elements by coding along with the video provided, reviewing the
concepts you were introduced to in the previous lessons. All the files you need
to follow along are provided, but if you would like to continue working from
your personal `exception-realty` repository:
## Objectives

```
git clone https://github.com/<your_username_here>/exceptional-realty
cd exceptional-realty
```
1. Introduce common semantic tags in HTML
2. Explore their use by applying them to existing content

## Instructions
## Non-Semantic Elements

* Fork this repository on Github.
* Use Terminal to clone your forked copy.
* Then change directory into the repository folder.
* Code along with the provided video below and/or its supplementary reading
  located below the video. Code everything you see there. Feel free to stop,
  pause, rewind or fast forward through the content to keep pace.
First, before we get into semantic elements, lets see some examples of
_non-semantic_ elements. Two of the most commonly used HTML tags are `span` and
`div`. Neither tag has automatic styling. The only difference between them:
content wrapped with the `span` tag will display without line breaks, whereas
content wrapped with `div` _will_.

```html
<span>This content will share the same line...</span><span>...as this content</span>

<div>
  This message will appear on a new line
</div>
```

<iframe width="640" height="480" src="//www.youtube.com/embed/xrDw6I4MSBk?rel=0" frameborder="0" allowfullscreen></iframe>
These tags certainly have their uses, and developers can sometimes favor them
_because_ of the lack of styling. However, they don't give any indication as to
what type of content they're wrapping. They are just _dividers_ of the content.

### Semantic Elements
## Semantic Elements

To get started create a feature branch in Terminal by typing `git checkout -b html5-layout`
and press return. Then open the index.html file in your code editor.
Many semantic elements also lack automatic styling, and act very similar to the
`div` tag.  What they provide, instead, is an explanation of what they wrap.

#### Header
### Introduce the Header and Footer Tags

Start by surrounding your `<h1>` and `<h2>`, as well as the `<a>` links of your
main navigation in a `<header>` element like so,
The first two semantic tags to discuss are the `header` and `footer` tags. The
purpose of these may seem obvious to those who have used document editors like
Microsoft Word. _That is the point!_ The `header` tag is used to wrap all
content we would want to contain within the top, header portion of a page. The
`footer` is for everything at the foot, the bottom of a page:

```html
  <header>
    <h1>Exceptional</h1>
    <h2>Realty Group</h2>
<header>
  <!-- Headers often contain company logos -->
</header>

    <a href="index.html">About</a> <a href="new-properties.html">New Properties</a> <a href="real-estate-listings.html">Listings</a> <a href="market-report.html">Market Report</a> <a href="contact.html">Contact</a> <a href="http://hud.gov" target="_blank">H.U.D.</a>
  </header>
<!-- All the main content of a web page goes in between -->

<footer>
  <!-- Footers often contain resources, privacy policy links, and copyright information -->
</footer>
```

On line 2 the `<header>` element gives importance to the content within it,
defining that content as the head of our document.
Commonly, a website with many different pages will have the same header and
footer content on each page... the only content that changes is what is in
between.

#### Nav
### Introduce the Nav Tag

Next let's wrap our links in the `<nav>` element like so,
Typically, inside or just below the header section of a page are navigation
links to help users access different parts of a website. For this block of
links, we can use the `nav` tag. Wrapping `nav` around links helps describe
those links as the page navigation itself:

```html
  <header>
    <h1>Exceptional</h1>
    <h2>Realty Group</h2>
    <nav>
      <a href="index.html">About</a> <a href="new-properties.html">New Properties</a> <a href="real-estate-listings.html">Listings</a> <a href="market-report.html">Market Report</a> <a href="contact.html">Contact</a> <a href="http://hud.gov" target="_blank">H.U.D.</a>
    </nav>
  </header>
<nav>
  <a href="about.html">About</a>
  <a href="contact.html">Contact</a>
</nav>
```

On line 5 our `<nav>` element semantically represents the navigation area of
this page. Looking good!
A reader glancing over an HTML page can quickly see what these links are meant
for. The `nav` tag is not meant for all links, just those typically used for
site navigation.

#### Section
### Introduce the Main Tag

Next we will section off our page by adding a `<section>` element wrapping our
`<img>` image and `<p>`paragraphs like so,
The `main` tag specifies the _main_ content of a web page.  This would typically
be everything in between the `header` and `footer` areas, and may contain many
nested tags:

```html
  <section id="featured-property">
    <img src="images/intro-pic.jpg" alt="A beautiful living room." title="Welcome to Exceptional Realty Group">
    <p>Lorem ipsum dolor sit amet...</p>
    <p>Lorem ipsum dolor sit amet...</p>
  </section>
<header>
</header>
<nav></nav>
<main>
  <!-- All the main content of a web page goes here -->
</main>
<footer></footer>
```

Note that we gave our section an id of `featured-property` on line 3 of the
snippet above. Make sure to properly indent all the content images, and
paragraphs that have been nested within the section element.
With these three tags, all content within the `body` of a web page can be
separated in a way that is easy to interpret.

Continuing on we will insert the next section with an id of `promotional`
surrounding the promotion video like so,
### Introduce the Section Tag

Within the `main` tag, we can continue to breakdown content into specific,
meaningful sections. One way we can do this is to use the... well... `section` tag.

```html
  ...
  <section id="promotional">
    <video controls>
      <source src="videos/real-estate.mp4" type="video/mp4">
      <source src="videos/real-estate.ogv" type="video/ogg">
      Your browser does not support HTML5 video. <a href="http://browsehappy.com" target="_blank">Please upgrade your browser</a>.
    </video>
  <section>
    <p>Lorem ipsum dolor sit amet...</p>
    <p>Lorem ipsum dolor sit amet...</p>
  </section>
```

#### Footer
The `section` tag can be used to define specific portions of a web page. A page
may have multiple boxes of content within a larger container like `main`. For
each box, we can use a `section` tag to separate the content.

At the bottom of the page before the closing `</body>` tag lets create a
`<footer>` element and insert some copyright information.
### Introduce the Article and Aside Tags

```html
...
  <footer>
    &copy; 2014 Exceptional Realty Group. All Rights Reserved.
  </footer>
</body>
```
The `section` tag more informative than, say.. `div`, but it still may not be as
specific as we need.  For particular parts of a web page, we have semantic
options like `article` and `aside`. The `article` tag is for containing written
content such as a news story or blog post. The `aside` tag is for containing
content that may be related to other content, but is better kept separated.

On line 3 we used `&copy;` the html name for the ascii character for the `©`
symbol.
#### Introduce the Figure and Figcaption Tags

#### Figure and Figcaption
Along with `section`, `article` and `aside`, we also have some tags specific for
containing image and media content. The `<figure>` tag wraps self-contained
media content. For instance, a blog post could have an accompanying image to
support the content.

Next we can surround our image and media content with `<figure>` element and
insert a `<figcaption>` within to include a caption about the media content.
We'll start with our `<img>` image element.
The `figure` tag also comes with a companion for providing captions, the
`figcaption` tag.  Since `figure` is used for media, the `figcaption` tag can be
used to add an additional message about that media or its source.

```html
  <section id="featured-property">
  <section>
    <article>
      Lorem ipsum dolor sit amet...
    </article>
    <figure>
      <img src="images/intro-pic.jpg" alt="A beautiful living room." title="Welcome to Exceptional Realty Group">
      <figcaption>345 Carl Street Apt 12, Carrol Rd. Brooklyn, NY - photo by Denise Richards</figcaption>
      <img src="images/intro-pic.jpg"  alt="An exceptional living room." title="Welcome to Exceptional Living Rooms">
      <figcaption>"An Exceptional Living Room" by Leonardo DaVinci, photograph</figcaption>
    </figure>
  </section>
```

On line 2 we included our `<figure>` element which wraps our image and sets it
out as something that is usually a picture, illustration, diagram, code
snippet, or schema that is referenced in the main text of the page. Inside it
on line 4, we included a `<figcaption>` element calling out the text as a
caption for the figure it is held within.
Here, we've wrapped an image in the `figure` tag, and included a `<figcaption>`
providing the title and creator of the image.

Now add another surrounding our video player.
## Reinforcing What We've Learned About Semantic Elements

```html
  <section id="promotional">
    <figure>
      <video controls>
        <source src="videos/real-estate.mp4" type="video/mp4">
        <source src="videos/real-estate.ogv" type="video/ogg">
        Your browser does not support HTML5 video. <a href="http://browsehappy.com" target="_blank">Please upgrade your browser</a>.
      </video>
      <figcaption>Exceptional Realty Group Promotional Video - Source: archive.org</figcaption>
    </figure>
  </section>
```
Let's practice what we've discussed. In `index.html`, we have a web page with
some example content for a real estate agency. However, most of the HTML tags
within the `body` are non-semantic `div` and `span` tags.

Your task is to read through the provided comments and add in the appropriate
semantic tags. Run `learn` to test your work and use the provided error
messaging to work through the tests. When finished, run `learn submit`.

**Note:** there are a _few_ semantic tags in `index.html` not explicitly discussed in this
readme. Use the comments to figure out what tag you will have to use.

Make sure that for every `div` and `span` you replace, that you also replace the
corresponding _closing_ tag!

You can view `index.html` by running `httpserver` or opening the file in a
separate browser tab.  It is worth noting, though, that the layout of the page
won't change as you add semantic tags. We are not changing the styling or
structure, but the description of the content contained on the page.

## Conclusion

Using semantic tags serves multiple functions. It provides a greater
_readability_ for yourself or anyone else who may edit an HTML document in the
future. It also helps search engines identify and categorize content on
websites. In addition to these two functions, using semantic tags also makes it
easier to _style_. With Cascading Style Sheets, we can easily set up styling for
_just_ the `nav`, or make sure that `main` is always a certain height on the
page. These terms are more natural to write and faster to understand than `div`
and `span`.

There are more semantic tags to explore, some of which you've already used! Tags
such as `form` and `table` are semantic as well, as they describe the contents
within.

Don't forget to indent the content such as the video and image that are nested
inside of our `<figure>` elements. Then you can save this file and give it a
preview in the browser. Since we just surrounded the preexisting content it
won't look too different, although the HTML5 semantic elements do act as boxes
that will stack vertically giving some separation between each and the figures
do have some default spacing that will indent the video and image a bit.

Normally you would add these HTML5 semantic elements where applicable to all of
your site pages. I will add these to the other pages for you and the next code
along will already have them present in its starter code. We just did it on the
index page for some practice. Nice work!

It's now time to version our changes using Git. To do so, in Terminal type
`git add index.html` and press return. Then type
`git commit -m "add semantic containers to index"` and press return. Then push
up this feature branch `git push -u origin html5-layout` and press return. Next
merge the changes into your master branch. Type `git checkout master` and press
return, then `git merge html5-layout` and press return. Then
`git push origin master` and press return.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/html5-semantic-containers-code-along' title='HTML5 Semantic Containers Code-along'>HTML5 Semantic Containers Code-along</a> on Learn.co and start learning to code for free.</p>
<p data-visibility='hidden'>View <a href='https://learn.co/lessons/html5-semantic-containers-code-along' title='HTML5 Semantic Containers Code-along'>HTML5 Semantic Elements Lab</a> on Learn.co and start learning to code for free.</p>
