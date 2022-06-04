# rqkoelle
I do not know where this journey will end, but I do know where to start. Relaunch of my webpage based on {{distill}}

# setup

* setup new repo on github to host site & clone as new project in RStudio
* install / update latest versions of {distill}, {postcards}, and {rmarkdown}
* create web-site: distill::create_website(dir = ".", title = "mfeo", gh_pages = TRUE)
  ==> lean back for a minute ... website will be generated
  you can check out the dummy/start website in the docs folder, index.html
* close RStudio to make sure that the build pane is properly loaded in your project
  ==> Build Pane!
* (optional) add a postcard (about-ish): postcards::create_postcard(file = "tobi.Rmd")
  ==> template opens - augment as appropriate
  ==> add site name and pagename to _site.yml
  ==> build website to test (and see your new page)
  
  for postcard themeing check https://github.com/seankross/postcards#the-templates
  Note: I went with `trestles` for a start, but you can finetune with your own css.
* for styling: create_theme(name = "theme") 
  ==> this creates a template css with the parameters one can change, e.g. colour, font-size, etc.
  check out https://rstudio.github.io/distill/website.html#create-theme
  
  for site-wide application of theme, add theme: your-theme-name.css to _site.yml
  
* add a blog to your site. as simple as distill::create_post("welcome")
  A first blog post will establish the underlying infrastructure/folders
  
  Note: posts need to be knitted intentionally!
  
  for a blog "listing" page, let's create an "empty" rmarkdown file
  file.edit("blog.Rmd")
  add the following YAML
  ---
  title: "RQ's Blog"  # any title you want
  listing: posts      # define page type ... do not anything below the YAML!
  
  hook up the listings page in your index, i.e. _site.yml
  ---




