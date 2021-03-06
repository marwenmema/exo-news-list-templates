# News list templates for eXo Platform
A set of content list templates (in GTMPL code format) for displaying eXo Platform news articles. They are ready to use—as a functional admin you can add them to your eXo Platform site ([see how](https://docs.exoplatform.org/en/6.1/Administration.html#list-templates)).

### Where to report issues & propose improvements?
In the [issues tab](https://github.com/marwenmema/exo-news-list-templates/issues) of this repo. Or talk to your eXo solutions consultant.

### Features:

* **CROSS-BROWSER** (except Internet Explorer)

* **MOBILE READY**: The templates are responsive. Their responsiveness is not simply based on viewport (screen) size, but rather on container size! This means that they adapt based on the width value of the _area_ of the page where you put them instead of the width of the _whole page_. [Skip the following paragraph if you are not interested in how I did this.] This was a _very_ important requirement I had set for making these templates due to the nature of how they're used. Think about it: They're not static web page components, they are components that can be placed in varying locations on an eXo page (for example on the header of a page, or squeezed in the narrow right column area of a space's Stream page, etc...). So their responsive break points need to be based on the location of the page itself, not on the window size. (Except for some things like facilitating use of fingers on mobile, then I would use pure screen-based media queries.) Unfortunately, container-based media queries still do not exist in pure CSS. (Yes, that's right. It's impossible with CSS. (A lot is written on it on the internet explaining why it's tricky to create this CSS feature.) But it's finally coming. Once it becomes popular and well supported by browsers, then we can start to use it. Meanwhile, the best (cleanest/most efficient) alternative JavaScript-based solution I have found (and thus have implemented in all of my templates) is this one by Philip Walton which relies on very simple vanilla JavaScript and, being reliant on [ResizeObserver](https://developer.mozilla.org/en-US/docs/Web/API/ResizeObserver), has very good browser support today: [https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem](https://philipwalton.com/articles/responsive-components-a-solution-to-the-container-queries-problem/)

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
* **Finger swiping on mobile**: I'm implementing this as soon as I have time whether you ask me to or not. :p

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

### **Image slider 1a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/2afed70e78b355b4e877d20d0fab906724137603/Image%20slider%201/Image%20slider%201a.gtmpl))

Displays articles in an automatic slideshow/carousel. The auto slide switching interval is 10 seconds. You can adjust it in the javascript snippet inside the template (look around line 432).  

NOTE: This is an improvement upon the existing (as of this writing) "news slider" template in eXo Platform.  
Note: If you (or your client) doesn't like the subtle auto-zoom effect on the images, you can deactivate it (take a look at the CSS code around line 117). My intention was to make the slider feel alive and calling for some attention without being too distracting.

![image](https://user-images.githubusercontent.com/9139631/122273824-c992d380-ced9-11eb-899b-897883156ea2.png)

### **Image slider 1b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/906da22452e3f5f879fc928793b1b9da542944e6/Image%20slider%201/Image%20slider%201b.gtmpl))

A variation without article summary.

### **Image slider 2a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/906da22452e3f5f879fc928793b1b9da542944e6/Image%20slider%202/Image%20slider%202a.gtmpl))

An image slider/carousel that shows more information (such as the article's space name) and is better suited for less wide areas such as half or 2/3 of the web page. 

![image](https://user-images.githubusercontent.com/9139631/122273521-6b65f080-ced9-11eb-89e0-8bad19107870.png)

### **Image slider 2b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/906da22452e3f5f879fc928793b1b9da542944e6/Image%20slider%202/Image%20slider%202b.gtmpl))

A variation without article summary.

### **Featured articles mosaic 1a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20mosaic%201/Featured%20articles%20mosaic%201a.gtmpl)

A small grid/mosaic of articles, suitable for displaying featured articles at the top of a page at about two thirds of the page width. For example:

![image](https://user-images.githubusercontent.com/9139631/122273257-23df6480-ced9-11eb-8220-7c5535abcd57.png)

The main variation of this templates below includes article space names.

![image](https://user-images.githubusercontent.com/9139631/122274507-838a3f80-ceda-11eb-93e8-015b314a435c.png)

### **Featured articles mosaic 1b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20mosaic%201/Featured%20articles%20mosaic%201b.gtmpl)

A variation that displays publication dates instead of space names.

### **Featured articles mosaic 1c** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20mosaic%201/Featured%20articles%20mosaic%201c.gtmpl))

A variation that displays 5 articles instead of 4, with space names.

![image](https://user-images.githubusercontent.com/9139631/122274636-aae10c80-ceda-11eb-857b-f3603bbf9006.png)

### **Featured articles mosaic 1d** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20mosaic%201/Featured%20articles%20mosaic%201d.gtmpl))

Same as above, with publication dates instead of space names.

### **Featured articles with highlight 1a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20with%20highlight%201/Featured%20articles%20with%20highlight%201a.gtmpl))

Displays a set of featured articles, with the latest one being more highlighted (hence the name). Suitable for use in a section of a page where you want to feature some articles (two thirds of page width works nice with this).  

NOTE: This one is a remake the existing (as of this writing) "Latest News" template in eXo Platform which I find has some UI issues (inconsistent paddings, no mouse-over effects, titles that truncate too soon/in just one line, etc...). This remake addresses those issues and provides variations based on client feedback that I've had about this template.

![image](https://user-images.githubusercontent.com/9139631/122275038-2773eb00-cedb-11eb-8812-8aea11fd3194.png)

### **Featured articles with highlight 1b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20with%20highlight%201/Featured%20articles%20with%20highlight%201b.gtmpl))

A variation without the small article images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/122275264-67d36900-cedb-11eb-8e72-ea57cb47c647.png)

### **Featured articles with highlight 2a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20with%20highlight%202/Featured%20articles%20with%20highlight%202a.gtmpl))

Similar to the above with a little different positioning of elements.

![image](https://user-images.githubusercontent.com/9139631/123260717-cad18b00-d4ed-11eb-8b27-ee4b8b7ecc15.png)

### **Featured articles with highlight 2b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20with%20highlight%202/Featured%20articles%20with%20highlight%202b.gtmpl))

A variation without the secondary images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/123261123-43d0e280-d4ee-11eb-971f-0ebc9ccb0f50.png)

### **Featured articles with highlight 3a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20with%20highlight%203/Featured%20articles%20with%20highlight%203a.gtmpl))

Potentially useful as an alternatif page image header.  
NOTE: As you reduce the container width, at some point the secondary/right-side article images disappear.

![image](https://user-images.githubusercontent.com/9139631/123261369-98745d80-d4ee-11eb-9871-8f0fe41afd84.png)

### **Featured articles with highlight 3b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Featured%20articles%20with%20highlight%203/Featured%20articles%20with%20highlight%203b.gtmpl))

A variation with 4 secondary articles instead of 3.

![image](https://user-images.githubusercontent.com/9139631/123261524-c5c10b80-d4ee-11eb-9d5a-5fb6941ffc2d.png)

### **Article list 1a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%201%20(small%20single%20column)/Article%20list%201a.gtmpl))

Let us now explore different "list" layouts.  

This first one lets you have a small one-column list including article space names. Ideal for displaying news on a small'ish container somewhere on your page. (Like in the Snapshot page's bottom boxes, a space Stream page's right column, etc...)  
NOTE: If you squeeze it enough (reduce container width), the images will disappear.

![image](https://user-images.githubusercontent.com/9139631/123287731-dd0bf300-d506-11eb-9413-f94536c484a4.png)

### **Article list 1b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%201%20(small%20single%20column)/Article%20list%201b.gtmpl))

A variation of the above without images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/123288292-53a8f080-d507-11eb-888f-bd480e3c6fca.png)

### **Article list 1c** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%201%20(small%20single%20column)/Article%20list%201c.gtmpl))

Same concept (small one-column article list), but with __author names__ instead of __space names__. So more suited for displaying news from _a single space_ where it would be redundant to display the same space name over and over again. ;-)  
NOTE: If you squeeze it enough (reduce container width), the images will disappear.

![image](https://user-images.githubusercontent.com/9139631/123288853-d631b000-d507-11eb-88e5-d5dcf563a1d6.png)

### **Article list 1d** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%201%20(small%20single%20column)/Article%20list%201d.gtmpl))

A variation of the above without images. (For clients who prefer "less pictures".)

![image](https://user-images.githubusercontent.com/9139631/123289012-f8c3c900-d507-11eb-8926-3c714fe0c2c8.png)

### **Article list 2a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%202%20(small%20multi-column)/Article%20list%202a.gtmpl))

Arranges articles in a __multi-column list__, in order to scale nicely horizontally.  

How many columns depends on the container width you put it in. It's adaptive. The wider the area, the more columns you get. If you squeeze it in a small enough space, it becomes one column just like the above templates.  

How tall the columns are then depends on how many overall articles there are. (And you can of course restrict the max number of overall displayed articles from your content list portlet settings just like with all the templates in fact.)

![image](https://user-images.githubusercontent.com/9139631/123289632-89020e00-d508-11eb-9b89-5f2931d2f5b8.png)

### **Article list 2b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%202%20(small%20multi-column)/Article%20list%202b.gtmpl))

Same as above but without images. (For clients who prefer "less pictures".)  
Very reminicent of newspaper websites.

![image](https://user-images.githubusercontent.com/9139631/123293035-8a810580-d50b-11eb-89f8-6d4c8e99049b.png)

### **Article list 2c** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%202%20(small%20multi-column)/Article%20list%202c.gtmpl))

Same concept (adaptive multi-column article list), but with __author names__ instead of __space names__. So more suited for displaying news from _a single space_ where it would be redundant to display the same space name over and over again. ;-)  

![image](https://user-images.githubusercontent.com/9139631/123291119-ba2f0e00-d509-11eb-848e-63e8f0fec726.png)

### **Article list 2d** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%202%20(small%20multi-column)/Article%20list%202d.gtmpl))

Same as above but without images. (For clients who prefer "less pictures".)  

![image](https://user-images.githubusercontent.com/9139631/123291361-ef3b6080-d509-11eb-9e68-2dd6b1578f0e.png)

### **Article list 3a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%203%20(big%20single%20column)/Article%20list%203a.gtmpl))

A _bigger_ one-column article list. Ideal for an all-page blog for example.  

![image](https://user-images.githubusercontent.com/9139631/123291753-4f320700-d50a-11eb-98c4-317ac7256825.png)

### **Article list 3b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/62250c7bd995f2471deeaf498b323d423f920b9e/Article%20list%203%20(big%20single%20column)/Article%20list%203b.gtmpl))

Same as above, but with author names instead of space names. So more suited for displaying news from _a single space_ where it would be redundant to display the same space name over and over again. ;-)  

![image](https://user-images.githubusercontent.com/9139631/123292465-fa42c080-d50a-11eb-8a97-6c6e2931488e.png)

### **Articles cards slider 1a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/e0e4a03dc63342d3a0837fb3384579792e77b510/Articles%20cards%20slider%201/Articles%20cards%20slider%201a.gtmpl))

A horizontal slider of article cards. You can scroll through this slider by clicking the right/left scroll arrow.  

Pointing your mouse over one of the cards displays its summary (with a nice slide-up animation).  
Clicking on the reactions (likes/comments) takes you to the news article's and scrolls down to its likes/comments section.  

NOTE: If you disable "show header" through your portlet display setting, the header area with "Featured news" and the "See all" button will be hidden and a card will be added at the end of the slider that will be named "See all articles". The role of this card is to replace the "See all button" by keeping it possible for the user to see go browse for more articles.  

![image](https://user-images.githubusercontent.com/9139631/123297701-b9997600-d50f-11eb-95da-1b8026ab4426.png)

### **Articles cards slider 1b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/b05a124bab1caa980a6cb8f0b5fcdae1e2365bb1/Articles%20cards%20slider%201/Articles%20cards%20slider%201b.gtmpl))

A variation of the above without space names. So more suited for displaying news from _a single space_ where it would be redundant to display the same space name over and over again. ;-)  

### **Articles cards slider 2a** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/b05a124bab1caa980a6cb8f0b5fcdae1e2365bb1/Articles%20cards%20slider%202%20(stories)/Articles%20cards%20slider%202a.gtmpl))

A smaller-sized (than the above) horizontal slider of article cards. Pointing your mouse on one of the cards reveals its number of reactions and views.
This one is inspired by Facebook stories. Try it on top of an activity stream where it will look nice and familiar, and enjoy pinning your "top stories".  

![image](https://user-images.githubusercontent.com/9139631/123298809-c9658a00-d510-11eb-8a9e-f02283b30d76.png)

### **Articles cards slider 2b** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/b05a124bab1caa980a6cb8f0b5fcdae1e2365bb1/Articles%20cards%20slider%202%20(stories)/Articles%20cards%20slider%202b.gtmpl))

A variation of the above without the author picture. (To get rid of the "too much of the same face" effect where needed.)  

### **Photo gallery widget** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/b05a124bab1caa980a6cb8f0b5fcdae1e2365bb1/Photo%20gallery%20widget/Photo%20gallery%20widget.gtmpl))

Sometimes a photo speaks better than words.  
I have seen a client posting some touching "silent" photos of their elderly care providers assisting people during times of a global healthcare crisis.   
Maybe you have a "photo gallery" space where a community manager wants to share photos regularly. Or maybe you want to organize a "photo of the day" or "photo of the month" thing.  

This widget is here to enable you to bring forth your latest photo in a section of your homepage for example. To share a photo, publish a little news article with an illustration image. This widget takes those articles and shows them in a stream/slider of photos (the photos are simply the illustration images of each publication/article. We want to always leverage the news feature here, not create a new feature).  

![image](https://user-images.githubusercontent.com/9139631/123301269-632e3680-d513-11eb-8baa-1ce98d85ee97.png)

The user can scroll through the photos using the "next" and "back" buttons:

![image](https://user-images.githubusercontent.com/9139631/123302085-3b8b9e00-d514-11eb-964a-3e1665ba69e8.png)

Clicking the photo switches to a full-screen mode (_this is just an overlay on the page, not a seperate page_) where the user can preview the photo, and continue to scroll back and forth between photos in full-screen:

![image](https://user-images.githubusercontent.com/9139631/123302356-8c9b9200-d514-11eb-9cdd-c1550fd36fe7.png)

Clicking the "close" button (top left) exits the full-screen mode.

### **Critical alerts ticker** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/b05a124bab1caa980a6cb8f0b5fcdae1e2365bb1/Critical%20alerts/Critical%20alerts%20ticker.gtmpl))

Displays critical alerts in a an automatic ticker (a horizontal roller where the text is animated/rolling from right to left).  
It's like what you see on news TV channels.  

Can be linked to an "emergency alerts" kind space and used to show important pinned alerts from it (like announcing unexpected site downtime, etc.) seperately from regular status quo news. If no alerts exist, this component disappears.

Pointing your mouse over the ticker pauses the rolling/animation effect if you want to read the announcement at a slower pace.
Clicking an alert opens the news article associated with it.

![gif](https://raw.githubusercontent.com/marwenmema/exo-news-list-templates/main/docs/Critical%20alerts%20ticker%20(GIF%20demo).gif)

### **Critical alerts slider** - ([GET IT HERE](https://github.com/marwenmema/exo-news-list-templates/blob/b05a124bab1caa980a6cb8f0b5fcdae1e2365bb1/Critical%20alerts/Critical%20alerts%20slider.gtmpl))

Same as the above, but with a slider display instead of an auto-animated ticker/roller.  

It switches to the next alert every 10 seconds. And you can switch back and forth between them using the next/previous buttons.  

![image](https://user-images.githubusercontent.com/9139631/123307580-91634480-d51a-11eb-990b-91407d2562fe.png)

