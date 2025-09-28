---
title:  "Note-Taker"
summary: "A minimalistic website for creating, editing, and storing notes. Built with various web-development tools including Node.js, Express, EJS template engine, MongoDB and Mongoose, and Passport for user authentication."
tags: ["project"]
showTags: true
date: 2021-10-04
---

Since my work with MitoVisualize largely focused on the frontend, I wanted to get more practice on the server-side logic and build a more solid understanding of the backend. I decided to start with something simple, building a small website for creating, editing, and storing notes. This was a server-side/Node.js practice project, so I focused on building the backend mechanisms and tried to keep the frontend as simple as possible.

GitHub repo: [lilyzhouZYJ/note-taker](https://github.com/lilyzhouZYJ/note-taker)

### Functionalities

* Creating, editing, and deleting notes.
* Support both public and private notes. A user can view other users' public notes, but not their private ones.
* User authentication using Google.

### Technical Tools

On the back end, I'm using Express to build my server. I'm also using the EJS template engine to render templates that would be sent to the front end. For the database, I'm using MongoDB, and I'm using the mongoose package to help interact with MongoDB. The schema and model for mongoose are built in `./models/note.js`.

### Display

{{< figure src="img/note-taker/home.png" alt="Homepage" caption="Figure 1. Home Page" >}}

{{< figure src="img/note-taker/dashboard.png" alt="Dashboard" caption="Figure 2. Dashboard" >}}

{{< figure src="img/note-taker/public-notes.png" alt="Public Notes" caption="Figure 3. Public Notes" >}}

{{< figure src="img/note-taker/single-note.png" alt="Display Note" caption="Figure 4. Display Note" >}}

{{< figure src="img/note-taker/create-new-note.png" alt="Create New Note" caption="Figure 5. Create New Note" >}}