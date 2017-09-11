---
layout: post
title:  "CLI Data Gem Project Journal"
date:   2017-09-11 03:12:50 +0000
---


Hello Fellow Coders!

This is my journey with the CLI Data Gem Project:

**8/3/2017 - Day One:**  I finished my ‘Student Scraper’ project on the 1st and it took me a few days to accomplish.  Yesterday I didn’t want to have anything to do with Flatiron or programming or anything and I took the whole day and just vegged out.  To get started today I am going to tackle this ‘CLI Data Gem’ project by going over all the instructions, resources and videos.  I watched Avi Flombaum’s video and he makes it look so easy!  I did walk through with him on Atom to get the ‘feel’ of the order of things.  Next I will go through the rest of the documentation.

**8/8/2017 – Day Two:**  I am going through the steps of what are the easy steps to complete, such as making a repository.  Then I will go through all the links on the lesson page to watch any tutorials and read through all the documentation.

**8/15/2017 – Day Three:**  Finishing up on videos and taking notes on what is needed for the project such as, Git Repo Address, Blog Post, Coding video sample, README.md file, Video demo of gem  and to publish my gem.  Attending the study group today on this project.  Study group did not go – not sure if the coordinator had issues, but I decided to watch the rest of the videos and tomorrow I will start to code.  Pushed up my spec.md to github.

**8/28/2017 – Day Four:**  Watched videos and uploaded a recording application (RecordMyDesktop) to record my process and the 30 minutes of how to use my gem.  I also took a few days off for the last part of summer with the eclipse and all and basic procrastination.  Now I must pursue the rest of my Flatiron School lessons.  Made gem called “knitting yarn deals”.

**8/29/2017 – Day Five:**  It’s on! I’m going to finish this project!  So I am going to record some of my thought process for the lab requirement.  Video recordings were not successful.  I will try to do this later in the project.  

**8/30/2017 – Day Six:**  Now to continue on with getting this project done! Figured out the scraping methods and changed some of the wording on my CLI.rb file.  I think I have a good roll on this.  I want to be done with this before Saturday, September 2nd.  I procrastinated too much and I thought it was going to be really hard.  I let this project intimidate me and now I need to kick it’s butt!  I can do this because I have the intelligence and the fortitude!  I will conquer!  I will get it done! I will go to bed now because I am tired.

**8/31/2017 – Day Seven:**  Worked on scraping methods and couldn’t make a ‘list’ for the CLI for the user to pick from.  Well, the user did have one option because I wrote the code for just one instance of a class.  I did attend a study group and found that maybe I should change up the files by adding a scraper.rb file. I kind of thought that I had a one instance of a class going, but I wasn’t totally sure.  I also knew deep down that I should do a scraper file, but I really didn’t want to re-do my project.  Not that I have to throw everything out. I just have to re-write some of my code and add a file or two.  I will be working on that tomorrow.  I got this!

**9/1/2017 –  Day Eight:**  Today I will tackle my files and try to think about patterns.  I will use the restaurant example to guide me.  I can do this! So, I’m looking at the pattern in the restaurant example and I did add an environment file.  I have my CLI.rb file and I will keep that as it for now.  I may have to readjust it, but overall it is working.

**9/4/2017 –  Day Nine:**  Today I am going over a video to see how I can build my CLI project.  Man, I am just getting so frustrated and I almost quit, but then I figured out some stuff on my project.  I have been using a couple of other student’s projects for an example.  I switched around some of the methods from the yarn_deal.rb to put it in the scraper.rb file.  Then I had a problem with my CLI.rb in the list_yarns method.  It just wouldn’t list and then boom, I changed the name of my variable from yarns to skeins and it now works.  

> def list_yarns
    @skein = KnittingYarnDeals::Scraper.this_day
    @skein.each.with_index(1) do |yarn, i|
      puts "#{i}. #{yarn.name} - #{yarn.price}"
    end
  end
> 	

Now to get the other things working in my project.

**9/5/2017 –  Day Ten:**  Now to get my app to work.  I have to make sure it shows my list, but not like this:

###### Hello! Check out the yarn deals for your next knitting project.
###### 
###### @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
###### 
###### 1. Wool of the Andes Worsted Yarn -
######     $1.99 / 50g ball
###### 2. Palette Yarn -
###### 
######     $3.49 / 50g ball
###### 3. Hawthorne Fingering Multi Yarn -
######     $6.59 - $10.99 / 100g Hank
###### 4. Chroma Twist Fingering -
######     $9.99 / 100g Hank
###### 5. Chroma Worsted Yarn -
######     $5.99 - $9.99 / 100g ball
###### 6. Chroma Twist Bulky -
######     $5.99 - $9.99 / 100g Hank
###### 7. Chroma Fingering Yarn -****

Well, I worked on this all day and couldn’t figure out the blank spaces in my list and how to get rid of them.  I tried changing the scraping method to try to get down to the exact css, but that didn’t work.  I tried different methods like select or each to iterate through my array to try to get rid of the blanks in my index.  Well, tomorrow is a new day.  Arg!!!!

**9/6/2017 –  Day Eleven:**  So I tried to figure out my blank spaces, but I could not.  I reached out on slack and Avi Flombaum helped me – Yay!  The code I tried to use wasn’t in the right place, but after Avi showed me it made sense.  


>def save
    if valid?
      @@all << self
    end
  end

  def valid?
    validate_name
  end

  def validate_name
    !@name.strip.empty?
  end
> 

So, I had to save my instances when they were valid.  I wasn’t doing that in my previous code.  It was saving everything and I just wanted the items that were not blank or nil.  Cool! I feel like I am getting closer to the end of my project.  Now I have to figure out how to give the user an option of picking the yarn they want to look at by entering the number next to the yarn and then a web page can open up to show the picture, price and all of that.  I did want to add the price, but it wasn’t coming up correct in the yarn package deals.  In the html, there was a previous price crossed out and then a new price.  I decided not to add that into my list.  I am keeping it in the code for now.

I got my code to work by putting the web site address on the screen, but that’s not what I want so far.  But I did get it to work when you type in the number to get that choice of yarn – yay!!  I figured out the description issue that I wanted to scrape the next web page when you click on the individual yarn product. I’m feeling more accomplished today than I have in a long time with this project!  

> yarn_array.each do |each_skein|
      yarn_ball = KnittingYarnDeals::YarnDeal.new
      yarn_ball.name = each_skein.css("a.titleSmall").text
      yarn_ball.price = each_skein.css("span.costSmall").text.delete(" ").gsub /^\s*/, ''
      yarn_ball.url = "http://www.knitpicks.com#{each_skein.css("a").attribute("href").value}"
      yarn_ball.description = Nokogiri::HTML(open(yarn_ball.url)).css("span.prodDesc").text.delete("").gsub /^\s*/, ''
> 

Tomorrow the world!!

**9/7/2017 –  Day Twelve:**  Ok, now to make sure I have the description of each yarn accessible to the user and that they can open a web page to see pictures and all of that.  I kept getting more information for my description that I did not need.  It looked like reviews and I just wanted the short description of the yarn.  Guess what!?  I thought that I had to delete words and use ‘gsub’ to get rid of the extra words.  Then I played with the scraping again and got it down to just the yarn description.  So cool!  Sometimes it isn’t a method replacement, but just playing with the html/css to put in the right div’s or span’s or id’s. I did learn more about gsub and using regex with that method.  For example, 

> x.gsub /.{3}$/, ‘’

will get rid of the last three characters from your string.

Now to clean up my CLI so that everything can flow a bit better for the user.  After that, I want to make available the web page for the user to access.  Not sure how I will do that, but it will be fun to figure out!  Ok! Now I have my CLI flowing!  Yay!  Now I want to try to get each page to open at the user’s whim.  See if I can do that.  So, I am not going to be able to finish tonight.  Got to take a break.  I am going to get this done!  I want to figure out the web page thing and then I will update all the directions and the rest of my files and then I should be done. 

**9/8/2017 –  Day Thirteen:**  So I am not able to make a ‘link’ in the command line like I thought I could.  I just left the web address and the user will just have to copy and paste.  All I have to do now is clean up my code and update the other files with directions, such as the gemspec file.  I will probably capture video on that.  Then to do a video on how to use my new gem!

**9/9/2017 –  Day Fourteen:**   I got up really early this morning. No, not to jump on the project and get it finished.  Ha Ha!  I went  to the Farmer’s Market in Cheyenne. Got my roasted chili’s and some other vegetables, like purple carrots.  Now I’m at my computer and I need to figure out how to run the gem as if I was a new person running the command line.  I changed my gemspec file and the readme file, but I can’t seem to make it work.  Below are links that helped me learn about gems and rvm, but I'm still not able to make the gem work with just typing in 'knitting_yarn_deals':

[gems-on-the-command-line](http://tomdebruijn.com/posts/gems-on-the-command-line/)

[managing-ruby-versions-and-gem-dependencies-from-a-net-perspective](http://www.hurryupandwait.io/blog/managing-ruby-versions-and-gem-dependencies-from-a-net-perspective)

[rvm-tutorial](http://www.natashatherobot.com/rvm-tutorial/)

Still trying to make my gem work in bash.  Not successful today.  The above links have pointed me in a direction. Hopefully tomorrow I can get this.  I’m doing a tutorial on Linux to see if I can find answers there.  There is also .rvm documentation that may help like the links above.

**9/10/2017 –  Day Fifteen:**   

This link is a good link to understand bash and the commands.  I did change my background picture on my terminal:

[BASH](http://bash.cyberciti.biz/guide/Main_Page)

Now after all of that I looked at my README.md file and found that all I had to do was type in ‘bundle exec rake install`.  Now it works.  I’m going to publish, video and wrap it up before I go to bed tonight!

There is an issue with me publishing my gem because it says I have more than one gem with the same name.  So, I will figure that one out, but I will get my video done and my blog which is this journal.  Then I can get my assessment in the next few days.  Whew! It was a long road for me on this project, but I must say, it’s not all that bad.  I did learn something on the way and I know I will learn from my assessment and beyond. 

I did take some days off in between with the end of summer approaching and I got to see the total eclipse near Lusk, Wyoming.  That was an adventure!  Maybe someday I can fill you in on that day and night!  I can honestly tell you that I did procrastinate on this project.  I felt a little intimidated and I wasn’t sure I would finish this project let alone the curriculum.  I did it!  My advice is don’t be afraid.  Tackle it with all that you’ve got because you got this far, you can do it!!

Thank you for reading my blog!  Happy Coding!
