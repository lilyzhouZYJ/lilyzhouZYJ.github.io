---
title: "MitoVisualize"
summary: "A web interface that aggregates and displays data on mitochondrial DNA, and allows for searches and interactive visualizations. Built with React, Node.js, Express, and ElasticSearch."
tags: ["project"]
showTags: true
date: 2021-03-27
---

Designed and built by the Lek Lab at Yale, <a href="https://mitovisualize.org/">MitoVisualize</a> is a web tool that aggregates information on mitochondrial DNA from a range of genetic databases and generates visualizations for genes and variants of interest. It provides a useful tool for the interpretation of mtDNA variants and for exploring mtDNA variation in general. 

I worked on the development of this tool from March 2020 to June 2021, as an extension of my work during the previous summer.

GitHub repo: [lilyzhouZYJ/mitovisualize](https://github.com/lilyzhouZYJ/mitovisualize)

### Functionalities

* Visualization of mRNA- and tRNA-encoding genes.
* Visualization of genetic variants in mitochondrial RNA genes.
* Display of information for variants in mitochondrial RNA genes, such as population frequency, in silico predictions, and reported disease associations.
* Visualization of data across mitochondrial RNA structures, such as to show all positions with disease-associated variants.

### Technical Tools

{{< figure src="img/mitovisualize/mito-visualize-structure.png" alt="MitoVisualize Structure" caption="MitoVisualize Structure" >}}

* **React**: We used React to build the interactive interface.
* **Express**: We used the Express module to build the backend server.
* **GraphQL**: We used GraphQL to build the data query API into the database.
* **ElasticSearch**: We used ElasticSearch to build our database.

### Display

{{< figure src="img/mitovisualize/homepage.png" alt="Homepage" caption="Figure 1. Homepage" >}}

{{< figure src="img/mitovisualize/trna-variant.png" alt="Display tRNA Variant" caption="Figure 2. Display tRNA Variant" >}}

{{< figure src="img/mitovisualize/rrna-variant.png" alt="Display rRNA Variant" caption="Figure 3. Display rRNA Variant" >}}

{{< figure src="img/mitovisualize/gene-region.png" alt="Display Region of Deletion" caption="Figure 4. Display Region of Deletion" >}}

{{< figure src="img/mitovisualize/gene-image.png" alt="Display Gene Information" caption="Figure 5. Display Genetic Information" >}}