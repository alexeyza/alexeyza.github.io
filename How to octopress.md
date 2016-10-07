#How to use Octopress
I found myself looking repeatedly for these commands, so I decided to store them in one single file.

##Installing
Clone [Octopress](https://github.com/imathis/octopress) (or fork):
```
git clone git://github.com/imathis/octopress.git octopress
cd octopress
```

Next, install dependencies:
```
gem install bundler
bundle install
```

Install the default Octopress theme (optional):
```
rake install
```

Install the [MediumFox theme](https://github.com/sevenadrian/MediumFox):
```
cd yourOctopress
git clone https://github.com/sevenadrian/MediumFox .themes/MediumFox
rake install['MediumFox']
rake generate
```

##Updating
First backup all the files (just in case).

Update Octopress:
```
git pull octopress master     # Get the latest Octopress
bundle install                # Keep gems updated
rake update_source            # update the template's source
rake update_style             # update the template's style
```

Update a theme:
```
cd octopress/.themes/MediumFox
git pull
rake install['MediumFox']
rake generate
```

##Posting
Create a new post/page:
```
rake new_post["title"] or rake new_page["title"]
```

Preview the blog locally:
```
rake generate   # Generates posts and pages into the public directory
rake watch      # Watches source/ and sass/ for changes and regenerates
rake preview    # Watches, and mounts a webserver at http://localhost:4000
```

##Deploying
```
rake generate
rake deploy
```

##Commiting the source to GitHub
```
git add .
git commit -m "message"
git push origin source
```