# static-site-in-angular
Repo - For allowing any repo to work with Angular. 

The idea is that a static site generator will only be used for the blog page. We want to be able to gut out Angular pages statically, by curling headless cms, running it through whatever static site generator you are using, and then have the routes be managed using Angular. 

I think this solution would be more scalable, and maintainable than re-writing a framework so that it works with a particular language. In fact, arguably, it can be independent of a static site generator, and work exclusively within Angular. Will start independent of any static site generator, so that it can work with Angular exclusively. This is done with the following pre-conceived notions in mind: 
1. Angular users(and really all people) for simplicity sake, would rather just use Headless CMS, and UI Framework. 
2. People are only using static site generator on a case per case basis. Would rather use UI framework for rest of page. 
3. Two areas where static site generation happens. Blog landing page, and and actual blog page. 
4. Script for curling and cutting out posts directory under blog folder(located in lib folder, using Nrwl's structure).
5. Using Javascript library, for converting from markdown to html. Static site generators will never be in the equation. 

Path moving forward to solve without static site generator: 
1. Styles will be contained within container page, e.g. `blog` page.
2. There will be a standard for what html classes will look like. 
3. Use `Strapi` for the headless CMS, and it's api. 
4. After curl process, `posts` folder, with number 1, until x will populate posts folder. 
4a. Only part of api needed for blog landing page in this process, is id's, title of blog, and url for images. 
4b. Assumption is that at this time, images are going to be hosted already on a server. 
4c. For actual blog page, will simply have html. Should just need content for blog, and images, being hosted, should already be there already. 

###Considerations at this time###
