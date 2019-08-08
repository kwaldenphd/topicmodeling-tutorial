# Introduction to Topic Modeling

This tutorial was written by <a href="https://www.grinnell.edu/users/waldenka">Katherine Walden</a>, Digital Liberal Arts Specialist at Grinnell College.

This tutorial was reviewed by <a href="https://www.grinnell.edu/users/purcelsj">Sarah Purcell</a> (L.F. Parker Professor of History) and <a href="https://www.grinnell.edu/users/donovang">Gina Donovan</a> (Instructional Technologist) at Grinnell College, and edited by Papa Ampim-Darko, a student research assistant at Grinnell College.

This tutorial is adapted from the Programming Historian’s <a href="https://programminghistorian.org/en/lessons/topic-modeling-and-mallet">Topic Modeling and MALLET tutorial</a>.

<a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license"><img style="border-width: 0;" src="https://i.creativecommons.org/l/by-nc/4.0/88x31.png" alt="Creative Commons License" /></a>
Introduction to Topic Modeling is licensed under a <a href="http://creativecommons.org/licenses/by-nc/4.0/" rel="license">Creative Commons Attribution-NonCommercial 4.0 International License</a>.

<hr />

As the authors in <em>Exploring Big Historical Data </em>point out, “Keywords have their limitations, in that they require us to know what to search for” (113). As an alternative, topic modeling builds a list of significant terms by calculating what terms, phrases, clusters, etc. are significant or occur frequently within a text.

In this tutorial, we will introduce topic modeling using digital tools that represent the types of technical interfaces historical scholars use in their research. Across these digital tools, we will be using the process Underwood describes for topic modeling:
<blockquote>“You assign words to topics randomly and then just keep improving the model, to make your guess more internally consistent, until the model reaches an equilibrium that is as consistent as the collection allows” (Underwood, quoted on page 119)
<em>Exploring Big Historical Data</em>: Chapter 4</blockquote>

<hr />

# GUI Topic Modeling Tool (GTMT)

As we’ll explore later in this tutorial, the more robust topic modeling tools can sometimes have a steep technical learning curve. The <a href="https://github.com/senderle/topic-modeling-tool">Topic Modeling Tool</a> in a Google Code repository provides a graphical user interface for preliminary topic modeling. The project was created in 2011 through a Institute of Museum and Library Services grant and was developed by Yale University, the University of Michigan, and the University of California, Irvine. The GUI Topic Modeling Tool is built on the <a href="http://mallet.cs.umass.edu/">MALLET toolkit</a>.

<hr />

## Getting Data

Download the "Topic_Modeling_Corpus" compressed zip folder in this Repo to your Desktop. Extract the folder contents.

## Launching GTMT

To use it on your own computer, go to the <a href="https://github.com/senderle/topic-modeling-tool">GitHub page</a>, download the Mac or Windows version, and follow the installation instructions.

<p align="center"><a href="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_GTMT.PNG"><img class="aligncenter size-full wp-image-616" src="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_GTMT.PNG" alt="" width="852" height="322" /></a></p>

Navigate to <strong>C:\Program Files (x86)\TopicModelingTool\app</strong> in File Explorer, and double click on the <strong>TopicModelingTool-jfx</strong> file to launch the program.

<hr />

## Importing and Analyzing Data

<p align="center"><a href="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_1.PNG"><img class="aligncenter size-full wp-image-567" src="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_1.PNG" alt="" width="930" height="575" /></a></p>

1-Click the <strong>Input Dir…</strong> icon and select the folder where the S&amp;B text files are located.

2-Click the <strong>Output Dir…</strong> icon and <strong>create a folder</strong> on the Desktop named <strong>Topic Modeling</strong>. Select this folder as your Output Directory.

3-Click the <strong>Learn Topics</strong> icon to topic model the source text.

<p align="center"><a href="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_2.PNG"><img class="aligncenter size-full wp-image-568" src="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_2.PNG" alt="" width="932" height="576" /></a></p>

4-What you see happening in the Console is the back-end work the MALLET tool does to generate the topic models.

5-Once modeling is complete, the locations for output files is the folder you selected as Output Dir… The full file path for the output files is listed under <strong>**Generating Output**</strong> in the Console.

<hr />

## Exploring Results

<p align="center"><a href="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_3.PNG"><img class="aligncenter size-full wp-image-569" src="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_3.PNG" alt="" width="742" height="313" /></a></p>

6-Open <strong>File Explorer</strong> and navigate to the folder you selected as the <strong>Output Directory</strong>. In that folder, you have the results of your topic modeling as <strong>CSV and HTML files</strong>.

7-Click on the <strong>output_html folder</strong>.

8-The <strong>Docs folder</strong> contains an HTML file with topic modeling for each individual document contained in the <strong>Input Directory folder</strong>. <strong>All_topics</strong> is an HTML file that provides the list of topics. The <strong>Topics folder</strong> contains an HTML file that lists how many times a specific topic appears in each document.

<p align="center"><a href="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_4.PNG"><img class="aligncenter size-full wp-image-570" src="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_4.PNG" alt="" width="973" height="341" /></a></p>

9-Open the <strong>all_topics HTML file</strong>.

10-Based on your existing knowledge of the source text, how accurate or expected/believable are these topics? What terms or topics surprise you? What terms or topics are absent that you think might be significant?

<p align="center"><a href="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_5.PNG"><img class="aligncenter size-large wp-image-571" src="https://raw.githubusercontent.com/kwaldenphd/topicmodeling-tutorial/master/screenshots/Capture_5.PNG" alt="" width="676" height="496" /></a></p>

11-Open the <strong>output_html folder</strong> and open the HTML file for a specific topic.

12-Based on your knowledge of the source text, are you surprised by the distribution of this topic or how frequently it appears in specific texts? What questions do you have about the results for this topic?

13-Open the <strong>output_csv folder</strong>. The <strong>topics-words CSV</strong> includes the list of topics generated from the GTMT.

14-The <strong>topics-in-docs CSV file</strong> is organized by document and lists the topics that appear in each document. The <strong>docs-in-topics CSV file</strong> is organized by topic and lists the documents that include each topic.

15-<strong>Open both CSV files</strong>. How does the organization of information compare across the two table structures? How is the presentation of information in the CSV files different than your experience with the HTML files? What questions do you have about the information contained in the CSV files?

16-How useful did you find the GTMT for enriching your understanding of the text?

<hr />

# Additional Exploration

<ul>
 	<li>Change the number of topics generated by the GTMT and compare results. How did changing the number of topics change the topic modeling structure?</li>
 	<li>Click on the Optional Settings icon to see additional customization options for the GTMT, like adding a list of stopwords and changing the number of topic words to print.</li>
</ul>

<hr />

# Topic Modeling in Historical Research

In our tutorials on mapping and spatial analysis, we looked at Cameron Blevins’s historical research that uses U.S. postal service data. In another research project, Blevins uses topic modeling to better understand <a href="http://dohistory.org/diary/index.html">27 years of diaries</a> written by 18<sup>th</sup> century New England midwife Martha Ballard.

Visit Blevins’s personal site and read his blog post titled “<a href="http://www.cameronblevins.org/posts/topic-modeling-martha-ballards-diary/">Topic Modeling Martha Ballard’s Diary</a>.”

<hr />

# Reflection questions:
<ul>
 	<li>Why does Blevins see topic modeling as a useful research methodology for analyzing Ballard’s diaries?</li>
 	<li>What does Blevins have to say about the results MALLET generated?</li>
 	<li>How does Blevins connect MALLET’s calculations to an argument about the historical meaning and significant themes in Ballard’s diaries?</li>
 	<li>Based on your own experience and Blevins’s project, in what ways do you see topic modeling as a useful digital approach for historians?</li>
 	<li>What types of historical research questions might topic modeling help researchers address?</li>
 	<li>What types of data or research questions might not be a good fit for topic modeling? And why?</li>
</ul>
