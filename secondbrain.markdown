---
layout: default
title: "Second Brain/Zettelkasten"
date: 2022-07-24 (first version)
permalink: /secondbrain/
image: "/assets/images/2022-07-24 Second Brain.png"
secondbrain_image: "/assets/images/Folder Structure Second Brain.png"
secondbrain_inprogress: "/assets/images/Writing the Post on Second Brain.png"
---

# Second Brain/Zettelkasten

![Jan Spörer's Second Brain Visualized in a Graph]({{ page.image }})

## Basic Idea
The second brain concept was first brought to my attention by [productivity book](https://www.ultraproductive.net){:target="_blank"} author [[Dr. Christian Poensgen]]. 

While there are different flavors to using a second brain, the basic idea is to have atomic notes that are interconnected.

Another important convention is to use [[Evergreen Notes]]. As the system organizes itself with minimal overhead and scaling costs, notes are meant to last. One does not need to delete old notes and one can revisit existing notes to gradually add information and refine low-quality notes as needed.

## Where Do These Strange Square Brackets Come From?
Throughout this post, you are seeing multiple `[[ ... ]]`-style annotations. Those are links to other notes. I originally wrote this post directly in my second brain (as any other post on this website) and I intentionally left the square brackets in.

## Implementations
[Obsidian](https://obsidian.md/) is my recommendation. It is available on all desktop operating systems. Obsidian, however, does not have free built-in backups and versioning. I use `git` to version my Obsidian second brain. You can also put your Obsidian files in a Google Drive folder, in another folder synced by a cloud provider, buy Obsidian Sync, or get used to `git` (ask me for help).

Obsidian is a great private Wiki, just that it performs quicker than any web-based Wiki page. Obsidian executes fully locally and feels like a breeze. The shortcuts in Obsidian make usage more productive and intuitive.

Implementation options include:
* [Obsidian](https://obsidian.md/) -> **Free, desktop-based**. No mobile version. Built-in sync costs money. But other automated sync options are available as well (Google Drive, `git`, and many others).
* [Roam Research](https://roamresearch.com/) -> Paid subscription, **browser-based**. 
* [Athens](https://www.athensresearch.org/) -> Free local version. Specialized on being a Wikipedia for startup **teams**. Thus emphasizes the idea of shared access. (Which would also be possible using multiple git-tracked repositories with Obsidian, each with different access permissions.)
* [RemNote](https://www.remnote.com/notes) -> Paid subscription. Ability to create flashcards. Available on **mobile devices**!
* [[The Archive]] -> Out of completeness, I also wanted to mention The Archive here.

## More Advanced Concepts and Recommendations for More Advanced Structures
While no second brain requires a classical folder structure, it still might be useful to at least give your second brain a minimal bit of rigid structure. **Links between notes** will still always be the most important structuring mechanism.

So first of all: **don't over-engineer this!** You will probably notice that links between notes already provide 10x better structure than any note-taking approach that you have used to far, even without any additional structure.

If you do would like to get a little bit more advanced, I recommend the `PARA` method by [[Tiago Forte]]. Check [this link](https://fortelabs.co/blog/para/). `PARA` will, at the very minimum, require you to drag-and-drop each new note into one of four different folders. That's an acceptable effort.

`PARA` divides your notes into `1_PROJECTS`, `2_AREAS`, `3_RESOURCES`, and `4_ARCHIVE`. Check the link mentioned in the previous paragraph, and here is my own interpretation:
* `1_PROJECTS`: Short-term, completable to dos. A completable to do would be "finish this homework". I tend not to use this folder much as it is too much overhead for me.
* `2_AREAS`: Long-term, **non-completable** to dos. These are areas of life that require a certain balance to be maintained. My `2_AREAS` folder contains the following sub-folders and one file:
```
|-2_AREAS
||-21e6
||-Commerzbank
||-Education
||-Finance
||-Leisure & Private
||-Physical Health & Longevity
||-Productivity
||-Psychology, Social Interaction, Happiness, Wellbeing, Wohlbefinden
||-Spoerico GmbH
||-Work
||-Ziele, Goals (file)
```
As you can see, these are crucial, high-level, long-term, never-ending areas in life that require constant attention.
* `3_RESOURCES` is, by far, the biggest chunk in my second brain. For each concept that I find interesting, I would create a note and put it in there. I also manage all static real-world concepts and objects there such as `Countries & Cities`, and `People`. I have hundreds of people notes in there and thousands of notes on tech-related concepts. (There are 22 sub-folders in my `3_RESOURCES`.) There is also a note called `Russian Invasion Into Ukraine 2022` with embedded videos about political and military analysis.
* `4_ARCHIVE` is where old `1_PROJECTS` go.

The PARA structure is simply a folder structure, see here:
![[Pasted image 20220724110130.png]]

Another good concept: [progressive summarization](https://fortelabs.co/blog/progressive-summarization-a-practical-technique-for-designing-discoverable-notes/) by [[Tiago Forte]].

Also check the [NESSLABS newsletter](https://bit.ly/368Dr5y) .

[NESSLABS guide to Roam Research](https://nesslabs.com/roam-research-beginner-guide).

A note on labels: **Do not use labels.** They are not necessary. if, after using a second brain for a year, you feel the need for labels, go ahead. 

## Resources for Beginners

### Video: Obsidian for Beginners

[https://youtu.be/QgbLb6QCK88](https://youtu.be/QgbLb6QCK88)

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/QgbLb6QCK88" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Explains that a Zettelkasten helps to separate information capture [[Capture - Progressive Summarization]] and organization [[Organize - PARA]] from the writing process. You can just WRITE. 

### Video: My Comprehensive Obsidian Workflow

[https://www.youtube.com/watch?v=Ewhfok91AdE&t=329s](https://www.youtube.com/watch?v=Ewhfok91AdE&t=329s)

<iframe width="560" height="315" src="https://www.youtube.com/embed/Ewhfok91AdE?start=332" frameborder="0" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Video: My Comprehensive Obsidian Workflow (Long Version)

[https://www.youtube.com/watch?v=wB89lJs5A3s](https://www.youtube.com/watch?v=wB89lJs5A3s)

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/wB89lJs5A3s" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## History of the Concept

[[Niklas Luhmann]] used the Zettelkasten method for note-taking. He had 90k index cards for his research.

Described his approach in an essay called ["Kommunikation mit Zettelkästen"](https://link.springer.com/chapter/10.1007/978-3-322-87749-9_19).

His Zettelkästen were made available in [digital format](https://niklas-luhmann-archiv.de/) in 2019.

Credits: Thanks for my colleague Leona Blehova for pointing out the origins of the Zettelkasten method.

## Bonus

See a screenshot of me in action writing this post in `markdown` format directly in Obsidian.

![Jan Spörer's Progress Writing the Blog Post]({{ page.secondbrain_inprogress }})

And a screenshot of my file explorer showing the `PARA` folder structure.

![Jan Spörer's PARA Folder Structure]({{ page.secondbrain_image }})

