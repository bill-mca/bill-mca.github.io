---
layout: page
title: Markdown Publishing
Author: Bill McAlister
---

Markdown is a writing format for text files that can be automatically converted to many other formats. I got interested in learning markdown when I learnt about GitHub pages. This service allows you to generate whole websites from your uploaded markdown. Markdown can also be transformed into PDFs and Word documents. Drafting documents in markdown leaves you open to later publish in any format or several at once.

Part of the appeal of using markdown to author content is that it is straight-forward to write scripts that query and edit it.  At a later date, if I decide a that I want to re-publish this website as a PDF, I might need to change the format of the references. Because it is markdown, I'll be able to write simple code to process the raw md files and make the necessary changes to the reference format. I can also throw all the markdown that I have ever written into a big folder and then use tools like grep to find all mentions, for example, of the term 'systems thinking'. 

Markdown can also be integrated with open-source collaboration transparency tools such as [git](https://git-scm.com/) and [make](https://www.gnu.org/software/make/). This way, the full process of authoring the document is open for anyone to see or replicate. I think this creates fascinating data especially for documents that are being maintained over a long time or remixed. In sum, I think markdown is the best way of encoding text for future knowledge systems and that learning to do it well will open up possibilities for me and just generally make the world a better place. 
 
## Objectives
1. **Workflow** --- Identify software and establish workflows for doing as much of my writing as possible in markdown and versioning it with git.
3. **Publishing documents** --- Author complicated documents in markdown that include academic citations, footnotes, internal references, figure captions etc. 
4. **Publishing websites** --- Be able to apply and customise Jekyll templates to design markdown based websites.

## Prior knowledge
**Limited.**

Before starting this course, I had an app on my phone to write notes in markdown so I've been taking all my personal notes in markdown for a few years. I had also published a very small amount of markdown as readmes for my major coding projects.  Below is the most sophisticated markdown I had written before starting the course. The [file can be found on my GitHub profile](https://github.com/bill-mca/geotag-leaflet/blob/main/README.md).

```
# geotag-leaflet

The purpose of this code is to allow me to quickly generate a map of a landscape following a site visit. I intend to be able to download photos from my phone and drone and use this tool to create a leaflet map in 10 minutes. these webmaps could be deployed to my website by another script for a rapid turnaround on a site assessment.

## Attribution
This is largely adapted from code writen by Jayson DeLancey and available in [this tutorial](https://developer.here.com/blog/getting-started-with-geocoding-exif-image-metadata-in-python3).

## Instructions
geojson_from_exif.py is a script that takes a path to a directory as input and outputs a geojson of all the geotagged jpegs in that folder to the stdout.

generate_thumbnails.py makes a copy of a directory with all jpegs shrunk to thumbnails.

webmap_from_photos.sh takes a path to a directory full of geotagged photos and will generate thumbnails and a json layer compatible with the included index.html template.
```

I'd never used Pandoc before and I'd always used Microsoft Word to author documents. Apart from some brief attempts at writing HTML, I've only ever used integrated content management systems to publish websites. I did have a go at using Jekyll once but didn't get very far. The presentation of this web-page represents the limits of my Jekyll capabilities.

## Progress

### Objective 1 - Workflow

#### March 2024

*Significant progress*

I've done a lot of writing in markdown since starting this course including [two skills work assessments](https://github.com/bill-mca/CYBN8001-Build-Skills/) and [this webpage](https://github.com/bill-mca/bill-mca.github.io)! I've experimented with a few markdown editors and decided that it doesn't really matter which one you use because markdown is so simplistic. My biggest success has been demystifying git by learning to use [Gitfiend](https://gitfiend.com/). 

I'm not comfortable that this objective has been reached. Once I've authored a few large documents I'll feel confident in the workflow that I've established.

#### June 2024

*Some further progress*

With a lot of tight deadlines in the second half of the semester I found myself abandoning markdown as my primary tool for writing. I wrote most of the problematique in Microsoft Word. There were a few reasons:
1. The editor I was using Stackedit, inexplicably deleted a lot of the notes that I had written. It supposedly saves stuff on to a folder in my Google Drive but, try as I might, I couldn't recover the content. That was a serious set-back in completing the learning potfolio assignment. I stopped using that Stackedit because losing a half-finished assignment would be catastrophic.
2. The other editor available on Chromebook, the default text editor, doesn't have a what you see is what you get (WYSIWYG) preview. It also doesn't have a spellchecker. Both of these are serious limitations when you are working on a tight time frame.

I'm going to need to invest a bit of time in experimentation if I want to succeed on this objective. I think I'll need to test which markdown editors I can get from the Debian container in my Chromebook. I'll also need to setup a Github hosted repo for my notes rather than storing them in less reliable locations.

#### November 2024

*Accomplished*

I'm satisfied that I've become quite competent at using Markdown to author content. Though I had struggles at the end of semester one and used other tools to produce documents, my habit of writing in Markdown recovered and I have since had a lot of practice[^sibanetics][^buildskills]. 

I'm comfortable that HackMD is amoung the best available authoring tools. However, depending on the situation, I sometimes use the default text editor on my Chromebook. HackMD is more powerful and allows me to commit directly to GitHub repositories. It also has a save as you go feature and the ability to preview what's being written. I typically use it to author long or complex documents. I'm also satisfied that Git and especially GitHub is a great way of storing and keeping track of my Markdown documents. As I noted in my March update, GitFiend has been a real game changer in making Git very easy and quick to use. I no longer hesitate in establishing new repositories, cloning them, branching them, reverting them, etc. and this granular versioning control over my documents is extremely powerful. I'm very satisfied that I've developed the skill to write in markdown and I'm confident that it will be useful in the future.

Starting out, I believe that I was looking for a single monolithic tool that would allow me to easily author markdown while previewing and also keeping track of versions and exporting into multiple formats. I realised that my perspective has changed and now I'm quite happy to maintain a library or libraries of different markdown documents and to edit and process these with numerous different tools as situationally required. I realised that I've effectively adopted the Unix philosophy in my approach to document authorship now. 

There's one tool for quick note taking, there's one tool for writing long documents, there's one tool for inserting citations, one tool for converting out into different formats, one tool for keeping track of versions, but all tools are simple to use and very effective at what they do.

### Objective 2 - Publishing documents

#### March 2024
*Some progress amid frustrations*

I have made PDF versions of my two skills work assignments but the process was not smooth for either of them. For skills work assignment 2 I resorted to making the PDF via some edits on a docx version because I was worried I wouldn't be able to debug the Pandoc errors in time for submission!

![My current setup of pandoc crashes anytime the markdown file includes an emoji.](src/no-emojis-allowed.png)

I've had frustrating errors thrown at me by Pandoc. Here's a list of the issues I encountered while trying to PDF Build Skills 2: 
1. The default margins are much too big
2. Some of the figures are given captions but some are not
3. Some of the ordered lists are not recognized as such and so drawn as big ugly blocks of text
4. Some hashes (##) were randomly inserted in the document
5. Heading sizes are hard to tell apart and the navigation pane of the PDF reader didn't show the expected hierarchy

![Pandoc's default PDF has enormous margins and it didn't recognise my list for some reason.](src/ugly-squashed-list.png)

I've struggled with adding references to markdown docs and had to use a workaround where Zotero outputs an HTML bibliography that I have to process with Pandoc before manually appending to the markdown document.

So far, I would've been better off using familiar tools such as Microsoft Word to do these assignments. The effort involved in proofing and debugging the Pandoc outputs has been substantial. nevertheless, I'm hopeful that, as my markdown familiarity and my authoring workflows improve, the whole process will get a lot smoother and I'll have a powerful new tool for publishing my work across formats. 

#### June 2024
*No further progress*

As described above, my habit of authoring in markdown fell apart towards the end of semester 1. I didn't get any practice using Pandoc to pull together complicated documents because I didn't have the content in markdown format. 

#### November 2024
*Accomplished but also... goal transcended*

I made a lot of progress towards learning how to publish good quality documents from my Markdown. However, my conception of this goal also changed somewhat. 

As part of our CPS build project, two of my peers, Amanda and Shi, made an effort to learn Git and publish Markdown into the same repository as me to document our project. This made me think a lot about how the workflow that I've established for myself can work for collaboration and how hard it is to teach beginners to do the same thing. The reality of working in the modern world is that there's no point in having a very efficient system of authoring documents and websites if it requires technical skills that most people don't have and that take time to learn. Shi was able to pick up Git and Markdown very quickly. It seems as though it was quite intuitive to him. Amanda got frustrated with it a few times and gave up trying to learn. I expect that this is how it would be out in the world, that about half the people you work with will struggle to pick it up. 

When it came time to author the final document for our CPS project, it was clear to me that I should use Microsoft Word so that others could easily collaborate. However, as lead author, producing the first draft was up to me. So I was able to draft all the content in Markdown[^sibanetics] before using Pandoc to convert over to Microsoft Word format. I then uploaded the Word document and my other group members collaboratively edited the final version with me. This was also a pretty effective way of styling the document and spell checking. It increasingly makes sense to me to use a tool like Microsoft Word or Google Docs as the final step in my document authoring pipeline. I can quickly compose most of the content in Markdown and then use Pandoc to convert it for collaborative editing in a format that's common and easy to use for most people. 

Notably, I had a positive experience of using my Markdown skills to help out my girlfriend in preparation of a proposal document for her PhD project. She had authored a fairly large academic document in Microsoft Word and manually written in-text citations and a bibliography. However, there had since been significant edits to the document and the citations and bibliography were out of sync. Using my Markdown skills, I was able to simplify the job of checking the bibliography and the in-text citations against each other. I took a copy of her proposal as a DocX and then converted it to Markdown using Pandoc. I then found a regular expression on the internet (` \(([\w\&\.\s]+,\s\d{4}(;\s+[\w\&\.\s]+,\s\d{4})*)\)`) that fairly reliably identifies Harvard-style in-text citations. I modified this regular expression slightly so that it would include context around the citation. I then ran grep over the Markdown and got it to output a list of all the in-text citations in context. Running through this list, she was able to quickly identify citations that had not been included in the bibliography and those in the bibliography that were no longer cited in text. The satisfying thing is that having solved this problem once, I know that I'll be able to solve problems like it very efficiently in the future.

As noted in relation to workflow, Initially I was looking for a software package that was monolithic and could provide the same features as Microsoft Word (plus more) so that I could author documents from start to finish but also publish them as a website or a PDF easily. [Zettlr](https://www.zettlr.com/) comes close to doing this but it is a bit buggy in my experience. Interestingly, I've now changed my philosophy. When I used to write documents in Microsoft Office, I would use all the complex features such as figure captions, internal references and the Zotero plugin for formatting citations. In hidsight this workflow was problematic when it came to collaboration in the exact same way that I've experienced with my Markdown workflow. Most people don't have the Zotero plugin installed and a lot of people don't know how to use internal references and figure captions. I believe that my approach to document authoring has simplified a lot. Now I just manually write the figure captions in Markdown. Ironically, the Word documents that I now produce are actually easier for people to work on and understand than the Word documents that I used to produce when I was a Microsoft Word user.

Though I'm satisfied with my progress towards this goal, I do feel that my skill will continue to evolve and that I will continue to experiment going forward. I have come across an alternative approach called Scholarly Markdown[^scholarlyMD] which I will look into. I have also found a fantastic article[^seminaryMD] that talks about a pretty easy way of implementing academic references that can be translated across Pandoc's different output formats. I've had a first go at implementing that citation system in the production of this website. 

### Objective 3 - Publishing websites

#### March 2024
*Starting out*

This website represents my first serious attempt at publishing a markdown-based website. I feel that it is functional but I haven't even started on trying to design something appealing. Also, as it is, the medium has been limiting me somewhat. I've held back on adding some content because of a feeling that it would be too much hassle to pull off. I haven't been able to do references for this site properly. All the references have had to go on a separate page rather than being placed near where they are on the site. This was mostly due to time constraints but I anticipate referencing to be one of the major challenges in mastering this markdown skill.

#### June 2024
*Some progress*

I'm not as far advanced in this skill as I had hoped to be. In preparing for this assignment, I've managed to apply a different template to my website but I don't feel like I have fine-grained control of the features of the website or the rendering of the content. I don't know why, for example, the navigation bar disappeared from the top ribbon of the website. 

On the good side, I've figured out how to setup a Jekyll development environment in the Debian container on my Chromebook. This allows me to see how any changes that I make will be seen in the final website immediately. It will also allow me to quickly prototype alternative structures for the site.

![The develpment folder on my chromebook](/src/development-environment.png)

One challenge in applying the templates was that github pages can't deploy most templates automatically. It should've been obvious but it took me running into that wall to realise that Jekyll, when run on my local machine, generates a folder `_site` that holds the html CSS and javascript generated from the template and the markdown. So, for the next checkpoint, I should be able to use my local development environment to generate quite a complex  site and then manually upload it to a static site host. This is important because I feel that this template is over-full with content now that it includes two checkpoint. 

#### November 2024

*Good progress*

I did not have very much time to experiment further with Jekyll publishing during the second semester. I did have a go at changing the theme of this website while I was editing it ([code is commited here](https://github.com/bill-mca/bill-mca.github.io/tree/theme-change). I succeeded in previewing several different themes but I decided that the theme that I used in June was the most practical of all the themes that I have tried. If I had more time, I would like to add a navigation bar to make long pages easier to navigate. I did manage to set up internal links so that the summary of my progress links to specific sections where readers can get more detail about my progress. There are some aspects of this site that are clunky. The way that I reference and hyperlink things is pretty inconsistent. These are mostly teething problems that reulted from me building this website as a beginner. I believe that the next website that I build with Jekyll will actually be quite sleek.

Though I didn't manage to customise a template during semester 2, I feel that I got pretty close to accomplishing everything that I wanted to with my markdown website skill and I do feel confident that I'll now be able to use markdown to publish my own blog. 

## Final Reflections

I feel that I've advanced a long way in this skill and I'm also glad that I picked it as one of the skills for my build journey. I'm going to continue to develop this skill over the coming years and to convert more of my workflows into markdown. 

Though I've historically been a skeptic of the concept of a [zettelklaassen](https://zettelkasten.de/overview/), I think I will build a library of my writings in markdown. Doing so should allow me to maintain git versioning of every single document that I've written and to quickly remix content and output it into different formats. I've also read a lot about people establishing [personal language models](https://www.reddit.com/r/LocalLLaMA/) and I believe that this library of my writings assembled in a machine-readable format would enable me to build a pretty powerful PLM. 

I feel that the website publishing part of the skill has got to the point where it should be fairly low fuss for me to write a blog now, so after this program is finished as I am establishing a library of my writings I'll start to publish snippets of them as a personal blog using the skills that I've developed. 

I already see [my Github page](https://github.com/bill-mca) as an intellectual asset that has helped to advance my career and I believe that gradually building up a blog would help me to communicate about who I am and what my goals and professional interests are. I've found that linking people to my Github page is a very quick way of proving my competency as a programmer. Similarly, being able to link people to my blog should quickly demonstrate my capabilities as a writer and my sustained interest in certain topics.

Finally, developing my markdown publishing skill has also given me insights about other technological skills in general. Reflecting on workflows, I noted that, through markdown publishing, I have been practicing the Unix philosophy. I believe that putting a philosophy into practice is how we shift our paradigms and also that having experienced multiple different paradigms, and being able to move between them, is one of the most powerful skills a person can have.

## References

[^sibanetics]: McAlister, Bill, Shi Pui Ng, and Amanda Topaz. *Bill-Mca/SIBAnetics*, 2024. <https://github.com/bill-mca/SIBAnetics>.

[^buildskills]:  McAlister, Bill. *Bill-Mca/CYBN8001-Build-Skills*, 2024 <https://github.com/bill-mca/CYBN8001-Build-Skills>. 

[^scholarlyMD]: Lin, Tim. "Scholarly Markdown." Scholarly Markdown, n.d. <http://scholarlymarkdown.com/>.

[^seminaryMD]: Krycho, Chris. "Academic Markdown." *Medium* (blog), July 28, 2015. <https://medium.com/@chriskrycho/academic-markdown-and-citations-fe562ff443df>.
