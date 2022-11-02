---
title: Visualising Translation Flows in Ibero-American Literary Magazines 
date: 2022-10-28
author: Ventsislav Ikoff
categories: [Animal, Insect]
tags: [translation studies]
comments: false
---

**Ventsislav Ikoff (1), Alessio Cardillo (1), Laura Fólica (1), and Diana Roig Sanz (2),(1)**

1 Internet Interdisciplinary Institute (IN3) – Universitat Oberta de Catalunya – Barcelona, Spain\
2 Catalan Institution for Research and Advanced Studies (ICREA) – Barcelona, Spain

# Abstract 

Within the scope of the ERC project “Social Networks of the Past. Mapping Hispanic and Lusophone Literary Modernity”, the purpose of this work is to study literary translation within periodicals published in Ibero-America during the first half of the XXth century. We focus on the heterogeneity of the authors, literatures and languages that were translated, in order to explore how foreign literature circulated during the modernism and avant-garde periods. In fact, literary translation in Ibero-American periodicals was one way of internationalisation of the Ibero-American cultures (Roig-Sanz and Fólica, 2021).

To address this question, we propose a sort of a “composite visualisation” (Javed and Elmqvist, 2012), comprising a geographical visualisation (a map) and a nested Sankey diagram, both representing the same data.

Concerning our dataset, we consider the set of contributions we identified as ‘translations’ published in a collection of 9 well-known Ibero-American literary magazines between 1909 and 1949. Our research group manually curates and maintains these data. Within the metadata for each contribution, we focus on the author’s country of origin or nationality, the place where the magazine was published, and the original language, where this information is available.

From these records, we compute the amount of contributions written originally in language i, published by magazine j, by authors with nationality k, w(i,j,k). Then, we use the software Gephi  (Bastian M., Heymann S. and Jacomy M., 2009) to visualise the relationships between languages, magazines, and the authors’ country of origin as a weighted network embedded into space (Latora 2017). Using the network representation, the data is presented as a set of elements (nodes) and relationships among them (edges). In our case, the nodes are either the author’s countries of origin or the journals. The edges, instead, denote the presence of contributions written by authors of a certain country in a given journal. We add further information about the original languages of all contributions written by authors from a certain country in a given journal by encoding it through the colour of the edge. Finally, we account for the number of contributions existing between two nodes by changing the thickness of the corresponding edge.

After setting our visual encoders, we use one of the layout algorithms available in Gephi to generate a world’s map and plot the nodes on it according to their coordinates.
Most of the diagram’s visual aspects were handled directly in Gephi and the final visualisation was then exported as an SVG format. Nonetheless, some minor adjustments –like positioning the labels or creating a legend– were handled through the vector-graphics editor Inkscape.

Eyeballing the resulting network, we can observe the translation flows, especially those existing between Europe, Russia, and South America. Another distinguishable flow is that existing between the United States and one between Europe and South America. The map allows to easily identify the predominance of European-origin authors and to establish the principal languages in translation or relations between journals and authors’ countries of origin or nationality. While lacking great precision or detail, the diagram allows us to understand in a simple, intuitive manner the geography of literary circulation in Spanish and Latin American cultural periodicals during the first half of the XXth century.

Despite being very intuitive, the network representation has some shortcomings. For instance, the spatial proximity between neighbouring countries gives rise to an overlap between nodes, edges and labels (especially those located in Europe) and imposes a limitation as to what information can be displayed. For instance, the node sizes, while designed to represent the number of translations from a given country, cannot differ too much in size –or risk making sections of the map unreadable– and therefore become unsuitable to draw visual comparisons between most countries. Similarly, although some edges are quite thick and well distinguishable, indicating a greater number of interactions between a given journal and country, many others are very thin; this makes them difficult to spot and renders their color discrimination harder.

These (and other) biases can impair our ability to extract useful, non trivial, information from the data. To overcome this problem, we nest into the map an inset that displays the same information encoded via a so-called Sankey diagram (Wilke, 2019). Specifically, we represent magazines, languages, and countries as boxes (each type aligned vertically together) and a line connecting magazine i and language j denotes the number of contributions w(i,j) with those characteristics (similarly, one can define w(j,k) to count the number of contributions with language j written by authors of country k). The height of a box denotes the number of contributions for that node with respect to the total.

Sankey diagrams highlight natively the most important flows between distinct groups of categories, and therefore are well suited to represent associations among data possessing two or more quantitative variables. We created our Sankey diagram using the native implementation available in the Python graphing library Plotly.

The resulting Sankey diagram allows to visually explore the flows between countries, languages and journals, and also to compare the items within each category. The visual inspection of the Sankey diagram highlights, for instance, the prominent role played by French and English contributions together with that played by contributions written originally in Italian, German, and Russian and how these languages map into countries of origin. Besides, we note the important presence of a box at the bottom named “Unknown”, corresponding to those contributions for which the information on the original language is missing. This group is made of authors of several nationalities and highlights the key role of meta information on the identification of contributions as translations. Nonetheless, this group can hardly be identified on the map as there it is scattered among flows from different countries.

In summary, the composite visualisation offers a more nuanced answer to the research question about the circulation of translated literature in Ibero-American periodicals. The two elements of the visualisation reveal different information from the same underlying data. Combined in a composite visualisation, they complement each other and mitigate their shortcomings.


# Slides

{% pdf "https://raw.githubusercontent.com/chpollin/InfoVisDHGraz/5fd88139ff2f86b254e152dadfe7719d2c53403c/slides/slides_presentation_6_ikoff.pptx" no_link %}

# Resources