# CSS Deep-dive

## Semantic HTML - David

In programming we can make a distinction between **syntax** and **semantics**.

Broadly speaking syntax refers to the symbolic representation of code, and semantics refers to the meaning.

In HTML (Hypertext Markup Language), documents are structured through the use of syntactical tags to indicate and divide elements such as paragraphs, links, lists, images, quotes, and forms, among others. The tags inform the semantics, or meaning, of the webpage and its divisions.

If you inspect a website to look at its HTML, you will most often find the ```<div>``` tag used over and over to divide different regions of the page.

HTML actually has many more tags with a better semantic flavour than the most often used tags. These include tags like ```<section>```, ```<aside>```, ```<article>```, and ```<nav>```.

Semantic HTML is the careful use of these more explicit and semantically flavoured tags in creating HTML documents. There are a few reasons for this. For one, it improves the readability of the HTML, with sections and purposes better demarcated by the tags themselves, rather than needing to be distinguished from the anonymous cloud of ```<div>```s.

Semantic HTML also assists and enables accessibility features, including screen-readers, by providing more information about the structure of webpages and documents.

Unfortunately, it remains very common to find very unsemantic HTML in the wild, often because tools that create webpages (such as WYSIWYG pagebuilders) default to creating ```<div>```s to tag sections.




## CSS Execution Order - Rich

# CSS Style Application: Comprehensive Overview

# Specificity Hierarchy

| Priority | Selector Type | Description | Examples |
|:--------:|:------------:|:------------|:--------:|
| 1 (Highest) | Inline Styles | Directly on elements | `<h1 style="color: pink;">` |
| 2 | ID Selectors | Unique element identifiers | `#navbar` |
| 3 | Classes & Pseudo-classes | Targeted group styles | `.test`, `:hover` |
| 4 | Attributes | Element attribute matching | `[type="text"]` |
| 5 (Lowest) | Elements & Pseudo-elements | Basic HTML element styles | `h1`, `::before` |

# Cascade Algorithm Stages

1. **Origin & Importance**
  - Prioritize style sources
  - Handle `!important` declarations
  - Manage browser defaults

2. **Specificity Calculation**
  - Rank selectors by complexity
  - Resolve style conflicts
  - Apply most precise rules

3. **Source Order**
  - Last defined rule wins
  - Resolve equal-specificity conflicts
  - Cascade through stylesheets

4. **Inheritance**
  - Transmit styles from parent elements
  - Apply inherited properties
  - Use inheritance keywords

# Key Principles

- More specific selectors override less specific ones
- Inline styles have highest precedence
- Systematic, predictable style application

## Flexbox vs Grid - Anna 
There are strong similiarities between both, so it's easy to pick up grid if you've learnt flexbox
- Grid is great for structuring entire page layouts
    - You can arrange items in both rows and columns simultaneously 
- Flexbox is great for small components (nav bars, buttons, form layouts)
    - You can arrange items in a row or column, so items are aligned + distributed along a simple axis

Grid lets you code the website's exact look
- structured, fixed layout where elements are placed precisely
- define exact sizes, positions & spacing

Flexbox lets you code a flexible website
- dynamic layouts that adjust based on screensize and content 
- distributes space automatically based on available space

Flexbox layouts out an inline list of elements
CSS grid made them a grid of columns and rows

90% of the time - website navigation should be built with CSS flexbox.



### Flexbox 
#### Components
- Flex Container
- Flex items 
#### Flex Direction 
- Direction items are placed in the container. Default is row, but you can set row-reserve, column & column-reserve
#### Alignment
- Justify-content: Aligning flex items along the main axis
- Align-items: Aligning flex items along the cross axis 
- Align-content: aligns multiple rows of flex items along the cross axis
#### Flex Wrap 
- by default items are placed on one line & content shrinks to fit
- flex wrap allows items to run onto multiple lines

### Grid
Grid container, grid items, grid lines, grid tracks, grid cells 
https://dev.to/ridoy_hasan/css-grid-a-deep-dive-55l7




## ARIA - Connor

ARIA arributes helps to make it more accessable and interactive on areas where it's not possible to do so in pure HTML, accessability like on users who only relies on a screen with no mouse.

A role can be given to an element, to specify what type to give to it, like "progressbar", "toolbar".

Properties and states can then be given to an element, to specify current values for it. Examples like:
- has a checkbox has been checked
- Setting current value and range to the progress bar
- Whenever if a dropdown box is currently drop down.

ARIA should only be used if absolute nessecary, if basic HTML do not have the support of such functionality. 