# Processes, Standards and Documentation for Data-Driven Projects

#### (A.k.a. teamwork)

[Paul Overberg, USA Today](http://www.usatoday.com/staff/1101/paul-overberg/)
[Christopher Groskopf, NPR](http://www.npr.org/people/348761273/christopher-groskopf)


## Case study — Changing Face, USA Today
[changingface.usatoday.com](http://changingface.usatoday.com)

* Focus on diversity
* Data driven
* ~70 newsrooms
* National umbrella
* Local data -> Local stories and approaches

##### Based on USA Today diversity index:

* every county 1960-2060
* every public school, 1991-2011
* Cities/tracts, 2000,2010

#### Content for USA Today:

* 3 major stories
* Supporting graphics, video, interactives

#### Content for networked newsrooms:

* Data files
* Advisories
* Documentation
* Data dictionary
* Webinars for print and broadcast
* Consultation

### E pluribus pluribus!

* Not a project
* No set team
* No common goal
* No set schedule
* No shared project

Calls for a separate set of skills

"Some people don't know how to play nice with the other kids."

### To succeed when no one's in charge…

* Listen **hard** (no project vocab/shorthand)
* Respect: Focus
* Respect: Park ego
* Start project vocab early
* Document early, often and in public
* Signal all turns!

## 16 solutions for data-driven projects

bit.ly/nicar15-process-slides
bit.ly/nicar15-process-notes
bit.ly/nicar15-process

Solutions for what? We're so bad at everything!

Two people who make mistakes: Me and everyone else.

### 1. Automate everything you reasonably can.

Suggestion: Use bash

### 2. Make scripts idempotent

Cleanup after yourself. Running it twice shouldn't change the output.

### 3. Never modify originals

Treat files as immutable objects. 15 steps = 15 files

### 4. Name things using least-to-most-specific pattern

Year-Month-Day-Org-Topic

Dashes to slashes creates a directory structure

### 5. Test to validate the original data

Is it what your souce is?

### 6. Test to audit your transformations

Is your file format conversion lossy?

### 7. Test when you assert novel facts.

CYA

### 8. Write detailed logs

It doesn't hurt to write to several different files.

### 9. Script setup and querying on databases

Then export to a neutral format.

### 10. Follow the crowd

Use CSV for tables. Use JSON for hierarchies. Use csvkit, ogr2ogr, jq etc. for processing.

### 11. Define and follow coding conventions

E.g. [NPR Visuals best practices](http://bit.ly/nprviz-best-practices)

Better to have some process than no process.

### 12. Store documentation with code

In version control (earlier code = earlier/relevant documentation).

### 13. Document provenance of data

How was this data created?

### 14. Have a setup script

New users should not need to know how your dependencies work

### 15. Be a ticketing zealot

If you find a bug, don't fix it. Don't get distracted.

### 16. Use comments to explain the why

But **code** should never be confusing. And don't restate the code in comments.

### 17(?). Be smart about breaking the rules.

## Questions

#### Ideas outside scope?

"Let's talk later"

#### Small temas or individuals?

"Love letters to future you"

#### Strategies for dealing with terrible filenames (if files are immutable)

Files of originals, first step is to copy and change names

#### Project management tools

Training people in, like a militia.

* People who we can mandate what they use
* People who will learn if you approach them correctly (often 1 on 1)
* Intransigent. Sometimes you just have to file a ticket and send an email.

#### Doing data before the USA Today  project

Bosses agreed USA Today should spearhead the project.

Set up the timetable to front load on purpose.

Maximizing asynchronousness

#### Ticketing systems

GitHub issues, because it integrates nicely. But it's not great.

#### Allotting time for documentation as opposed to tutorials, etc.

Part of the project planning. Whatever it takes to get it done. It's time well spent.

Two sources of documentation in CSVkit. API docs and tutorial. Very different audiences.

Non-technical users require non-technical documentation.

#### Forcing yourself to comply with the rules

Sometimes, but more guidelines.

Worry less about editing SQL table than a file, because you're not going to hand edit SQL

#### Dealing with non-reproducable steps

1. Anytime you're doing something like Open Refine (or mapping one value to another e.g. normalizing data). Produce a mapping file, then use that.

2. Also document that step in the code. Code break, say what you did, use new file.

#### Feedback on documentation

If it's bad, you'll get feedback.

Share to smaller group first.

Iterate documentation.