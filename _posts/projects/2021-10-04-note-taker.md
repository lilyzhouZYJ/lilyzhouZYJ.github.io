---
layout: post
title:  "Note-Taker: Independent Project"
description: "A minimalistic website for creating, editing, and storing notes. Built with various web-development tools including Node.js, Express, EJS template engine, MongoDB and Mongoose, and Passport for user authentication."
image: "/assets/img/note-taker/logo.png"
time: "August - September 2021"
categories: projects
tag: projects
---

Since my work with MitoVisualize largely focused on the frontend, I wanted to get more practice on the server-side logic and build a more solid understanding of the backend. I decided to start with something simple, building a small website for creating, editing, and storing notes. This was a server-side/Node.js practice project, so I focused on building the backend mechanisms and tried to keep the frontend as simple as possible.

<a href="https://github.com/lilyzhouZYJ/note-taker"><img src="/assets/icons/github-icon.png" alt="GitHub" style="width:25px; height:25px; vertical-align:top">&ensp;See the Source Code Here</a>

### Functionalities

* Creating, editing, and deleting notes.
* Support both public and private notes. A user can view other users' public notes, but not their private ones.
* User authentication using Google.

### Technical Tools

On the back end, I'm using Express to build my server. I'm also using the EJS template engine to render templates that would be sent to the front end. For the database, I'm using MongoDB, and I'm using the mongoose package to help interact with MongoDB. The schema and model for mongoose are built in `./models/note.js`.

### Display

<figure>
    <img src="/assets/img/note-taker/home.png" alt="Homepage" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 1. Home Page</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/note-taker/dashboard.png" alt="Display tRNA Variant" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 2. Dashboard</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/note-taker/public-notes.png" alt="Display rRNA Variant" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 3. Public Notes</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/note-taker/single-note.png" alt="Display region of deletion" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 4. Display Note</figcaption>
</figure>
<br/>

<figure>
    <img src="/assets/img/note-taker/create-new-note.png" alt="Display gene information" style="width:100%; display:block; margin-left:auto; margin-right:auto;"/>
    <figcaption>Figure 5. Create New Note</figcaption>
</figure>