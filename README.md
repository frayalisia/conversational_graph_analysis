# Conversational-graph-analysis

###Problem Statement

The purpose of my research is building *weighted undirected conversational network*, where nodes represent characters, and edges signify conversation between them with edge weights corresponding to the length of the dialogues.

###Data

We have chosen the drama **“Blue bird” by M. Meterlink** for analysis. 

*Reasons:*
*	many characters in the text
*	drama text is easy to parse because of its structure
*	all characters are uniquely identified, no need for anaphora resolution and clustering names of the same character
*	don’t need to find instances of quoted speech 
*	author’s remarks help to identify entering\exiting of the character

###Approach

First of all we find “speaking” characters, **our nodes**. They are not just persons from the characters list because ones is not in list, some is not talking and others has different names. 

Then we split the text into acts, as we want to make graphs for every single act in text.
So, we analize one act at the time. Split it into scenes. Then we split it further by the authors comments. We do it because authors remarcs often signify entrence or exit of some characters. So we obtain many chunks of text. We call them *conversations*. They are our **edges**.

Each such conversation adds weight to each edge between the characters participating in it. 
The numerical value of the added **weight** is conversation length divided by the amount of participants. 
Summing the weights over all conversations, we finally obtain the graph. After that we use to **Gephi and networkX** to visualize the result of the research. Then we calculate some statistics.

###Graphs
The edges between the most “communicative” persons are marked in rainbow colors or in bold.

ACT 1
![ACT 1](/pics/0.png)

ACT 2

![ACT 2](/pics/1.png)

ACT 3

![ACT 3](/pics/2.png)

ACT 4

![ACT 4](/pics/3.png)

ACT 5

![ACT 5](/pics/4.png)

ACT 6

![ACT 6](/pics/5.png)
