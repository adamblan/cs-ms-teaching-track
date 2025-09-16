---
layout: default
title: Add a Job Posting
nav_order: 5
---

# Add a Job Posting!

This site is run on a volunteer basis and we try to keep job postings here up to date and when a new one comes out, we try to add it quickly.

That being said, we may miss a posting or sometimes be delayed in adding a job posting. In these cases, you can submit your own job advertisement to the site so that we can add it.

There are two ways to do this:
1. Submit a github pull request (Preferred)
2. Email us

-----------

## Github Pull Request

If you have a job posting ad and can submit a github pull request, please do. This is the preferred way as it helps ease the burden of volunteers maintaining the site and it also allows you to tweak the ad posting to your desire.

All you need to do in your pull request is modify the appropriate `jobs-25-26.yml` file, which can be found here: [https://github.com/adamblan/cs-ms-teaching-track/blob/main/_data/jobs-25-26.yml](https://github.com/adamblan/cs-ms-teaching-track/blob/main/_data/jobs-25-26.yml)

As an example, lets say that the `jobs-25-26.yml` file has the following contents:

```
- institution: University of Colorado, Boulder
  department: Information Science
  posted: 01-August-2024
  title: Assistant Teaching Professor <br> (Told that ad has wrong title, it should be this, not "instructor")
  link: https://jobs.colorado.edu/jobs/JobDetail/?jobId=58252
  notes: (Told that ad has wrong title, it should be "Assistant Teaching Professor" not "instructor") 
```

If I wanted to add the University of Pennsylvania with a job posting from CIS that was posted on October 9th at this link: [https://www.cis.upenn.edu/open-faculty-positions/](https://www.cis.upenn.edu/open-faculty-positions/)

I would edit the file to look like:

```
- institution: University of Colorado, Boulder
  department: Information Science
  posted: 01-August-2024
  title: Assistant Teaching Professor <br> (Told that ad has wrong title, it should be this, not "instructor")
  link: https://jobs.colorado.edu/jobs/JobDetail/?jobId=58252
  notes: (Told that ad has wrong title, it should be "Assistant Teaching Professor" not "instructor") 
- institution: University of Pennsylvania
  department: Computer and Information Science
  posted: 09-October-2024
  title: Lecturer or Practice Assistant Professor
  link: https://www.cis.upenn.edu/open-faculty-positions/
```

Please add your ad to the bottom of the yml file and don't worry about messing up. If there is anything that breaks the site a volunteer will fix it since they must approve the edits anyways before it is integrated into the site.

If you need more help for submitting a github pull request, there is some documentation here you may find useful:
- [Forking a repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)
- [Creating a pull request from a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)

-----------

## Email Us

If you have a job posting ad and are having difficulties with setting up a pull request (or are just too short on time), you can send us an email with a link to your ad posting and any other notes you want to add to the posting.

Just send an email to :

`tqmcgaha` at `seas` dot `upenn.edu`

with the subject line `CS Teaching No PhD Job Posting`

Expect a response within ~1 or 2 days.

-----------

## Credits
Credit goes to the CS PUI (Primarily Undergraduate Institutions) website for doing this first and inspiring us to add this :)
For those interested, you can find their site here: [https://cs-pui.github.io](https://cs-pui.github.io)
