Creating Your First Website
=============================

Creating a Project
-------------------

1.  Login to your Github account and create a new project on Github, look for the book icon with
    a "+" symbol, this is used to create a new project on Github.

2.  Give your project a memorable name, you can even create a project just on Cloud9, but it is
    usually preferrable to create a project on Github first.

3.  Login on [cloud9](https://c9.io/) using your github account (click the little octocat icon).

4.  Now that you are logged in on cloud9 you can open up your github project by finding it under
    "github projects" on the leftside, click on the project to create a new workspace to start
    working on it.

5.  You should now be able to open the project in the cloud9 IDE and begin working on it



Bootrapping your Project
-------------------------

1.  First start by downloading [Bootstrap](http://twitter.github.com/bootstrap/) and extracting
    it.

2.  Now, in cloud9 select "upload to this folder" and upload the css, img, js folders you extracted
    from bootstrap.zip

3.  Next download JQuery and then select the js folder and upload the jquery file to the JS folder 
    or you can simply use this later on when we get to adding scripts.

    ```html
    <script src="http://code.jquery.com/jquery-1.9.1.min.js"></script>
    ```

Committing Changes
--------------------

1.  Now, if you created this through github we can easily commit the changes by doing the following

2.  Open the terminal (bottom right)

    ```bash
    git status          (shows modified/untracked files)

    git add .           (this adds all the files to be committed)
 
    git commit          (type in a commit message and press ctrl + x and then Y to save)
    
    git push            (this sends your changes to github server)
    
    git pull            (download updates from github to local machine)
    ```


Creating Your First Website
----------------------------

1. Start by creating a new file, index.html this is the default html to show for your website

2.  We need to start by adding the basics, most times you just need to understand what these 
    mean, 99% of the time I just copy paste this template from my other projects  
    - If you are lost google!  
    - <!DOCTYPE html> is the default for an HTML5 website  
    - meta is just metadata such as author and language  
    - <link> references the CSS files    

3.  The main body is just the bootstrap navbar and a title message, nothing special!
    The following is a great place to see some more [Bootstrap Examples](http://twitter.github.com/bootstrap/getting-started.html#examples)

4.  Now you can view your website locally in cloud9 and update it until it's the way you like, 
    press the play button to view your website.

5.  For a simple website in HTML like what we are doing you can view your result by pressing the 
    "preview" button, normally for PHP/etc.. you can use Play

6.  Once you are happy with the results we will begin the deployment step



Deploying Your Website
-----------------------

1.  Heroku uses Cedar and doesn't support static websites (limitation of PAAS!)

2.  Create the following files which contain the contents listed below the file
    
    ```
    index.php 
    <?php echo file_get_contents('index.html'); ?>
      
    .htaccess
    php_flag engine off
    ```

3.  Now to deploy    
    - Click the deploy button (hot air balloon) and click "+"  
    - Select heroku from the list and click "Create new" and give your app
      a unique name  
    - click on the project and click ADD this should now create an empty app
      on your heroku account, you can verify it was created by logging in on
      Heroku.  

4.  Now that it shows your heroku "app" as active in the deploy tab you can
    deploy your website to heroku by doing the following.  
    - open the terminal (bottom right)  
    - enter

    ```
    git remote add heroku git@heroku.com:<your Heroku app name>.git
    ```      
    - This is the name of the heroku app you just created! You can also get this by
      looking into heroku clicking settings and copying the git url git@heroku.com.....
    - Now push your changes to the Heroku Server.   
    
    ```
    git push heroku master  # this sends your code to the heroku server
    ```
    - It will now launch your web site and give you a link to the domain

5.  Congrats you have your own website hosted for free and you even have a domain
    name (something that costs about $15 a year for free)



    
  
