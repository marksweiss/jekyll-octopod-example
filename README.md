## Who is This For?

If you are an engineer thinking about launching a blog and/or podcast, this project is a great place to start. It really shines if you want to have a single unified web site for both a podcast feed and a blog feed. `jekyll` is a great static site generator for blogs. `jekyll-octopod` is a great `jekyll` plugin that adds almost everything you need to extend `jekyll` for hosting a podcast. But neither supports one site that have a separate blog and podcast feed. This modification/example does.

Here is a [working example](http://www.usingreflection.com).

The intent of this sample project is to give you a jump start.  Start with it, learn enough to control it, and build what you need. If you are a developer, you really should invest the modest amount of time to learn to use them to create the publishing setup that exactly fits your needs. The payoffs are a publishing workflow that is fast and minimal and lets you concentrate almost wholly on producing your content, and a savings of $10-40 a month vs. hosting and serving a blog and podcast episodes with a commercial hosting service.

This project is not a substitute for learning `jekyll` and `jekyll-octopod`. Both projects have excellent online documentation. To get started [install jekyll](https://jekyllrb.com/docs/installation/), then go to the excellent [jekyll-octopod site](https://jekyll-octopod.github.io/) and follow the installation instructions. Then come back here, clone this repo into a directory, and start hacking.

## What Unique Value Does This Project Provide?

This project modifies the underlying jekyll files to support having two feeds on your site, one for podcast entries and one for blog entries. You will see the included `all_episodes.md` page is the listing page for podcast episodes, and the included `show_blog.md` page is the listing page for blog entries.

To create new podcast episodes, copy the provided `_posts/sample_episode.md` file, give it a name like `my_first_episode.md`, and modify the front matter appropriately. Copy your episode audio file into the `episodes` folder. The name of your audio file must match the value you provide for the key `audio` in the `my_first_episode.md` file YAML front matter.

To create new blog posts, copy the provided `_posts/sample_post`, and again rename and modify the front matter as desired.

The underlying includes and templates will handle the following:

* episodes list in the episode feed which can be reached through the `all_episodes` page
* blog posts list in the blog feed which can be reached through the `blog` page
* the sidebar RSS links provide separate subscriptions to each feed

## What Other Features Does This Project Provide?

### Getting Site Search Working

This project also helps you jumpstart Google site search, by including a `_plugins` folder with the excellent `json-feed-jekyll` plugin in place. The included `_config.yaml` includes entries to configure this plugin. Complete documentation is [here](https://github.com/kaishin/json-feed-jekyll). To get site search working you need to do the following:

* Create your initial content so you have something to index and something for users to search for
* Run the `json-feed-jekyll` plugin to generate a `sitemap.xml` file in your project root
* Sign up for a Google Search Console account and follow the instructions to provide your domain(s). Upload the `sitemap.xml` file you generated as instructed.
* Wait a couple of days

### Starting With This -- Ending With Your Site

`jekyll` is useful to developers because it gives you a lot of control and features while requiring very little code from you. The cost is an expected one, lots of magic and layers of behavior you need to unravel to understand what is actually happening when you want to change what is happening. I can't help with you that, but this working example customizes many things relative to the default `jekyll-octopod` so you can learn from its code. Some examples among many:

* Uses YAML front matter to customize the `podigee` audio player style
* Customizes the icon in the browsable RSS feed
* Makes many changes to the sidebar include and layout, including adding a second RSS feed, moving the search box into the sidebar, adding a second Twitter link, displaying different text and displaying a different show log
* Modifies the behavior of selected entries in listings to not hyperlink their title text
