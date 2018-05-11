# SACA Group Website - Tutorial Branch

This branch will be showing how to modify the website and it's content. I will also detail the steps I've taken at each step.

### Good to know before modifying

This site uses jekyll and github pages to function. Knowing the following is very helpful in being able to make edits to the site (in order of importance):

* git
* Markdown
* html

[Here is a useful site for testing markdown](https://pandao.github.io/editor.md/en.html)

### Testing the site locally

To test the site locally you'll need to have a few things installed

* ruby
* gem
* jekyll
* bundler

Here is a [good guide](https://jekyllrb.com/docs/installation/#ubuntu) on how to set this up on ubuntu.

Once you have those installed cd to the local directory in which this project is contained. You'll then most likely have to run bundle install to install the neccessary jekyll components to run this.

Once all of that is said and done you can use the following to host the website locally

```bundle exec jekyll serve```

Then you can navigate your browser to 127.0.0.1:4000 to see the site.

### Adding a new sponsor (also how to take one away)

To add a sponsor you'll first need their logo, optionally a logo for the footer, and then you're ready to make the two modifications needed to add it to the site.

You can add the logo to the home page by adding an image tag to the /\_layouts/home.md, if you wrap it in <a href> tags, you can make a link to their website as well (this is done in the commit). The image will need to be added within a paragraph tag that wraps all of the sponsors, which is a bug found with the site. Shortly after this is added to the test branch this should be fixed in the main branch.

Next to add it to the footer, modify /\_includes/footer.html and add a similar a and image tag in the sponsors section. If there is another image to be used for the footer (one that is more square, etc), then you can change the image tag to reflect the path of the correct image.

For both of these, you will likely need to play with heights and widths of the images, I've gone ahead and done these for these images (see the style="" in the iamge tags), and then play around with the local copy of the website by chanigng the browser width and height before finally pushing it to production (the master branch).

To remove a sponsor, simply remove the a and image tags for the respective sponsor that is no longer actually a sponsor.

### Modifying the home slideshow

To do this you'll need to edit /\_layouts/home.html, and add the image you wish to feature to the images folder under some directory (I'm using /images/slider7001400/ for this example). I am unsure how different image height to width ratios will look on other devices, to be safe I've stuck with using images cropped and resized to 1500x500px.

It is a bit more manual than other steps, and requires editing HTML. 

In homelay.html you'll want to add two things: 

* A list item under carousel-indicators, so a user can see there is another image in the slideshow
* A div for the item with the image inside. 

You can change the image by changing the src attribute of the inner img. There can only be one item active picture, which should be the first in the list and is the first visible to a user when they navigate to the side.

The accompanying commit should showcase these changes, if there is any confusion or problems with this, please reach out to me.

### Adding news

To add news to the site you'll want to edit /\_data/news.yml

By default the nine most recent news posts will be shown on the home page. To change this limit, edit /\_includes/news.html and change ```limit:9``` to ```limit:n``` where n is the number of news articles which you want to article. You'll need a few fields for each news piece you want to feature, a date, the headline, and the description (named decr).

### Adding/changing text content

To modify the text in (most) pages, you'll need to modify the respective markdown file in /\_pages/. In this example, I've removed IoT research (we shouldn't actually do this), decided it might be nicer to have larger subtitles, and then added a link to the Wikipdia article for supercomputers. 

The page that is the most complex is the research page, this is because it includes data elements, as well as html (which any of the other files can include as well!).

Each page will start with a heading that looks like the following:

```
---
title: "SACA - Home"
layout: homelay
excerpt: "Secure and Advanced Computer Architecture (SACA) Research Group."
sitemap: false
permalink: /
---
```

The title is the title of the website to the browser and search results. The layout will be the html layout which this page fits into before being rendered (most will inherit textlay.html, that's the one for text based pages). The excerpt is the description that will be shown on google and other search engines. The sitemap field mandates whether this will be added to the sitemap.xml which doesn't actually generate currently (this shouldn't matter as of now). Finally, the permalink is the sub-url at which the page will be located, for example team.md is actually located at /members/.

If there are any questions with any of this, please e-mail me, or raise an issue on this branch! This is probably the most complex part of the site, but hopefully all we will need to do from here on out is edit markdown.

### Adding Master's Students

In this part of the tutorial, I'm adding a master's students field and moving Vamsee over to it. 

I first created the yaml file for master's students and named it _masterstudents.yml_ in the /\_data directory. Next I simply moved over the data for him to that file. He still won't show up at this point, that is because I hadn't added master's students to the page. 

To add master's students to the page, I modified \_pages/team.md to have another field, by copying and pasting the field for Ph.D. students, then changing which data file it grabs data from, by changing _phdstudents.yml_ to _masterstudents.yml_. 

I am not sure if we want to list past education experience for users, so a large bulk of each one of those blocks (for director, phd, masters, and undergrad) in the file is legacy from testing. I'll safely remove these soon more than likely to make the code simpler.

### Adding a Ph.D. student

To add Vamsee to the Ph.D. student list, I first add his image to /images/teampic/. You can see that I've added vamsee.jpg in this commit. Next I add the content for his bio to phdstudents.yml which is a yaml file that holds the data for each student. 

Each student is required to have a name, photo, and info field. To add an undergraduate student, you would take the same steps, adding the name, photo, and info to the ugstudents.yml

In the next tutorial I'll be adding a masters students listing, and add Vamsee to that area.

### Original readme   

This is the website of our academic research group at the University of Central Florida.

It is a fork of the website used by the Allan Lab, thanks to them for open sourcing their project.

This website is powered by Jekyll and some Bootstrap, Bootwatch. We tried to make it simple yet adaptable, so that it is easy for you to re-use it for your purpose. Plese feel free to copy and modify for your own purposes.  You don't have to link to us or mention us (but of course we appreciate it).

Go to *aboutwebsite.md*  to learn how to copy and modidy this page for your purpose. 
