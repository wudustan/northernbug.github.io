---
layout: page
title: Contact
permalink: /contact/
---

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
  twitter: bioinfomatt
  interests: Clinical Bioinfromatics, Cancer, Variant Calling, Structural Variants
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

### Adding/Editing A Meeting Page
Add a page in the format `northernbug2.md` to the folder `meeting_details`this should have the following format:

```
---
layout: meeting
author: <MEETING_HOSTS>
title: <MEETING_TITLE>
date: <DATE>
institute: <INSTITUTE>
postcode: <VENUE_POSTCODE>
address: <FULL_VENUE_ADDRESS>
permalink: <FILENAME_WITHOUT_.md> 
---

# General

# Agenda

| Time          | Speaker        | Presentation | Information |
|---------------|----------------|--------------|-------------|
| 12:00-13:00   | Lunch          |              |             |
| 13:00-14:30   | Session 1      |              |             |
| 14:30-15:00   | Coffee         |              |             |
| 15:00-16:00   | Session 2      |              |             |
| 16:00-17:00   | Discussion/Pub |              |             |


# Registration

# Attendees

```


### Meeting Sign-Up
Meeting sign-up is powered by google forms. We have just hijacked the names
of fields and the action to create our own form. Responses go into a google sheet.

Once a meeting registration is closed we will create a new tab and preserve the
sign-up list from previous meetings in their own tabs.
