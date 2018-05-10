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
