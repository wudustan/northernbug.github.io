# NorthernBUG

## Website Updates
We encourage community participation in the administration of NorthernBUG 
so please feel free to submit pull requests to add yourself to the members 
page, make a post, add your meeting etc.

Fork this repository to get started:
https://github.com/NorthernBUG/northernbug.github.io.git

### Adding a Post
Add a new markdown file in the `_posts` directory with the filename in the format:

```
YYYY-MM-DD-quick-title.md
```

The 1st few lines of the page should be like this:
```
---
layout: post
author: <AUTHOR_NAME>
title: <DISPLAYED_TITLE>
---
```

### Adding/Editing Members
In the `_data` directory you will find a `members.yml` file. Simply add a new entry
using the existing ones as a template or make edits as required.

Each entry should look like this (if you don't have github please omit that line):

```
- name: Matthew Parker
  github: mattdmem
  institute: Sheffield University Bioinformatics Core
  email: matthew.parker@sheffield.ac.uk
  website: http://sbc.shef.ac.uk/
```

### Adding/Editing Meetings
In the `_data` directory you will find a `meetings.yml` file. Simply add a new entry
using the existing ones as a template or make edits as required. Meetings are automatically
displayed in the "Past" section if the date of the meeting was before today's date.

Each entry should look like this:

```
- meeting: NorthernBUG|2
  theme: Clinical Bioinformatics
  month: September
  day: 14
  year: 2018
  institute: University of Sheffield
  city: Sheffield
```
