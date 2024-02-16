---
title: 'How I Keep Track of my Research'
date: 2024-01-26
permalink: /posts/2024/01/research-pipeline/
tags:
  - tools
---

Through my undergrad and in my first year of grad school, I had no clue how to do background research. I'm talking finding papers, keep track of what I have read (hopefully with some simple notes or the pdf's too), and how to find gaps or future directions to investigate. While I am still new to the space and am likely rediscovering the wheel, I struggled finding anyone who laid out their "wheel design" plainly. So, let's do that here.

# The Core Tools
My current process of management relies on a few tools:
- Paper management system
- Search engine
- Graph construction tools
- Note taking system
- 
Each of these tools serves a niche task, and are utilized to do what they do best. There is a [common philosophy in the Unix sphere](https://www.wikiwand.com/en/Unix_philosophy), such that each task is minimal in scope and does the task it needs to well. As such, you can easily swap one of the systems for another. I would advise, however, to ensure that when you are trying a new system that you first check to see if you can export any data you want to save into a universal format. For example, I can export all the data stored in my paper management system of choice, Zotero, to a bibtex or ris file then feed that into another system, like Mendeley. What we are trying to do is allow ourselves the space to grow without either losing data or needlessly losing time to data-entry. It is also key that you look into the underlying companies and possible flaw with them (i.e., if you are still using Google or Bing, why? Consider Brave and DuckDuckGo, or, better yet, a combination of all four). I will point out some issues that I have found and considered below, but this is part of the reason that we stress modularity and backing up your work. What will you do if tomorrow the system that you store all your knowledge in decides to invest in practices that you cannot support (financially or morally)?

## Paper Management System
This system store all your papers and allows you to have a database record. There are many ways to do this, but there are a few key features that I would consider essential (notice that my early method of a directory with all the papers and scattered notes of what I read does not meet these requirements): 
1. Allows for saving, tagging, and sorting by meta data. <Br>
  Storing the basics of the details of the papers you are looking at is the bare minimum, you need to have the flexibility to add personalized tags (I *need* to be able to tag things as "read" or "unread", and I would guess that you do too). Sorting and querrying on specific information is important too; how many papers are unread? What is the timeline of papers? What papers were made by the same person/people/group (more on this later)?
2. Allows exporting to a standardized datatype.<Br>
  This may be more domain specific, as the technical requirements in publishing will change, but at least having a predictable datatype is essential. Zotero allows you to export to a variety of types including BibTeX, CSV, RIS, JSON, and more. I am sure the other big hitters let you do the same. But having a JSON or CSV means you can pass the exported data through another system to convert it into the specific format you want. On that point: never write your own formatted citations! Humans are dumb and bad at following rigid rule structures, computers are great at this. Fill in the information, and double check it is correct, but let a computer system finalize the structure for you. This allow allows you to leave that hair in your scalp when there was a miscommunication and the citations need to be in Chicago and not MLA like you thought.
3. Can be arbitrarily large.<Br>
   Text files, as citations tend to be, are small files. You should be able to store as many as you could reasonably need. Avoid saving PDFs of the papers in the system (save them locally and add a link to the file or a link to the website sourcing it), this will likely eat up any data-cap a company may give you. If a system sets a limit on the number of entries you can have, run. There are free versions of the software that will work just as well (may not be as pretty, but they work and work well).

Anything else is extra and depends on how you work best. What are some of the systems to look into? 
- [Zotero](https://www.zotero.org/)<Br>
  This is what I use, and it work really well. Like any of the good ones, there is a Chromium plugin to export data for you. The syncing process works seamlessly between the various computers that I use. The project is [open source](https://github.com/zotero/zotero) and managed by [Digital Scholar](https://digitalscholar.org/). The system is committed to being for the people and has the infrastructure to stay that way.
- [Endnote](https://endnote.com/)<Br>
  [Clarivate's](https://clarivate.com/) Endnote is the pretty and expensive choice. If you are familiar with IDEs, it seems the Endnote is to Zotero as Pycharm/Jetbrains is to Visual Studio Code (a better parallel would probably be Atom, but since that got sunset, VScode is more relevant). If you know colleges who already use it and your institution/company has a subscription for you, it's worth at least looking at. [RefWorks](https://about.proquest.com/en/products-services/refworks/) is a similar product from the same company.
- [Mendeley](https://www.mendeley.com/)<Br>
  From my understanding, Mendeley used to be great, then Elsevier bought them in 2023, and they did what large companies do best. As Elsevier is one of the largest distributors or papers, the citation process is robust and reliable within system (using the the Scopus database). It is too early to tell, but there is a mumble of systematic issues with Mendeley. It seems to be free, and I know there are programs to export data out of Mendeley into Zotero, so it is work a look.
- Spreadsheets<Br>
  One of my committee members recently shared her strategy for saving papers (before a few years ago she had none at all!): Google sheets. The idea works with Google sheets, Excel, text files, or even a SQL database. You do all the manual data entry and design your system from the bottom up. I would urge you not to go this direction, as all data entry will either be manual or through a creative solution (the three above all have easy to use plugins), how the data will be exported needs to be thought of at creation to avoid issues, and a lack of one of the Unix tennets: "Make each program do one thing well." You can't argue that everyone has the ability to use a spreadsheet, and thus anyone can view your database.

## Search Engine
How are you finding your papers? There are many ways search for new papers, and my go to is [Google Scholar](https://scholar.google.com/). Similarly, you have [Elsevier's Mendeley](https://www.mendeley.com/), [Web of Science](https://www.webofscience.com/wos), [Semantic Scholar](https://www.semanticscholar.org/), and [more](https://paperpile.com/g/academic-search-engines/); there are even domain specific engines like [Papers with Code](https://paperswithcode.com/about). 1

The functionality that you are looking for are:
1. Title and abstract searching
2. Links to the full paper
3. Up-ladder search; that is being able to look at papers derived from this work (cited by) and recommendations on related papers.
4. Citation information; while not necessary, the ability to get most of the citation information in one click is useful.

## Graph Construction Tool
[3 New Tools to Try for Literature Mapping](https://aarontay.medium.com/3-new-tools-to-try-for-literature-mapping-connected-papers-inciteful-and-litmaps-a399f27622a)
This is currently where my personal investigations are ongoing. I have recently found the power of graph construction tools. The purpose of these systems are to take seed papers, think of these are papers that are fundamental to your work and those you find intriquing, and provide you with new papers or common themes from those papers. This is similar to doing a two step citation review (what papers were cited by this seed paper, and who cited that previous paper) and a cited by search (who cited the papers I have in my list). Some provide you with the list of papers and statistics upfront, like Inciteful and Connected Papers, some assist you through a research process, giving papers to look at and asking if you want to add them to the graph, like Research Rabbit and Lit Maps. 

- [Inciteful](https://inciteful.xyz/)<Br>
  This is my personal choice at the moment. It plays with Zotero fantastically.
- [Lit Maps](https://app.litmaps.com/)<Br>
- [Research Rabbit](https://researchrabbitapp.com/)<Br>
- [Connected Papers](https://www.connectedpapers.com/)<Br>
  From what I understand, Connected Papers uses both a citation based method and some simple topic extraction methods to provide you with a web of connected papers and unconnected papers that share similar themes. From my experience, the former does the heavy lifting, but it is an intriguing idea. The product has recently become a free-mium model, allowing for only a few free queries a month.

## Note Taking System
Understand how you take notes, and how you want to. Some people do great with a large system specially built to be productive, others (like myself) are better with smaller chaotic systems. Take a look at [this GitHub project README](https://github.com/bramses/bramses-highly-opinionated-vault-2023/blob/main/README.md) for some of the ideas behind some opinions on the topic. The baseline we are looking for is an ability for you to take notes on papers, then link those notes to the papers in question. Many PDF views allow you to leave annotations in the PDF documents, Zotero allows you to leave notes directly in the app attached to the entry, I personally use a notebook and tag sections with papers when relevant. When you are reading through papers, make sure you have a system available for you to take notes.

# My Current Work Flow
- [Google Scholar](https://scholar.google.com/)
- [Zotero](https://www.zotero.org/)
  - Read/Unread tags with color coordinated color blocks
  - Collections for different projects
![Example image of my Zotero setup](/images/zotero.png)
- Chromium based browser with Zotero plugin (search in your web extension store - links may not work)
- [Inciteful](https://inciteful.xyz/) with Zotero bibtex
![Example image of plugging Zotero information into Inciteful](/images/incitefulxyz.png)
- [Okular PDF viewer](https://okular.kde.org/) (I am currently looking for a replacement as Okular comes with unnecessary KDE bloat) and [Pencil](https://www.wikiwand.com/en/Pencil)/[Paper](https://www.wikiwand.com/en/Paper)

# AI Tools
With the rise of generally successful natural language processing models, the question arises of whether we can reliably use these models to sift through the mountains of literature that exists today. The answer: somewhat. I would not be doing my due dilagence is I didn't voice that these models rely on "averaging" over all text on the internet, using a probabilistic model of the space opposed to an explicitly imposed symbolic knowledge of some sort. This idea pops up in the idea of the grounding problem. When a NLP model gives you a result, we are not guarenteed that such answer is grounded in some sort of definitional axiomatic root. As such, it could easily be hallucinating (making up facts for the purpose of delivering a convincing narrative) or weaving an inconsistent arguement. Both are unsound arguments, the first from using a valid argument with false premises and the second using true premises with invalid arguments. All this said, analyze everything you read from a model under the assumption that the claims are unsound, using them as suggestions for directions in personal research.

We have already seen some AI models above, but here is a short list of NLP based models that I have looked into (most are based off a Generative Pre-trained Transformer (GPT), often using OpenAI's work). 
- [Consensus](https://www.consensus.app)
- [SciSpace](https://typeset.io/): Cool website that allows you to search for topics/questions and get related papers. The results are then aggregated using CoPilot to create a synopsis of the results. A tabular list is returned with information according to proposed questions (i.e., what is the TL;DR of the paper, what were the contributions, etc.). The website offers pdf scraping. When looking at one paper, CoPilot can be used to explain text and math/tables. 
- [HeyScience](https://www.heyscience.ai/)
- [ResearchBudddy](https://researchbuddy.app/): I have not properly tested this model yet, as it requires you to sign up to use it. It has a good reviews on [product hunt](https://www.producthunt.com/products/researchbuddy-app).
- [Writeful](https://www.writefull.com), [Grammarly](https://www.grammarly.com/), 
- [Jenni](https://jenni.ai/), [Wisio](https://wisio.app/#blog), [Paperpal](https://paperpal.com/pricing)
- [Penelope](https://www.penelope.ai), and  
- [Kudos](https://www.growkudos.com/)