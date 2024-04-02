![](src/cybernetic-stream-table.png)
# Introduction
I'm undertaking the Master of Applied Cybernetics at ANU and this website has been created to document my learning as I progress towards Building cyber-physical inventions alone or in interdisciplinary teams. The first invention, that I have undertaken to build alone, is called the cybernetic stream table and you'll read many references to it throughout this site.   

## Skill choices

Please choose from the list below to learn about my journey developing the skills of a cybernetician:

1. [Markdown publishing](markdown-publishing)
2. [Systems thinking](systems-thinking)
3. [Computer vision](computer-vision)
4. [Purposeful interdisciplinary collaboration](purposeful-interdisciplinary-collaboration)

![](src/investigating-table.jpg)

This is a Jekyll website created with markdown. 

# Markdown publishing
Markdown is a writing format for text files that can be automatically converted to many other formats. I got interested in learning markdown when I learnt about GitHub pages. This service allows you to generate whole websites from your uploaded markdown. Markdown can also be transformed into PDFs and Word documents. Drafting documents in markdown leaves you open to later publish in any format or several at once.

Part of the appeal of using markdown to author content is that it is straight-forward to write scripts that query and edit it.  At a later date, if I decide a that I want to re-publish this website as a PDF, I might need to change the format of the references. Because it is markdown, I'll be able to write simple code to process the raw md files and make the necessary changes to the reference format. I can also throw all the markdown that I have ever written into a big folder and then use tools like grep to find all mentions, for example, of the term 'systems thinking'. Markdown can also be integrated with GNU transparency tools such as git and make. This way, the full process of authoring the document is open for anyone to see or replicate. I think this creates fascinating data especially for documents that are be maintained over a long time or remixed. In sum, I think markdown is the best way of encoding text for future knowledge systems and that learning to do it well will open up possibilities for me and just generally make the world a better place. 
 
## Objectives
1. Identify software and establish workflows for doing as much of my writing as possible in markdown and versioning it with Git.
3.  Author large documents in markdown including academic citations, footnotes, internal references, figure captions etc. 
4. Be able to apply and customise Jekyll templates to design markdown based websites.

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
I'd never used pandoc before and I'd always used Microsoft Word to author documents. Apart from some brief attempts at writing HTML, I've only ever used integrated content management systems to publish websites. I did have a go at using Jekyll once but didn't get very far. The presentation of this webpage represents the limits of my Jekyll capabilities.

## Progress

### Objective 1 - Workflow
**Significant progress**
I've done a lot of writing in markdown since starting this course including [two skills work assessments](https://github.com/bill-mca/CYBN8001-Build-Skills/) and [this webpage](https://github.com/bill-mca/bill-mca.github.io)! I've experimented with a few markdown editors and decided that it doesn't really matter that much which one you use because markdown is so simplistic. My biggest success has been demystifying git by learning to use [Gitfiend](https://gitfiend.com/). I'm not comfortable that this objective has been reached. Once I've authored a large documents I'l feel confident in the workflow I've established.

### Objective 2 - Publishing documents
**Some progress amid frustrations.**
I have made PDF versions of my two skills work assignments but the process was not smooth for either of them. For skills work assignment 2 I ended up having to make the PDF via some edits on a docx version because I couldn't debug the pandoc errors in time for submission!

![My current setup of pandoc crashes anytime the markdown file includes an emoji.](src/no-emojis-allowed.png)

I've had frustrating errors thrown at me by pandoc. Here's a list of the issues I encountered while trying to PDF Build Skills 2: 
1. The default margins are much too big
2. Some of the figures are given captions but some are not
3. Some of the ordered lists are not recognized as such and so drawn as big ugly blocks of text
4. some hashes (##) were randomly inserted in the document
5. Heading sizes are hard to tell apart and the navigation pane of the PDF reader didn't show the expected hierarchy

![Pandoc's default PDF has enormous margins and it didn't recognise my list for some reason.](src/ugly-squashed-list.png)

I've struggled with adding references to markdown docs and had to use a workaround where zotero outputs an HTML bibliography that I have to process with pandoc before manually appending to the markdown document.

So far, I would've been better off using familiar tools such as Microsoft Word to do these assignments. The effort involved in proofing and debugging the pandoc outputs has been substantial. nevertheless, I'm hopeful that, as my markdown familiarity and my authoring workflows improve, the whole process will get a lot smoother and I'll have a powerful new tool for publishing my work across formats. 

### Objective 3 - Publishing websites
**Starting out.**
This website represents my first serous attempt at publishing a markdown-based website. I feel that it is functional but I haven't even started on trying to design something appealing. Also, as it is the medium has been limiting me somewhat. I've held back on adding some content because of a feeling that it would be too much hassle to pull off. hopefully chipping away at this over the next couple of months will  

I haven't been able to do references for this site properly. All the references have had to go on a separate page rather than being placed near where they are on the site. This was mostly due to time constraints but I anticipate referencing to be one of the major challenges in mastering this markdown skill.

# Systems thinking
## Objectives 
1. Apply systems thinking to the design of CPS
2. Effectively communicate about systems with diverse audiences
3. Use CPS as boundary objects to facilitate constructive discussion about the future of environmental systems

## Prior knowledge 
My background is in natural resource management. Systems thinking is widely recognized as an important part of natural resource management (NRM) however, it is rarely delineated to which issues the systems lens must be applied. Moreover, despite my 5 years experience working in NRM, I couldn't say with confidence exactly what systems thinking was. I believe that, like most NRM practitioners, I was developing a ad-hoc systems thinking skill set 

In preparation for this course I read *Systems Thinking - A Primer* by Donella Meadows (2008).

## Progress
### Objective 1 - Systems thinking for design
**Some progress**
As part of my preparation for the resource facilitation assignment, I read the paper *Designerly Ways of Knowing: What Does Design Have to Offer?* (Hocking 2010) from the book Tackling Wicked Problems (Harris *et al.* 2010). Earlier, I had written a note about my goals for the build journey and, under the heading 'Systems analysis' I'd stated that my goal was "Properly describing systems and identifying where the leverage points are so that my work is purposeful and strategic". I've changed the boundary that I put around this skill and now see it as a way of relating and effecting change in the world as shown by my changed objectives as stated above. My theory of change has shifted to be more about the conversations that the CPS will provoke rather than building a CPS that will change the world. 

Below is an image that I presented as part of the maker project pitch assignment. It shows my conceptualisation of a stream table as an information system with feedbacks. It also shows how I intend to augment that system by adding an extra feedback loop so that the state of the table influences the flow rate of water. On the day I tried to explain (see below) that the extra layers of feedback make the cybernetic stream table a better model of human interaction with the environment than a conventional stream table.

![A model of information flows in a cybernetic stream table, how could this model be improved?](src/cst-feedback-diagram.png)

Since presenting the pitch, I've had some thoughts about better ways of conceiving of this model. The feedback, and the nature of the feedback should be more explicitly stated as part of the model. Furthermore, I could draw up a system model of how a river works with human interaction. I could then draw parallels between the structure of the real-life information system and my simulation of it. I'm finding these highly abstract concepts of systems very difficult to grapple with but I'm enjoying the challenge for now.


### Objective 2 - Communicating about systems
**Starting out.**
As part of the pitch of my maker project, I was expected to highlight '...new ideas or thoughts ... relevant to applied cybernetics'.  I tried really hard to get across my ideas about how an extra layer of feedback will change the meaning of the stream table but I felt that I didn't get the message across. I'm looking forward to honing this as the program progresses. I believe that the first demo day will be an excellent opportunity to hone my ability to coherently communicate about systems.

### Objective 3 - Futuring with CPS
**No progress**

# Computer vision
This will be fundamental to the CPS project that I have in mind. In thinking of ideas for my CPS project, I heavily favoured projects that involved computer vision as it is increasingly important to the work I do in environmental science. The drone technology that I am hoping to work on in the future is based on computer vision for two separate applications:
1. Photogrammetry makes mathematical models by comparing many images to each other.
2. Remote sensing categorises image data to draw conclusions about the health of plants or ecosystems. It sometimes draws on hyperspectral data to augment the visible light images.

## Objectives
1. Write some computer vision code to recognise objects in digital photos
2. Understand the diversity of algorithms grouped as machine vision and a bit of an overview of how each works and what it can be used for  
3. Understand the algorithms underpinning drone photogrammetry
4. Develop a new computer vision method that could be applied to my work in natural resource management

## Prior knowledge 
**Very limited.** 

I use Open Drone Map (ODM) to make photogrammetric models from my drone photos. Though ODM draws heavily on python's OpenCV (Open Computer Vision) library. From the logs I've seen that an algorithm called flann is used to detect overlap in photos. I've got ideas aboutt how flann might work but I have never had occasion to get my hands dirty and try to edit or create OpenCV code. As a a scientist, I feel a strong urge to spend some time mucking around using flann to understand its limitations. for other aspects of my scientific practice I generally understand how the system works and what its limitations are. I understand my drone's satellite navigation much better than it's computer vision.

## Progress
**No progress against any of the objectives**

I haven't yet got around to opening the documentaion for OpenCV or searching for resources that will help me learn it. The one insight I've had was when Hannah Feldmann linked us to [Teachable Machine](https://teachablemachine.withgoogle.com/). This easy machine learning platform might be useful for realizing my computer vision aspirations. 

# Purposeful interdisciplinary collaboration
I'm not exactly sure how to phrase this one, I'm hoping that I will come up with some better terminology for this as I progress in the course, but I'd like to be purposeful in working on solutions that meet a genuine need. I see this as a skill of interdisciplinary work as a specialist is only meeting a genuine need when their work makes sense in a wider context.

I believe that interdisciplinary collaboration I will try to hone my conceptualisation of this skill before the 2nd check point. As it becomes clearer, it is possible that I will just fold this skill into systems thinking 

## Objectives
1. Apply new tools and strategies developed in the MACYB to interdisciplinary collaboration.
2. Find ways of embeding shared values into decision making about interdisciplinary projects.

## Prior knowledge
In (poorly) defining this desire, I'm drawing on the concepts of holistic grazing management (Savory & Butterfield 1999). Holistic management asks practitioners to carefully define their values and their decision making context before making any decisions about changes to environmental management regimes. One of the main drivers for me deciding to study the MACYB was the realisation of the importance of interdisciplinary work in the field of environmental management.

### Progress
**Still trying to properly conceptualize**

One way of making a start on developing this skill, leveraging the build project, would be to go to the potential end users of the technology that I am developing and then ask them to work with me on it so that what I come out with meets their needs.


