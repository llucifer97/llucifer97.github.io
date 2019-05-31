---
title: Pre-GSOC period
categories:
- GSOC
- Bodypose
feature_image: "https://picsum.photos/2560/600?image=872"
---
Since the community bonding period came to an end and soon coding period will begin. So I thought of giving an overview of the task performed in past 20-25 days. Well, most of my time went into the environment setup and data collection. For data collection, I had to build web crawlers to scrape the data. Though most of the data is already scraped there are still few resources which are left to be scrapped. Image data collected was then fed to the [Openpose](https://github.com/CMU-Perceptual-Computing-Lab/openpose) library to get the detected key points. I have used the COCO model due to its smaller size and also due to limited computing capabilities. Openpose outputs the list of detected keypoints in the form of JSON/XML file. I have extracted nearly 7000 JSON files(surely there is more to be extracted) which is the starting point of the data science cycle.
Now the most challenging part of the task comes that is data annotation. Surely not having a background in Humanities seems like a pain but my mentors helped me out, given that they themselves were master of this field. The first question which was to be solved was "How many gestures are present?".Obiviously given that 7000(and more) image it was quite expensive to manually hand annotate the images. For finding this, I tried different visualization, Dimension reduction, and clustering methods. Here, the k-means algorithm came to be handy because of its unsupervised approach. Initially, it gave me weird results but after rigorous hyperparameter tuning, it started giving me meaningful clusters(though not enough to train a good model).
For this, I am designing an ipython based data annotator tool which will have GUI interface and help the others in visualizing and annotating data. Along with these, I had to set up my HPC CWRU account which now has been successfully setup.

So to sum up ,
<p> Things done during community Bonding Period:</p>

<ul>
  <li>Collected the data from different websites</li>
  <li>Extracted the keypoints from the images as json output </li>
   <li>Further preprocess the data(JSON files) and tried to get any relevant observation</li>
  <li>Applied clustering algorithms on keypoints to identify the different gestures possibly present in the image</li>
  <li>Setup the environment on local machine and successfully created HPC CWRU account</li>
  <li>Discussed the project plan with the mentors over skype call</li>
</ul>

