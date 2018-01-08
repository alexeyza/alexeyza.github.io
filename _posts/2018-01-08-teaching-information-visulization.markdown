---
layout: post
title: "Teaching Information Visualization"
date: 2018-01-08 10:44:18 -0700
comments: true
published: true
categories: ['Information Visualization', Teaching, Data]
image: /assets/article_images/2018-01-08-teaching-information-visulization/background.jpg
image2: /assets/article_images/2018-01-08-teaching-information-visulization/background_mobile.jpg
---

I see information visualization as one of the most interesting and important areas, particularly for researchers or for anyone who works with data. From cases like [Charles Minard's](https://en.wikipedia.org/wiki/Charles_Joseph_Minard) map of Napoleon's campaign of 1812, and [John Snow's cholera outbreak  map](https://en.wikipedia.org/wiki/1854_Broad_Street_cholera_outbreak) of London 1854, we can see examples how visual articulation of data can impact the world. If I were to teach an InfoVis course, I would use the following material and tools.

<!--more-->

## Books

I can't think of a specific book that can serve as the course textbook. Hence, I'm recommending multiple sources of material.

![Charles Minard's map of Napoleon's disastrous Russian campaign of 1812. The graphic is notable for its representation in two dimensions of six types of data: the number of Napoleon's troops; distance; temperature; the latitude and longitude; direction of travel; and location relative to specific dates.](/assets/article_images/2018-01-08-teaching-information-visulization/minard_lg.gif "Minard's map of Napoleon's Russian campaign of 1812")

A book that's worth covering is Edward Tufte's ["The Visual Display of Quantitative Information"](https://www.edwardtufte.com/tufte/books_vdqi) book. It focuses on comprehensible and usable design, concisely and clearly articulating core principles. It includes many good examples.

Tamara Munzner's book, ["Visualization Analysis and Design"](http://www.cs.ubc.ca/~tmm/vadbook/), does a great job in providing and framing the proper terminology for learning about and discussing InfoVis topics (Figure 2.1 of the book shows a summary of this framework). While, Tamara's book would work great as a reference book, I don't think it should be used as the main textbook.

Additional material that may be worth covering or providing as recommended reading: ["Envisioning Information"](https://www.edwardtufte.com/tufte/books_ei) by Edward Tufte, ["Visual Thinking for Design"](https://www.amazon.com/Visual-Thinking-Design-Colin-Ware/dp/0123708966) by Colin Ware, and ["The Functional Art"](http://www.thefunctionalart.com/) by Alberto Cairo.  
For aspects of interaction, the paper ["Toward a Deeper Understanding of the Role of Interaction in Information Visualization"](https://dl.acm.org/citation.cfm?id=1313151) may serve as a helpful starting point (by Yi _et al._ 2007).

Additionally, I suggest reading the interesting [story of William Playfair](https://www.atlasobscura.com/articles/the-scottish-scoundrel-who-changed-how-we-see-data), the inventor of the pie chart, the bar graph, and the line graph. [Eugene Wei's depiction of his job at Amazon](http://www.eugenewei.com/blog/2017/11/13/remove-the-legend) as the first analyst in the strategic planning department is also worth reading.

![A line graph showing England and Scandinavia's import-export balance for the 18th century, from William Playfair's 1786’s Political and Commercial Atlas.](/assets/article_images/2018-01-08-teaching-information-visulization/1024px-Playfair_TimeSeries-2.png "Playfair's line graph from 1786")

For some modern examples, the ["Information is Beautiful" Awards](https://www.informationisbeautifulawards.com/showcase?award=2017&type=awards) website showcases interesting award winning examples. These projects were awarded for excellence and beauty in data visualizations.


## Software and Tools

These are commonly used tools that I find useful:

- Visualizations with R and [R Studio](https://www.rstudio.com/products/rstudio/download/#download) (and packages like [ggplot2](http://ggplot2.org/))
- [D3.js library](https://d3js.org/) and the ["D3.js in Action" book](https://medium.com/@Elijah_Meeks/d3-js-in-action-second-edition-8cf7ffa2a116): D3 is a great JS library for creating visualizations. It's commonly used and is very customizable
- Tableau or [Tableau Public](https://public.tableau.com/s/)


## Inspirational People in the Field

[Giorgia Lupi](http://giorgialupi.com/) is an award winning information designer. I find her work to be inspirational and superb. I suggest watching her [TED talk](https://www.ted.com/talks/giorgia_lupi_how_we_can_find_ourselves_in_data).

![A postcard from the Dear Data project, a year-long, analog data drawing project by Giorgia Lupi and Stefanie Posavec.](/assets/article_images/2018-01-08-teaching-information-visulization/giorgia_lupi.jpg "A postcard from the Dear Data project by Giorgia Lupi and Stefanie Posavec")

---

I'd love to add additional material that can be of help to others. If you've taught or taken an InfoVis course---what material did **you** use or have found useful?    

**P.S.** [I'd love to meet you on Twitter.](https://twitter.com/alexeyzagalsky)