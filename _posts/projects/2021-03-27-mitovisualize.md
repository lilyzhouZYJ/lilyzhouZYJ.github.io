---
layout: post
title:  "MitoVisualize"
description: "A web interface that aggregates and displays data on mitochondrial DNA, and allows for searches and interactive visualizations. Built with React, Node.js, Express, and ElasticSearch."
image: "/assets/img/mitovisualize/mitovisualize-logo.jpg"
time: "March 2020 - March 2021"
categories: projects
tag: projects
---

Designed and built by the Lek Lab at Yale, <a href="https://mitovisualize.org/">MitoVisualize</a> is a web tool that aggregates information on mitochondrial DNA from a range of genetic databases and generates visualizations for genes and variants of interest. It provides a useful tool for the interpretation of mtDNA variants and for exploring mtDNA variation in general. 

I worked on the development of this tool from March 2020 to June 2021, as an extension of my work during the previous summer.

<a href="https://github.com/lilyzhouZYJ/mitovisualize"><img src="/assets/icons/github-icon.png" alt="GitHub" style="width:25px; height:25px; vertical-align:top">&ensp;See the Source Code Here</a>

<a href="https://mitovisualize.org/"><img src="/assets/icons/external-link.png" alt="External Link" style="width:25px; height:25px; vertical-align:top">&ensp;See the website here</a>

### Functionalities

* Visualization of mRNA- and tRNA-encoding genes.
* Visualization of genetic variants in mitochondrial RNA genes.
* Display of information for variants in mitochondrial RNA genes, such as population frequency, in silico predictions, and reported disease associations.
* Visualization of data across mitochondrial RNA structures, such as to show all positions with disease-associated variants.

### Technical Tools

<img src="/assets/img/mitovisualize/mito-visualize-structure.png" alt="MitoVisualize Structure" style="width:500px; display:block; margin-left:auto; margin-right:auto;"/>

* **React**: React is a front-end JavaScript library for building interactive user interfaces.
* **Express**: We used the Express module in Node.js to build the backend server.
* **GraphQL**: We used GraphQL as the data query language for our API.
* **ElasticSearch**: We used ElasticSearch to build our database.

### Display

<figure>
    <img src="/assets/img/mitovisualize/homepage.png" alt="Homepage" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 1. Homepage</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/mitovisualize/trna-variant.png" alt="Display tRNA Variant" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 2. Display tRNA Variant</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/mitovisualize/rrna-variant.png" alt="Display rRNA Variant" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 3. Display rRNA Variant</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/mitovisualize/gene-region.png" alt="Display region of deletion" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 4. Display Region of Deletion</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/mitovisualize/gene-image.png" alt="Display gene information" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 5. Display Genetic Information</figcaption>
</figure>