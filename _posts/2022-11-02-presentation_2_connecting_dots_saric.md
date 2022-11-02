---
title: "Connecting the Dots in a Topic Model:  A Network Representation of Topics and Periodicals"
author: Sanja Saric
date: 2022-10-27
categories: [Animal, Insect]
tags: [bee]
comments: false
---

## Abstract

The topic modeling analysis results are twofold: a matrix called 'document topics' containing probability measures for each topic in each document, as well as a data frame of topics with their probabilities in the corpus and a predefined number of most frequent tokens per topic ('topic keys'). In DiSpecs, mean values of probability measures were calculated for each periodical. These results were then visualized using heat maps, line diagrams, word clouds, and – what is the focus in this submission -- networks (cf. https://gams.uni-graz.at/archive/objects/o:dispecs.result.tm.fr/methods/sdef:TEI/get?mode=topic-network, https://gams.uni-graz.at/archive/objects/o:dispecs.result.tm.es/methods/sdef:TEI/get?mode=topic-network, and https://gams.uni-graz.at/archive/objects/o:dispecs.result.tm.it/methods/sdef:TEI/get?mode=topic-network). Compared to heat maps, which are commonly used to visualize the probability of topics over analyzed entities (in this case periodicals), it can be argued that networks have the additional potential of representing the closeness between the entities based on topics, the scope of the entities (e. g. the number of periodicals), as well as of the inclusion of further annotated data from the analyzed corpus. This latter-mentioned advantage enabled the visualization of topics in combination with manually assigned keywords from the Spectators digital edition by using pie charts as nodes.
 
The network graphs were created in Gephi V. 0.9.2. The nodes' table includes topic labels, periodical titles, size (for topics: the overall probability over the corpus; for periodicals: the number of issues), and references to pie charts in PNG format for the representation of the periodical nodes, which were previously created using Python. The edges are directed from each topic to each periodical and weighted based on the probability of the topic in the periodical. The applied algorithms were Fruchterman Reingold to untangle the randomly arranged network, Force Atlas 2 to disperse groups, and the Louvain method (Blondel et al. 2008) to calculate the modularity. The nodes were colored based on the calculated modularity. The graph was eventually included on a web page next to the pie chart legends (in the menu section of each network's web page), a list of topics with their probability and keywords, and result files from the topic modeling analysis.
     
This allows the researchers to observe the closeness of periodicals by the probability size of the topics identified in the corpus. The French network shows for instance, that all three periodicals edited by Jean-François de Bastide form a cluster around topic 21 (assigned to the discourse field of love), as well as topic 6 (filled with terms of narrative vocabulary and pointing to a story-telling writing style). The results were evaluated by Romance Studies experts who reported that the network visualizations were insightful and compelling because of their ability to demonstrate otherwise invisible relations. These insights enabled a new perspective on the texts by helping the researchers to question their hypotheses and overcome habitual thinking patterns. However, our experience shows that the complexity of network visualizations is a challenge for researchers unfamiliar with this method since the results require a lot of time and research on how to interpret them.
 
By presenting this work at the "Workshop on Information Visualization in the (Digital) Humanities", I hope for an exchange of thoughts on the application of networks in combination with topic modeling and on further improvements necessary to make these highly informative visualizations better comprehensible for the non-digital research community.    

## Slides

PDF

{% pdf "slides/slides_presentation_2.pdf" %}

Powerpoint

{% pdf "slides/slides_presentation_2.ppt" %}

