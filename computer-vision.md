---
layout: page
title: Computer Vision
Author: Bill McAlister
---

Computer vision was an important part of the Cybernetic Stream Table (CST) project. In thinking of ideas for my CPS project, I heavily favoured projects that involved computer vision as it is increasingly important to the work I do in environmental science. The drone technology that I am hoping to work on in the future is based on computer vision for two separate applications:
1. Photogrammetry makes mathematical models by comparing many images to each other.
2. Remote sensing categorises image data to draw conclusions about the health of plants or ecosystems. It sometimes draws on hyperspectral data to augment the visible light images.

## Objectives
1. **Object Recognition** --- Write some computer vision code to recognise objects in digital photos.
2. **Algoritm Choice** --- Understand the diversity of algorithms grouped as machine vision and a bit of an overview of how each works and what it can be used for.  
3. **Algorithm Development** --- Develop a new computer vision method that could be applied to my work in natural resource management.

## Prior knowledge 
*Very limited* 

I use Open Drone Map (ODM) to make photogrammetric models from my drone photos. ODM draws heavily on python's OpenCV (Open Computer Vision) library. From the logs I've seen that an algorithm called FLANN is used to detect overlap in photos. I've got ideas about how FLANN might work but I have never had occasion to get my hands dirty and try to edit or create OpenCV code. As a a scientist, I feel a strong urge to spend some time mucking around using FLANN to understand its limitations. For other aspects of my scientific practice, I generally understand how the system works and what its limitations are. I'd like to understand my drone's computer vision abilities at least as well as I understand its satellite navigation.

## Progress

### Objective 1 --- Object Recognition

#### March 2024
*No progress*

#### June 2024
*Good progress*

I've written my first computer vision algorithm. The Cybernetic Stream Table had the ability to recognise yellow objects that were placed on the surface of the table. I achieved this by elevating a Raspberry Pi up above the table and pointing the Pi's camera down towards the table. I then wrote image recognition code to run on the Raspberry Pi.

![My image recognition code could recognise and count yellow objects](./src/object-recognition.png)

From the outset I knew that it would be best to write a very simple image recognition algorithm. I did some research on the alternatives but decided that, to keep it achievably simple, I would only try to recognise brightly coloured objects. I found the process of writing the code pretty straight forward. I got stuck for a couple of hours trying to define bright yellow in the HSV colour space but, apart from that, the computer vision code took much less time to develop than I had been estimating.

<iframe width="560" height="315" src="https://www.youtube.com/embed/t2YHfOZ1-vY?si=Ju2vy3iAj9-uPXkH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

One interesting learning from developing my own algorithm has been the recognition that most computer vision code runs in `while true` loops. The applications that I have been imagining for computer vision are all one-shot automated analysis but the extant literature is oriented towards sensing the world in real-time. When I started work on the Cybernetic Stream Table I envisaged that the computer vision algorithm would be run once every minute to sense the state of the table and adjust the flow. However, as I learnt about the capabilities of the technology I realised there was no reason not to try to sense and actuate in real time. This, and the fact that even a Raspberry Pi was adequately powerful to do so, has got me thinking about how *real-time* computer vision could be applied in my field.

### Objective 2 --- Algorithm Choice

#### March 2024
*Minimal progress*

I haven't yet got around to opening the documentation for OpenCV or searching for resources that will help me learn it. The one insight I've had was when Hannah Feldmann linked us to [Teachable Machine](https://teachablemachine.withgoogle.com/). This easy machine learning platform might be useful for realizing my computer vision aspirations. 

#### June 2024
*Good progress*

As part of the Cybernetic Stream Table project, I spent some time researching different ways to detect objects in images. I mostly focused on the capabilities of the [OpenCV python library](https://opencv.org/). OpenCV distinguishes between feature detection and object recognition. 

Feature detection is for recognising key-points in an image where there is a lot of contrast between neighbouring cells. Algorithms that automatically align or stitch images, such as photogrammetric algorithms, use feature detection. [The OpenCV documentation](https://docs.opencv.org/3.4/db/d27/tutorial_py_table_of_contents_feature2d.html) lists many feature detection algorithms. Amoung them are the SIFT and SURF algorithms that are familiar to me from my work with Open Drone Map. [The FLANN matcher](https://docs.opencv.org/3.4/d5/d6f/tutorial_feature_flann_matcher.html), with which I was also familiar, uses the key-points identified by SIFT and SURF to align images with each other. 

OpenCV has a range of object identification models that are based on key-point identification much like the above. Identification algorithms work by using many binary classifiers (e.g. faces or no faces present) to identify if a particular type of object is present in the image. Algorithms can be  weak classifiers or strong classifiers. The former make many errors but perform better than random chance. The latter can reliably classify images. [Strong classifiers can be made by the layering of many weak classifiers](https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html). 

Machine learning models are another completely different approach to solving this problem. [Hugging face has a long list](https://huggingface.co/models?pipeline_tag=object-detection&sort=trending) of models that are designed to recognise objects in an image. The vast majority of these models have been trained on everyday objects from the urban and domestic environments but, it seems to me, there is no reason that they couldn't be used to recognise emergent objects in natural environments.

For the Cybernetic Stream Table, I decided to stick to recognising brightly coloured objects as this was the most achievable in the short time frame that I had but the background research before making that decision has given me a fair bit of insight into the application of computer vision. 

### Objective 3 --- Algorithm Development

#### March 2024
*No progress*

#### June 2024
*Minimal progress*

The colour recognition algorithm that I created could be used to meaningfully analyse drone images of rivers if you had a hyperspectral camera. This way it would be possible to quickly classify bare ground, water and different types of vegetation. I've read [a paper](https://www.mdpi.com/2072-4292/13/19/3983) that did just that.  I haven't done any work towards that yet but the computer vision work that I did for the Cybernetic Stream Table project has developed some of the skills that I would need to write such code. 

On demo-day I did a lot of talking about how it would be cool to develop algorithms that recognised geomorphic features in a river. This would be a revolutionary tool for river science but it would be made of much more complicated algorithms than just colour recognition. I think that it would also need a significant machine learning component. 