# Core standard curriculum (B.E. 2551) interpretation
*Self project for curriculum development, Jan 2020*

Using Natural Language Processing for extracting an information in core curriculum B.E. 2551

**Editor**

Kittapat Ratanaphupha

Note: the analysis is only included the high school courses (M.4-M.6)

## Overall process in this work
For this work can separate a work in to 3 subtasks which are:
1. Convert original PDF file into machine readable file (.txt)
2. Create a simple relational table to seek a hidden information more easily
3. Visualization and summary information in the curriculum

![1](https://github.com/KittapatR/core-standard-curriculum/blob/main/Procedure1.jpg)

![2](https://github.com/KittapatR/core-standard-curriculum/blob/main/Procedure2.jpg)

![3](https://github.com/KittapatR/core-standard-curriculum/blob/main/Procedure3.jpg)

The main problem for Thai passage is about a tokenization which is difficult to find a distinction between words. In the early years of development for NLP in Thailand, there is an exact algorithm called Maximal Matching that is trying to tokenize as a least number of words and each word has fair amount of syllables. (That validating a word by using Thai corpus tries.) But, there are still too many issues for doing tokenization in Thai language. Then, in this project, I will use CNN-based model called "DeepCut" to tokenize a passage. \[ See more at: https://github.com/rkcosmos/deepcut \]

## Visualization
### Word cloud
When I successfully extract data into word frequency table, I use a wordcloud to find some insights. Here is the result for overall subjects:
![WordCloud](https://github.com/KittapatR/core-standard-curriculum/blob/main/word_cloud_all.jpg)

which emphasizes the words that is about students' capability and other main concept of things.

![WordCloud2](https://github.com/KittapatR/core-standard-curriculum/blob/main/word_cloud_each_subject.jpg)

Suppose I do it in more depth, subject level, the results can describe a behavior of a subject that was already defined by curriculum committee.

### Graph network
For this visualization, the graph network drawing is based on force-directed drawing algorithm which mimics from Molecular dynamics that calculating a force for each time intervals. So that means, if a node has more degree, the algorithm will suggest that the node has more centrality also for the case of using barycentric coordinates. The other meanings are shown below:

![GraphViz](https://github.com/KittapatR/core-standard-curriculum/blob/main/Graph%20viz%20description.jpg)
![GraphViz2](https://github.com/KittapatR/core-standard-curriculum/blob/main/Graph%20viz.jpg)

The platform I use for visualizing a graph network called Kumu. It can upload a JSON file which has created by code in previous subtask.

See more at: https://kumu.io/kittapatr/high-school-curriculum#keyword

## Other insights
In curriculum design for Thai school, a curriculum must follow a core curriculum B.E. 2551 legally. Although, there is no restriction that a class cannot be integrated as indisplinary subject. The shared words in each pair of subjects are interesting to gather the idea to design an interdisciplinary course. So, the result I found is shown as below:

![frq](https://github.com/KittapatR/core-standard-curriculum/blob/main/frequecy.jpg)
![frq2](https://github.com/KittapatR/core-standard-curriculum/blob/main/frequency2.jpg)
