# SACA Group Website - Tutorial Branch

This branch will be showing how to modify the website and it's content. I will also detail the steps I've taken at each step.

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
