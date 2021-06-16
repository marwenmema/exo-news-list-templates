# News list templates for eXo Platform
A set of content list templates (in GTMPL code format) for displaying eXo Platform news articles.

### How to add/remove/update content list templates in my eXo Platform site?
As an administrator, go to **Administration > CMS Settings > Templates > List**.  To add a new template, click "**Add template**", go to one of the templates in this repository and copy its code, paste the template code in the "Content" field, write the template name in the "**Name**" fields, leave "Template type" set to "**Content**", and then click "**Save**".
You will then start to see this template as one of the template options available within the display settings of your content list viewer portlets. 
For more information, contact your eXo solutions consultant. To discuss your solutions consulting services credit, you may reach out to your eXo client success representative.

### How to report issues or propose improvements?
Use the "Issues" tab above, or talk to your eXo solutions consultant (see above).

# Overview of the templates:

## Features:
* **Cross-browser support** (except IE of course)
* **Mobile-ready**: The templates are responsive. Their responsiveness is not simply based on viewport (screen) size, but rather on container size! [Skip the following paragraph description if you are not interested in how I implemented this.] This means that they adapt based on the width value of the **area** of the page where you put them instead of the width of the **whole page**. This was VERY important for me because of the nature of these templates. Think about it. They are not static web pages, they are componants that can be placed in varying places and situations (on the header of a page, or squeezed in the narrow right column area of a space's home page, etc...). So their responsive break points need to be based on parent containers. Unfortunately, container-based media queries still do not exist in pure CSS. It's a major lack today in the world of CSS due to it being so tricky to implement (a lot is written on it on the internet explaining that). But it's highly anticipated by developers and we are indeed getting there. Once it becomes popular and well supported by browsers, then we can use it. Meanwhile, the best alternative solution I have found (and have implemented in all of my templates) is this popular one by Philip Walton which relies on very simple vanilla JavaScript and has great browser support today: https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem/
* **Clean, pre-fixed and commented code**: Or at least I tried. The idea is to make it transferable to facilitate potential productization.
* **No external libraries/dependencies**: Relying exclusively on built in eXo Platform resources. (The platform's REST services are leveraged when needed and its built-in JQuery library is invoked when needed. That's it.)
* **Colors are based on platform theme/branding variables**: Colors used in these templates automatically adapt to your eXo Platform site's theme colors (see eXo's branding feature), thanks to CSS3 variables.


## Video demo:
I introduce the templates in this video:

## Naming convention:
The naming of the templates is organized as follows:  
[Template **type**] + [a number representing **a template** under that type] + [a letter representing **a variation** on the same template]  

For example:
* Image slider 1a
* Image slider 1b
* Image slider 2a
* Image slider 2b
* Article list 1a  and so on...

## List of templates & their descriptions:

### Image slider 1:

Displays articles in an automatic slideshow/carousel. The auto slide switching interval is 10 seconds. You can adjust it in the javascript snippet inside the template (look around line 432).

NOTE: This is an improvement upon the existing (as of this writing) "news slider" template in eXo Platform.
Note: If you (or your client) doesn't like the subtle auto-zoom effect on the images, you can deactivate it (take a look at the CSS code around line 117). My intention was to make the slider feel alive and calling for some attention without being too distracting.

Image slider 1a (main variation)

SCREENSHOT (big)

Image slide 1b (a variation without article summary)

SCREENSHOT (small)

### Image slider 2:

Similar to the above, except this one shows more information (like the article's space name) and is better suited for less wide areas such as half or 2/3 of the web page. 

Image slider 2a (main variation)

SCREENSHOT (big)

Image slide 2b (a variation without article summary)

SCREENSHOT (small)

### Featured articles mosaic 1:

A small grid/mosaic of articles, suitable for displaying features articles at the top of a page at about two thirds of the page width.

![image](https://user-images.githubusercontent.com/9139631/122273257-23df6480-ced9-11eb-8220-7c5535abcd57.png)

Image slider 2a (main variation displaying article space names)

SCREENSHOT (big)

Image slide 2b (a variation displaying publication dates instead of space names)

SCREENSHOT (small)

Image slide 2c (5 articles instead of 4, with space names)

SCREENSHOT (small)

Image slide 2d (5 articles instead of 4, with publication date)

SCREENSHOT (small)

### Featured articles with highlight 1:

Displays a set of featured articles, with the latest one being more highlighted (hence the name). Suitable for use in a section of a page (two thirds of a page works nice with this) where you want to feature some articles.

NOTE: This one is an improvement upon the existing (as of this writing) "Latest News" template in eXo Platform.
