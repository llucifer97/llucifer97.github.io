---
title: Week 1 implementing widgets
categories:
- GSOC
-annotationTool
feature_image: "https://picsum.photos/2560/600?image=872"
---
Well, My first week of Google Summer Of Code has come to an end. So, In my previous post, I had talked about the Annotation Tool and the widgets. Well, that was just an introduction nothing fancy!
This week my focus was much on learning and then implementing the interactive widgets to make it easier for the annotator to retrieve every gesture at once given the file name and the number of valid points you want to have in a pose. It has nothing to do with the database(certainly it will be implemented), it was just the magic of the data structure that I have created.
Talking a bit about the key points, for detecting the Keypoints COCO-18 key points model was used. 
The most challenging part of the gesture detection/pose detection in paintings(that too of Medieval period ) is the poor quality of the image. As I had mentioned in my previous blog I have not yet achieved the appropriate level of filtered data. One of the key problems that arose, with the gesture having 3 to 4 key points out of total 18 key points, as not been detected. It was not a nice idea to just discard those gestures since they still have important information regarding poses which needs to be addressed. So, Firstly I tried my own hack to remove those zeroes[0,0] by replacing the zeroes with the previous coordinate, which looked okay at first but it was not that effective. So, I was stuck, that goes the professionals come to rescue. My mentors suggested me to actually use the standard deviation method to replace zeroes rather by replacing with fake values. Though this week was kinda warmup time, playing around with things and experimenting with my ideas.


Also this weekend we had our meeting, where the major discussion was about the features to be implemented in the annotator tool.
<p>Things to be implemented in Upcoming week:</p>
<ul>
    <li>To design a interactive widget to be able to correct the detected gestures in the image</li>
    <li>To deploy my jupter-notebook using Dash plotly and make it available for everyone to use</li>
    <li>Add the feature to upload the images of there own and run the jupyter notebook to detect and annotate gesture</li>
</ul>


So , this is it. Will keep you posted about my progress. STAY TUNED!
 
