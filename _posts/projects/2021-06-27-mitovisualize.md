---
layout: post
title:  "MitoVisualize"
description: "A web interface that aggregates and displays data on mitochondrial DNA, and allows for searches and interactive visualizations. Built with React, Node.js, Express, and ElasticSearch."
duration: "March 2020 - March 2021"
categories: projects
tag: projects
---

Designed and built by the Lek Lab at Yale, <a href="https://mitovisualize.org/">MitoVisualize</a> is a web tool that aggregates information on mitochondrial DNA from a range of genetic databases and generates visualizations for genes and variants of interest. It provides a useful tool for the interpretation of mtDNA variants and for exploring mtDNA variation in general. 

I worked on the development of this tool from March 2020 to June 2021, as an extension of my work during the previous summer.

### Functionalities

* Visualization of mRNA- and tRNA-encoding genes.
* Visualization of genetic variants in mitochondrial RNA genes.
* Display of information for variants in mitochondrial RNA genes, such as population frequency, in silico predictions, and reported disease associations.
* Visualization of data across mitochondrial RNA structures, such as to show all positions with disease-associated variants.

### Technical Tools

<img src="/assets/img/mito-visualize-structure.png" alt="mito visualize structure" style="width:500px; display:block; margin-left:auto; margin-right:auto;"/>

* **React** React is a JavaScript library for building interactive user interfaces, and it is what we used on the front end.
* **GraphQL** We used GraphQL as the data query language for our API.
* **ElasticSearch** We used ElasticSearch for building our database.