---
title: "Towards a Global History of the International Institute of Intellectual Cooperation: Challenges and Opportunities" 
date: 2022-10-28
author: Rubén Rodríguez Casañ, Elisabet Carbó Catalan
tags: [bee]
comments: false
---

**Rubén Rodríguez Casañ, Elisabet Carbó Catalan and Diana Roig-Sanz**

# Abstract 

The International Institute of Intellectual Cooperation (IIIC, 1926-1946) was created under the auspices of the League of Nations to coordinate cultural and scientific relations in the interest of world peace, with the work in the domain of intellectual cooperation having brought together leading intellectuals such as Marie Curie, Paul Valéry and Henri Bergson. Although the IIIC's activity came to a standstill during the Second World War, it laid the foundations for the birth of UNESCO (Renoliet 1999).

In this paper we seek to present a visualization created with correspondence contained in the IIIC’s archive, which also contains documents and publications. The latter is today hosted by UNESCO (Paris), it has been partially digitized and is accessible online. The authors are currently exploring its analysis to try and reconstruct a global history of intellectual cooperation that i) measures the involvement of variegated countries and actors in different intellectual activities (literature, translation, arts, etc.), ii) empirically tests the common assumption of creative centers and imitative peripheries, and iii) unearthes the role of figures overshadowed by the presence of renowned celebrities, such as Marie Curie and Albert Einstein. To do so, we have applied Named Entity Recognition (NER) techniques to the IIIC’s correspondence, combined with methods of data science and network science, to reconstruct a co-occurrence network of cities and states on the one hand, and a network of personalities on the other hand.

In this contribution we will discuss a map that represents one example of what we would call "the geographies of intellectual cooperation", that is, a visualization representing the cities mentioned in said correspondence (nodes) and co-occurrences of pairs of cities in the letters (edges). To elaborate this visualization, there has been first a stage of preprocessing, that included: i) distinction between empty pages and written pages (an issue arising from the way correspondence has been digitized); ii) a division of the corpus between manuscript and machine-written letters by using deep learning models, a necessary step given the uneven quality results of OCR. The resulting 65.303 files were ocerised with Google Vision’s API; iii) the identification of letters (in opposition to attached documents) by using NLP (models Random Forest and Support Vector Machine), which provided a result of 19.385 letters with a 96.7% precision. Once we had our final dataset, we combined two NER entity recognition python libraries (Stanza and Spacy), along with lists of city and country names in different languages, to identify a total of 620 cities.

In order to analyse the resulting data, we have used metrics such as modularity, weighted degree centrality, betweenness centrality, degree z within the group, and the participation coefficient P. Through these values calculated in the z-P space, we have associated with each city a role within correspondence networks (Guimerà & Nunes Amaral 2005). Thus, we can identify ultra-peripheral nodes, peripheral nodes, non-hub connector nodes, non-hub kinless nodes and kinless hubs.

The visualization illustrates which zones in the world were more active in the network of intellectual cooperation, with the low interactions with Africa and Asia confirming the alleged eurocentrism of the IIIC. We have been able to observe that the greatest activity took place in European cities, particularly Paris and, to a second level, Geneva, which confirms previously existing knowledge. On the other hand, however, other cities stand out, such as Caracas and Bogotá, given their role as a bridge between European cities and cities in South America.

Several challenges have remained unsolved. The first group is related to the format of digitized archive material (creating PDF that correspond to folders, not to single documents), which makes it difficult for us to delimitate a letter within a PDF. The time-consuming nature of preprocessing tasks, coupled with the challenges derived from the coexistence of hand-written and machine-written letters, as well as the presence of multilingualism in said archive, compelled us to reduce our dataset and limit our analysis to folders A (general affairs) and F (artistic and literary relations). Another group of challenges have to do with results interpretation. The conclusions that can be drawn from a visualization of city mentions partially differ if we employ other geographic visualizations (for example, a visualization of mentions of states, or a visualization of states inferred from city mentions). Although
there are common elements between the possible maps, the fact that there are also differences problematizes the supposed transparency or self-explanatory character of the visualization per se and invites us to analyze the different visualizations both in isolation and in comparison with the others.

# Slides

# Resources
