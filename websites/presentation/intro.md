# Website workshop

```


                  🌐 www.yourwebsite.com
     ¯\_( ͡° ͜ʖ ͡°)_/¯ 




░░░░░░░░░░░░░░░░░░░░░░░░░ Presented by Dr. Paul Strøm
```

---
## The advantage of having a website

- People can find you online easier
  - Relevant for potential employers, collaborators, people wanting to invite you to give talks, media / outreach
  - Ads legitimacy that you are an astronomer
  - Makes you look more professional (and shows that you have website skills)

---
## The advantage of having a website

Once people have found your website
- You control what people find out about you
- You can showcase what you want to show (show your best work)
- You show them your expertise

---

```
~~~graph-easy --as=boxart
        [ In astronomy your website is your business card ]
~~~
```


---

## Ways of making a website

There are many ways of making a website such as:

- Code it ```from scratch``` using HTML, CSS, PHP, JavaScript etc...
- Edit a ```pre-made template``` (HTML5 Up!)
- Use a ```static site generator``` (Jekyll, Hugo, Zola, Gatsby)
- Use a ```content management system``` (Wordpress, Joomla, Drupal).

---

## Creating a website from scratch or editing a template

Doing this can be very time consuming and requires familiarity with a lot languages such as HTML, CSS (PHP, JavaScript etc.).

- It is not flexible. Limited features.
- Can require a lot of work to maintain the website
- You are "stuck with the look"

---

## Using a content management system

Although this can be user-friendly it is also

- Cumbersome to install yourself (you need to create and connect a database)
- Not easy to move or deploy on another server
- It can be overkill for what we need
- Needs maintenance

---

## Using a static site generator

This is no perfect solution (no user-friendly interface, limited templates, steep learning curve if you want to create your own template). But there are some clear advantages:

- Fast and easily portable
- Flexible and highly customisable
- Easy to deploy and run locally
- Once set up, easy to maintain

---

## Zola

For this project we will use Zola.

Zola is a static site generator (SSG) which uses as input Markdown. It then converts your markdown files into html webpages.

- No dependencies
- Really fast
- Excellent documentation

---

## The plan for this session

```
~~~graph-easy --as=boxart
[ Create a website using zola ] - upload to -> [ GitHub pages ]
~~~
```

---

## The plan for this session

```
┌─────────────────────────────┐
│   Add content to .md files  │
└──────────────┬──────────────┘
               │
               ▼ 
      ┌─────────────────┐
      │ Zola used to    │ ──────┐
      │ convert to HTML │       │
      └─────────────────┘       ▼
                           ┌──────────┐
                           │  GitHub  │
                           └──────────┘
```

---

## Using the terminal

You can use the Command Line Interface (CLI) or just and move things around in folders visually.

Use what text editor you like. Something simple like ```nano``` will work great, alternatively ```notepad/notepad++``` for Windows or ```sublime text``` for MacOS. Personally I prefer ```vim``` (neovim actually).

---

## Using the terminal

```sh
cd - change directory
mkdir - make a directory
ls - list a directory
touch example.txt - will create a blank file called example.txt 
```

---

## Let's go!

Create a directory where you want to store your website.

```bash
mkdir website
cd website
zola init
```

You will be asked a few questions. For now just ```hit enter```. We will be changing this later anyways.

---

## What did zola create?

```sh
ls
```

```sh
config.toml <-- The configuration / settings file  
content <-- where the website content goes 
public <-- where the "compiled" website goes when ready
sass <-- Your css files [ignore]
static <-- Any files which will not change such as images
templates <-- where you place your own template files [ignore]
themes <-- where you put the website themes
```
---
## Launch your website on localhost

```bash
$ zola serve
```
This will show your website (but there won't be much content yet).

Click on install themes. Then click the link to the list of themes. For our demonstration we will pick the theme ```DeepThought```.

Go to the DeepThought git homepage.

---

## Clone the repository into your themes folder

```bash
cd themes
git clone git@github.com:RatanShreshtha/DeepThought.git 
cd ..
```
---

## Replace your config.toml file

Replace your config.toml file with that belonging to the theme.

```sh
cp themes/DeepThought/config.toml .
```
---

## Edit your config.toml file
Open config.toml and make the following edits:

```toml
base_url = "https://username.github.io"
```

Add the following line somewhere in the beginning:

```toml
theme = "DeepThought"
```

---

## Re-run zola serve

Once any changes have been made to the ```config.toml``` for them to be visible we have to re-run the zola serve command again.

```sh
zola serve
```

To interrupt the currently running session you can use:

Ctrl + C / ⌘ + C


---

## Add content or suffer Error 404!

```sh
cd content
touch _index.md
```

Edit ```content/_index.md``` in your favourite text editor.

---

```content/_index.md```

```toml
+++
title = "Welcome!"
description = "Website of Your Name"
+++

Thank you for visiting.
```

---

## Refresh your website and look

The content of ```content/_index.md``` should be visible.

---
## Add a research page

In the ```content``` folder create a folder called ```research``` and add a ```_index.md``` file with the following content:

---

```content/research/_index.md```

```toml
+++
title = "Research"
description = "An overview of what I have been working on recently"
+++

Page content here.
```

---

## Edit the menu

To find this research page we have to link to it from the menu.  

We do this in the ```config.toml``` file.

---

```config.toml```

```
navbar_items = [
    { code = "en", nav_items = [
        { url = "$BASE_URL/", name = "Home" },
        { url = "$BASE_URL/posts", name = "Posts" },
        { url = "$BASE_URL/research", name = "Research" },
        { url = "$BASE_URL/tags", name = "Tags" },
        { url = "$BASE_URL/categories", name = "Categories" },
    ] },
]
```

---

## Restart zola serve and referesh

Hopefully your will see your research page upon a refresh.

---

## Do the same for blog posts

- Create an ```_index.md``` file in a new directory called ```content/posts```
- Then create a md file, with any name. Example: ```wake_trip.md```

---

```content/posts/_index.md```

```toml
+++
title = "Posts"
description = "My blog posts"
sort_by = "date"
+++
```

---

```content/posts/wake_trip.md```

```toml
+++
title="My trip to the UK with WAKE"
date=2022-07-16

[taxonomies]
categories = ["Free time"]
tags = ["trip", "UK"]
+++

I had a great trip.
```

---

## Create more posts

```sh
cp wake_trip.md trip_to_italy.md
```

and edit the file.

---

## Let's refresh and look

Notice how the tags and categories work.

---
## Let us customise!

Please navigate to the ```static``` folder and create a directory called ```images```. Place an image of yourself in that folder.

Next replace the avatar parameter in the ```config.toml``` file to point to this image:

```toml
avatar = "images/you.jpg"
```

---
## Creating a GitHub pages repository to host the website

It is all well and good having a website locally, but we wish to show it to the world!

Go onto GitHub and create an empty repository with the name

```
~~~graph-easy --as=boxart
[ username.github.io ]
~~~
```

---

## Deploy your website

In the root directory of your website issue the command

```sh
zola build
```

This will convert your website into html and css files which you can push to github. Copy the files in the public folder to the new repository

cp -r public/* ../paultheastronomer.github.io

---

## Deploy your website

Navigate to the GitHub repository and do the following

```git
git init
git branch -M main
git remote add origin git@github.com:paultheastronomer/paultheastronomer.github.io.git
git add .
git commit -m "initial commit"
git push -u origin main
```
---

## View your work online

In a browser go to

```
~~~graph-easy --as=boxart
[ username.github.io ]
~~~
```

and enjoy!
