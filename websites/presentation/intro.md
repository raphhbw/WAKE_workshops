# Website workshop

Presented by Dr. Paul Strøm

---
## The advantage of having a website

- You allow people to find you easier
  - This is important, especially if you want to be invited to give a talk or join a radio show, invited by a school to do outreach...
  - Ads legitimacy that you are an astronomer

Once people have found your website

- You control what people find about you
  - You can show that you know what you are talking about
  - You can showcase what you want to show


---

## Ways of making a website

There are may ways of making a website

- Code it from scratch using HTML, CSS, PHP, JavaScript etc...
- Use a template which you edit directly
- Use a static site generator
- Use a content management system such as Wordpress, Joomla, Drupal.

---

## Coding from scratch or using a template

Doing this can be very time consuming.

- It is not flexible.
- Can require a lot of work to maintain the website
- You need to know HTML, CSS (and perhaps even PHP, Javascript etc.)

---

## Using a content management system

Although this can be user-friendly it is also

- Cumbersome to install yourself (you need to create a connect a database)
- Is more prone to attack, such as spam comments
- Not easy to move or deploy on another server

---

## Using a static site generator

This is no perfect solution (no user-friendly interface, limited templates, steep learning curve if you want to create your own template). But there are some clear advantages:

- Fast and easily portable
- Flexible and highly customisable
- Easy to deploy and run locally


---

## The plan for this session

```
~~~graph-easy --as=boxart
[ Create a website using zola ] - upload to -> [ GitHub pages ]
~~~
```

---

## Using the terminal

You do not need to use the Command Line Interface (CLI) if you prefer to use your mouse and move things around in folders visually.

You are free to use what text editor you like. Something simple like **nano** will work great, alternatively **notepad/notepad++** for Windows or **sublime text** for MacOS. Personally I prefer **vim** (neovim actually).

```sh
cd - change directory
mkdir - make a directory
ls - list a directory
```

---
## Zola

For this project we will use Zola.

Zola is a static site generator (SSG) which uses as input content written in CommonMark, a strongly defined, highly compatible specification of Markdown.

---

## The plan
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

## Let's go!

Create a directory where you want to store your website.

```bash
mkdir website
cd website
zola init
```
- The URL of your website will be: https://username.github.io  
- Sass compilation? --> Yes  
- syntax highlighting? --> Yes  
- Search index? --> Yes

---

## What did zola create?

```sh
ls
```

```sh
config.toml <-- The configuration / settings file  
content <-- where the website content goes 
public <-- where the "compiled" website goes when ready
sass <-- Your css files [you won't use this]
static <-- Any files which will not change such as images
templates <-- where you place code should you wish to cutomise
themes <-- where you put the website themes
```
---
## Launch your website on localhost

```bash
$ zola serve
```
This will show your website (but there won't be much content yet).

Click on install themes. Then click the link to the list of themes. For our demonstration we will pick the theme DeepThought.

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
Open config.toml and add the following line somewhere in the beginning:

```toml
theme = "DeepThought"
```

Also make sure the base_url is changed back:

```toml
base_url = "https://username.github.io"
```

---

## Re-run the zola

Once any changes have been made to the *config.toml* for them to be visible we have to re-run the zola serve command again.

```sh
zola init
```

---

## Add content or suffer Error 404!

```sh
cd content
touch _index.md
```

Edit _index.md in your favourite text editor and add:

```toml
+++
title = "Welcome!"
description = "Website of Your Name"
+++

Thank you for visiting.
```

---

## Add a research page

In the ```content``` folder create a folder called ```research``` and add a ```_index.md``` file with the following content:

```toml
+++
title = "Research"
description = "An overview of what I have been working on recently"
+++

Page content here.
```

---

## Do the same for blog posts

- Create an _index.md file in a new directory called ```content/posts```
- Create a md file, for instance: ```wake_trip.md```

---

```_index.md```

```toml
+++
title = "Posts"
description = "My blog posts"
sort_by = "date"
+++
```

---

```wake_trip.md```

```toml
+++
title="My trip to the UK with WAKE"
date=2022-07-16

[taxonomies]
categories = ["Free time"]
tags = ["trip", "UK"]
+++

I had a great trip.

![](/images/wake.jpeg)
```

---

## Create more posts

```sh
cp wake_trip.md trip_to_italy.md
```

and edit the file.

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

Make the website public. Then clone the directory.

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
