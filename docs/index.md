# News list templates for eXo Platform
A set of content list templates (in GTMPL code format) for displaying eXo Platform news articles.

### How to add content list templates in my eXo Platform site?
As a functional admin, you can easily add these templates to your eXo Platform site. See [this documentation](https://docs.exoplatform.org/en/6.1/Administration.html#list-templates).  
For more information and/or help, contact your eXo solutions consultant. To discuss your solutions consulting services credit, you may reach out to your eXo client success representative.

### Where to report issues or propose improvements for these templates?
In the [issues tab](https://github.com/marwenmema/exo-news-list-templates/issues) of this repo. Or talk to your eXo solutions consultant (see above).

# Overview of the templates:

## Features:
* **Cross-browser support** (except IE)
* **Mobile-ready**: The templates are responsive. Their responsiveness is not simply based on viewport (screen) size, but rather on container size! This means that they adapt based on the width value of the **area** of the page where you put them instead of the width of the **whole page**. [Skip the following paragraph description if you are not interested in how I implemented this.] This was a **_very_** important requirement I've set for myself when making these templates due to the nature of how they're used. Think about it: They are not static web page components, they are componants that can be placed in varying places and situations (for example on the header of a page, or squeezed in the narrow right column area of a space's home page, etc...). So their responsive break points need to be based on parent containers. Unfortunately, container-based media queries still do not exist in pure CSS. It's a major lack today in the world of CSS due to it being so tricky to implement (a lot is written on it on the internet explaining that). But it's highly anticipated by developers and we are indeed getting there. Once it becomes popular and well supported by browsers, then we can use it. Meanwhile, the best solution I have found (and have implemented in all of my templates) is this one by Philip Walton which relies on very simple vanilla JavaScript and has great browser support today since it relies on [ResizeObserver](https://developer.mozilla.org/en-US/docs/Web/API/ResizeObserver): [https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem](https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem/)
* **Clean, pre-fixed and commented code**: Or at least I tried. The idea is to make it transferable to facilitate potential productization.
* **No external libraries/dependencies**: Relying exclusively on built in eXo Platform resources. (The platform's REST services are leveraged when needed and its built-in JQuery library is invoked when needed. That's it.)
* **Colors are based on platform theme/branding variables**: Colors used in these templates automatically inherit to your eXo Platform site's theme colors (see eXo's branding feature).
* **Tooltips** are implemented wherever needed.
* **Variations** I tried to provide what I felt might be useful variations on the same templates. The goal is to facilitate accomodating client preferences without having to mess with CSS mods. For example: an article list with images, and the same without images. The former for clients who have a more image-focused design approach, and the latter for those with a more info/text-focused minimalistic approach. (From experience I know both preferences exist in the real world, hence the attempt to accomodate them both.)

Features that are lacking and that I want to add in the future and if people tell me they want them:

* **Accessibility**: i.e. Ensuring a good accessibility score.   
* **Loading skeleton effects**: I've implemented it successfully in one of the templates and plan to generalize it when time permits and if people are interested.  
* **Placeholder when no articles are available yet**: Right now nothing is shown when no articles are available.  
* **Multi-lingual support for labels like "See all"**: Right now labels like that are hard coded in the templates. You can change them manually. For true multi-lingual support, I'm leaving that for if these get productized. But then again, something like the "header name" that are exposed in CLV display parameters (and which most of my templates support, so they are not hard-coded) are not multi-lingual by design at this time (product limitation). So there isn't really true multi-lingual support either way.

## Video demo:
I introduce the templates in this video:

## Naming convention:
The names of templates are structured as follows:  
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

**Image slider 1a**

![image](https://user-images.githubusercontent.com/9139631/122273824-c992d380-ced9-11eb-899b-897883156ea2.png)

[GET IT HERE]()

**Image slide 1b**

A variation without article summary.

[GET IT HERE]()

### Image slider 2:

Similar to the above, except this one shows more information (like the article's space name) and is better suited for less wide areas such as half or 2/3 of the web page. 

**Image slider 2a**

![image](https://user-images.githubusercontent.com/9139631/122273521-6b65f080-ced9-11eb-89e0-8bad19107870.png)

[GET IT HERE]()

**Image slide 2b**

A variation without article summary.

[GET IT HERE]()

### Featured articles mosaic 1:

A small grid/mosaic of articles, suitable for displaying featured articles at the top of a page at about two thirds of the page width. For example:

![image](https://user-images.githubusercontent.com/9139631/122273257-23df6480-ced9-11eb-8220-7c5535abcd57.png)

**Featured articles mosaic 1a**

Main variation displaying article space names.

![image](https://user-images.githubusercontent.com/9139631/122274507-838a3f80-ceda-11eb-93e8-015b314a435c.png)

[GET IT HERE]()

**Featured articles mosaic 1b**

A variation displaying publication dates instead of space names.

[GET IT HERE]()

**Featured articles mosaic 1c**

Displays 5 articles instead of 4, with space names.

![image](https://user-images.githubusercontent.com/9139631/122274636-aae10c80-ceda-11eb-857b-f3603bbf9006.png)

[GET IT HERE]()

**Featured articles mosaic 1d**  

Displays 5 articles instead of 4, with publication dates instead of space names.

[GET IT HERE]()

### Featured articles with highlight 1:

Displays a set of featured articles, with the latest one being more highlighted (hence the name). Suitable for use in a section of a page where you want to feature some articles (two thirds of page width works nice with this).

NOTE: This one is an improvement upon the existing (as of this writing) "Latest News" template in eXo Platform.

**Featured articles with highlight 1a**

![image](https://user-images.githubusercontent.com/9139631/122275038-2773eb00-cedb-11eb-8812-8aea11fd3194.png)

[GET IT HERE]()

**Featured articles with highlight 1b** 

A variation without the small article images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/122275264-67d36900-cedb-11eb-8e72-ea57cb47c647.png)

[GET IT HERE]()
