<!-- [![Netlify Status](https://api.netlify.com/api/v1/badges/8cfa8785-8df8-4aad-ad35-8f1c790b8baf/deploy-status)](https://app.netlify.com/sites/digital-garden-jekyll-template/deploys) -->

# Mad Spinning Top website

This repository contains the source code for the Mad Spinning Top website, currently hosted at:

https://mad-spinning-top.netlify.app/

It is a [Jekyll](https://jekyllrb.com/) website extended via a customised version of [Maxime Vaillancourt's Digital Garden](https://maximevaillancourt.com/blog/setting-up-your-own-digital-garden-with-jekyll).

## How to update and edit the site

It's relatively straightforward to make edits directly to the live website.  The website is made up of plain text files which anyone who is part of this project can edit here on Github's website.

### Editting the website

All the blog posts are contained within the folder `_notes`, so click into that...

![image](https://user-images.githubusercontent.com/8701448/176190297-77863a10-62a2-4a59-beaf-a9a43ba4e634.png)

... and then you should see a list of all the blog posts, with a folder called `things` at the top. I'll explain what goes in there in a moment.

![image](https://user-images.githubusercontent.com/8701448/176191043-9757ccfe-2343-4838-814c-0e5239d93732.png)

Look for the blog post you want to edit in this list. Click into it, and then to edit it click on the pencil icon in the top right of the blog's box.

![image](https://user-images.githubusercontent.com/8701448/176214419-f941f846-ec3c-437d-a8f8-476b7a68f658.png)

What you see now is the source code of the blog post. It is formatted
in a simple plaintext markup language called Markdown, perhaps with a
bit of html too, with the addition of a custom markup for highlighting
and backlinking propper names. Imagine this being a proof that has
been written on a typewriter for the eyes of a typesetter. Because of
the limitations of the typewriter, you might agree with the typesetter
on some special symbols for things like bold, italics, hyperlinks, and
so on. That's all a markup language is: a text-based language for
signifying formatting to an robot typesetter.

Let's start at the top.

#### Front Matter

At the top of the file you'll see something that looks like the
following. This is the [front
matter](https://jekyllrb.com/docs/front-matter/) and it contains
important metadata about the file, specifically the title and the
date. You can update the values of the date and title fields, but make
sure there's a space after the colon (`date: 2021-07-09`), and that the three
dashes (`---`) are on their own lines with nothing following them, and
the second of these has a blank line following it.

```
---
date: 2021-07-09
title: "Urbanism, Bibliographical Notes and Liane Mozère"
type: blog
---
```

### Body content

Following the front matter is the blog post content. This is probably
what you'll want to edit. 

Things to notice:

**Paragraphs** as designated by blank lines between blocks of text. The
system ignores the line breaks at the end of a line - you can make
them 50 words long or 5, the system will treat them as a single
paragraph block until it reaches a blank line.

**Italics** are designated by a single asterisk at the start and end of a
word or phrase, for example, `was originally a *Tel Quel* lecture from 1966`. `Command`+`I` (Mac) or `Ctrl`+`I` (Windows/Linux)

**Bold** is designated by two asterisks at the start and end of a word
or phrase, for example, `in the form of a **theory of intensities**`.

**Name backlinks**, which result in a name being able to be clicked on
the website for a pop-up box to appear, are designed by:
* Two square-brackets on either side of a *full name* 
  - `I met with my friend [[Gavin Bowd]] last week`
* Two square-brackets on either side of a  *surname*
  - `Re-reading [[Fourquet]] and [[Murard]]'s preface`
* A *full name* or *surname* separated by a vertical bar character
  (`|`) with two square brackets surrounding them. This is necessary
  for when you want the text to be something other than the full name
  or surname, for example the first name or a name with a possessive
  article on the end, but the box to still link to the person.
* `I remember a conversation with [[Sanja Perovic|Sanja]] about this.`
* `was written by [[Lion Murard|Lion (Murard)]]`
* `[[Fernand Oury|F. Oury]] on [[Célestin Freinet|Freinet]]`

The name backlinks need a relevant file in the `things/` folder to
link. 

**Bullet list items** are designated by a single dash (`-`) at the
start of a line. For example

```
- September 1971 -- Response to offer of funding -- Drafting of Chapter 1
'La Ville-ordinateur'

- May 1972 -- discussion Guattari, [[Fourquet]], Foucault (pp. 27-31)

- \[June 1972?\] 6 months of funding for exploratory research (the key
questions are: Is there a specificity to the urban? What is meant by
'Genealogy'?)
```

**Numbered list items** are designated by a number followed by a
fullstop and a space.

```
1. the history of the policies of the State, ...

2. the composition and reception history of *Anti-Œdipe*, ...

3. the internal politics and micro-history of the *Recherches* people
```

**Hyperlinks** to other websites can either be written in Markdown or as an html <a> tag
(my personal preference).

```
Markdown:
[KCL page of Patrick ffrench](https://www.kcl.ac.uk/people/patrick-ffrench) 

HTML: 
<a href="https://www.kcl.ac.uk/people/patrick-ffrench">KCL page of Patrick ffrench</a>
```

### Previewing edits
  
Although you can only see what the website looks like after you've commited your changes (below), it's a good idea to check if the Markdown is ok before doing so. Github allows you to preview the processed markdown. Click the Preview button at the top of the edit box.
  
![image](https://user-images.githubusercontent.com/8701448/176217005-ce2e6a7a-b279-4cf0-b345-be073764345f.png)

  
### Saving (committing) edits

Once you are satisfied with your edits, you need to 'commit' them. To
keep things simple, think of this as saving them, however doing so
with the ability to always go back to any previous save if something
goes wrong.

At the bottom of Github's edit page screen you'll see the 'Commit
changes' box, with two fields. The top for a title which concisely
summarises the changes made (necessary), the bottom for additional
comments (optional).

Writing titles effectively is an art. Try to start with a verb in
the imperative form, followed by a concise summary. For example

```
Correct typos on Taking a Step Back
Fix formatting on Right to Research
```

Don't fret too much about this, it's just for our reference.

Once you're done click 'Commit Changes'. This will set in motion an
algorithm which will compile the website and put it online. This might
take a couple of minutes. If you find that the live site does not
update, there may be a problem in the code so get in touch with Daniel
to look into it.

### Name Backlinks

What I'm unimaginatively calling a 'name backlink' is what allows for
a pop-up to appear when you click on a propper name. The formatting of
such a link within a blog post is described above. It's important to
understand that for them to actually link to a name, a separate file
is needed for that name, within the thin `_notes/things/` folder.

These are just small metadata files, one for every person.
- The filename should be surname.md. Eg `althusser.md`, `baldwin.md`,
  `bernheim.md`.
- The content should be nothing but front matter with the full name
  for a 'title', and a 'type' of 'person'. Eg:

```
---
title: "Louis Althusser"
type: person
---
```

or

```
---
title: "Félix Guattari"
type: "person"
---
```
  
## Need help?
  
It goes without saying that if you need any help, just get in touch with Daniel!

## License

Source code is available under the [MIT license](LICENSE.md).


