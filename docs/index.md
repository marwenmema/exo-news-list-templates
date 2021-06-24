# News list templates for eXo Platform
A set of content list templates (in GTMPL code format) for displaying eXo Platform news articles. They are ready to use—as a functional admin you can add them to your eXo Platform site ([see how](https://docs.exoplatform.org/en/6.1/Administration.html#list-templates)).

### Where to report issues & propose improvements?
In the [issues tab](https://github.com/marwenmema/exo-news-list-templates/issues) of this repo. Or talk to your eXo solutions consultant.

### Features:

* **CROSS-BROWSER** (except Internet Explorer)

* **MOBILE READY**: The templates are responsive. Their responsiveness is not simply based on viewport (screen) size, but rather on container size! This means that they adapt based on the width value of the **area** of the page where you put them instead of the width of the **whole page**. [Skip the following paragraph description if you are not interested in how I implemented this.] This was a **_very_** important requirement I've set for myself when making these templates due to the nature of how they're used. Think about it: They are not static web page components, they are componants that can be placed in varying places and situations (for example on the header of a page, or squeezed in the narrow right column area of a space's home page, etc...). So their responsive break points need to be based on parent containers. Unfortunately, container-based media queries still do not exist in pure CSS. It's a major lack today in the world of CSS due to it being so tricky to implement (a lot is written on it on the internet explaining that). But it's highly anticipated by developers and we are indeed getting there. Once it becomes popular and well supported by browsers, then we can use it. Meanwhile, the best solution I have found (and have implemented in all of my templates) is this one by Philip Walton which relies on very simple vanilla JavaScript and, being reliant on [ResizeObserver](https://developer.mozilla.org/en-US/docs/Web/API/ResizeObserver), has very good browser support today: [https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem](https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem/)

* **MULTI-LINGUAL**: All labels (like the "See all" button) are multi-lingual and automatically appear in the user's platform language. Translations are built into the templates themselves. They are available in the following 8 languages: English, French, Spanish, German, Italian, Portuguese, Russian, Arabic. (I'm open to adding more languages upon request.)

* **Clean, pre-fixed and commented code**: (Or at least I tried.) The aim is to make it transferable to facilitate any potential productization.

* **No external libraries/dependencies**: Relying exclusively on built-in eXo Platform resources. (REST services and built in JQuery library is invoked when needed. That's all.)

* **Colors based on platform theme/branding**: All main colors used in these templates automatically inherit the platform's theme colors including colors that you personalized using [eXo Platform's branding feature](https://docs.exoplatform.org/en/6.1/Administration.html#branding-exo-platform).

* **Tooltips** are implemented where needed.

* **Template variations** I tried to provide what I felt might be useful variations on the same templates. The goal is to facilitate accomodating client preferences without having to mess with CSS mods and template forking. For example: an article list with images, and the same without images. The former is for clients who have a more image-focused aesthetic approach or branding guidelines, and the latter for those with a more info/text-focused minimalistic approach. (Because I know from experience that both preferences exist in the real world.)

Below are features that are lacking (because I had considered them as "nice to have" requirements versus the above which I had considered as "must have"). I'll add them if people tell me they're really needed:

* **Accessibility**: i.e. ensuring a good accessibility score. (I didn't bother since the platform itself is not accessibility-compliant yet. But I will if it does.)
* **Loading skeleton effects**: I've implemented it successfully in one of the templates and plan to generalize it when time permits and if people are interested.  
* **Placeholder when no articles are available yet**: Right now nothing is shown when no articles are available (done on purpose). Let me know if you want a placeholder implemented, for which template(s) exactly, and why.

## VIDEO DEMO:

I introduce the templates in this video: 

## TEMPLAE NAMING CONVENTION:

The names of templates are structured as follows:  
[Template **type**] + [a number representing **a template** under that type] + [a letter representing **a variation** on the same template]  

For example:
* Image slider 1a
* Image slider 1b
* Image slider 2a
* Image slider 2b
* Article list 1a  and so on...

## LIST OF TEMPLATES:

### **Image slider 1a** - ([GET IT HERE]())

Displays articles in an automatic slideshow/carousel. The auto slide switching interval is 10 seconds. You can adjust it in the javascript snippet inside the template (look around line 432).

NOTE: This is an improvement upon the existing (as of this writing) "news slider" template in eXo Platform.
Note: If you (or your client) doesn't like the subtle auto-zoom effect on the images, you can deactivate it (take a look at the CSS code around line 117). My intention was to make the slider feel alive and calling for some attention without being too distracting.

![image](https://user-images.githubusercontent.com/9139631/122273824-c992d380-ced9-11eb-899b-897883156ea2.png)

### **Image slide 1b** - ([GET IT HERE]())

A variation without article summary.

### **Image slider 2a** - ([GET IT HERE]())

An image slider/carousel that shows more information (such as the article's space name) and is better suited for less wide areas such as half or 2/3 of the web page. 

![image](https://user-images.githubusercontent.com/9139631/122273521-6b65f080-ced9-11eb-89e0-8bad19107870.png)

### **Image slide 2b** - ([GET IT HERE]())

A variation without article summary.

### **Featured articles mosaic 1a** - ([GET IT HERE]())

A small grid/mosaic of articles, suitable for displaying featured articles at the top of a page at about two thirds of the page width. For example:

![image](https://user-images.githubusercontent.com/9139631/122273257-23df6480-ced9-11eb-8220-7c5535abcd57.png)

The main variation of this templates below includes article space names.

![image](https://user-images.githubusercontent.com/9139631/122274507-838a3f80-ceda-11eb-93e8-015b314a435c.png)

### **Featured articles mosaic 1b** - ([GET IT HERE]())

A variation that displays publication dates instead of space names.

### **Featured articles mosaic 1c** - ([GET IT HERE]())

A variation that displays 5 articles instead of 4, with space names.

![image](https://user-images.githubusercontent.com/9139631/122274636-aae10c80-ceda-11eb-857b-f3603bbf9006.png)

### **Featured articles mosaic 1d** - ([GET IT HERE]())
Same as above, with publication dates instead of space names.

### **Featured articles with highlight 1a** - ([GET IT HERE]())

Displays a set of featured articles, with the latest one being more highlighted (hence the name). Suitable for use in a section of a page where you want to feature some articles (two thirds of page width works nice with this).

NOTE: This one is a remake the existing (as of this writing) "Latest News" template in eXo Platform which I find has some UI issues (inconsistent paddings, no mouse-over effects, titles that truncate too soon/in just one line, etc...). This remake addresses those issues and provides variations based on client feedback that I've had about this template.

![image](https://user-images.githubusercontent.com/9139631/122275038-2773eb00-cedb-11eb-8812-8aea11fd3194.png)

### **Featured articles with highlight 1b** - ([GET IT HERE]())

A variation without the small article images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/122275264-67d36900-cedb-11eb-8e72-ea57cb47c647.png)

### **Featured articles with highlight 2a** - ([GET IT HERE]())

Similar to the above with a little different positioning of elements.

![image](https://user-images.githubusercontent.com/9139631/123260717-cad18b00-d4ed-11eb-8b27-ee4b8b7ecc15.png)

### **Featured articles with highlight 2b** - ([GET IT HERE]())

A variation without the secondary images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/123261123-43d0e280-d4ee-11eb-971f-0ebc9ccb0f50.png)

### **Featured articles with highlight 3a** - ([GET IT HERE]())

Potentially useful as an alternatif page image header.

![image](https://user-images.githubusercontent.com/9139631/123261369-98745d80-d4ee-11eb-9871-8f0fe41afd84.png)

### **Featured articles with highlight 3b** - ([GET IT HERE]())

A variation with 4 secondary articles instead of 3.

![image](https://user-images.githubusercontent.com/9139631/123261524-c5c10b80-d4ee-11eb-9d5a-5fb6941ffc2d.png)
