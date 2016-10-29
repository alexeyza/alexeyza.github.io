---
layout: post
title: "Supporting The Contributing Student"
date: 2016-05-04 21:26:38 -0700
comments: true
published: false
categories: [GitHub, Learning, Education, 'Social Media']
---
The modern ecosystem of tools and channels students use to support their learning is quite elaborate. For example, in a course we recently taught, *GitHub* was used to host and disseminate the course material; *Moodle* was used for assignment submission and for posting grades; For private communication students used *email*, and for group communication and class discussion they used *Slack*; For collaborating on files *Google Drive* or *Dropbox* were used; and for managing and coordinating tasks students used *Trello*.

<center><img style="margin: 8px 20px" src="/images/student_ecosystem_tools.png" height="360" title="Student ecosystem of tools and channels"/></center>

If we consider the learner's needs, we could say that the most **basic needs** (i.e., hosting and disseminating course materials, facilitating communication, and supporting evaluation) can be satisfied by Moodle and email. And then tools like *Google Drive*, *Dropbox*, *Slack*, and *Trello* support the learner's **collaborative needs**, while tools like *GitHub* and *Stack Overflow* support the learner's **participatory needs**.

In this post, we'd like to focus on *GitHub*.

<!--more-->

## Student Experiences Using GitHub in SE Courses
We [previously studied](/pdf/cscw15.pdf) **How** and **Why** educators use GitHub and we found that the use of GitHub provides many benefits. GitHub supports and encourages **knowledge co-construction** and allows reuse and sharing of materials. It provides transparency of activity, and promotes collaboration while fostering a **participatory culture** where students act not only as "consumers" but also as "contributors". And the use of GitHub also provides **applied benefits**, in the form of industry relevant skills and practices.

We [shared these findings with the community](/blog/2015/09/10/embracing-participatory-culture-in-education/) and discovered that many other educators have adopted the use of GitHub (each in their own way). However, until now we haven't considered the student's perspective. More specifically **how do students benefit** from using GitHub in their courses, **what challenges do students face** when GitHub is used, and **what recommendations can we give instructors** who plan to use GitHub.

Thus, we set out to explore the student experiences when using GitHub in software engineering courses.

## Our Study
We recruited a university instructor that was about to teach two different software engineering courses offered in the same semester: a Distributed Systems course aimed at both undergraduate and graduate students, and a Software Evolution course for senior undergraduate students. The distributed systems course covered topics surrounding distributed systems and included concepts such as design considerations, fault tolerance, and cloud computing. The software evolution course covered the development of large-scale systems and how software evolves over its lifetime.

<center><img style="margin: 8px 20px" src="/images/icse_seet_16_participants.png" height="300" title="Study participants"/></center>

Both courses were similar in size (34 in distributed systems, 29 in software evolution) and learning activities (weekly labs, two course projects). The course projects were done either individually or collaboratively with others (in groups of 2-4 students). Projects were open-ended and students could choose what they created, what topics they addressed, and what technologies and languages they utilized. Students were required to make their work publicly available so that other people, both inside and outside the course, could view their projects. While not mandated, the overwhelming majority of students opted to use GitHub to host their projects. The instructor did not formally introduce GitHub to the students, so those unfamiliar with the tool had to learn from others or teach themselves.

For the first phase of the study, we conducted a preliminary interview with the instructor in order to obtain context on how they were planning to use GitHub. Then, after the students have submitted their first course project, we conducted the main part of our study where we interviewed students. In total, we interviewed 19 students --- 12 students from the distributed systems course, 6 from the software evolution course, and 1 student who was taking both courses. We concluded this phase with interviewing the instructor.

Informed by the findings from the previous phase, and by obtaining additional context from the students' project repositories on GitHub, we composed and deployed a validation survey. 33 students answered the survey (not necessarily the same students that were interviewed previously).

## How was GitHub used in these courses?
In both courses, GitHub was used for hosting and disseminating course materials, and for hosting student projects. Additionally, GitHub 'issue' feature was used to facilitate lab work and discussions.

However, GitHub was NOT used to completely replace the university's learning management system (i.e., Moodle) --- private discussions and grades were still hosted on Moodle. Furthermore, advanced use cases of GitHub to support learning were not utilized, e.g., the use of Pull Requests for assignment submission, or the use of continues integration tools for auto-grading.

## The contributing student
Enabling cross-team collaboration and contributions:
{% blockquote SE10%}
<em>"I believe that one other group decided for project 2 to use [our project 1] and they made a couple of pull requests."</em>
{% endblockquote %}

{% blockquote SE11%}
<em>"I thought [peer reviews] was the best way to learn..."</em>
{% endblockquote %}

Student contributions to course content:
{% blockquote SE1%}
<em>"I like being able to fix the mistakes that [the course instructor] might make... because it makes me feel a little more involved."</em>
{% endblockquote %}

## Breaking the "walled garden"
Students find mentors "upstream" [John Britton 2015]

{% blockquote SE1%}
<em>"These are just people in the community I've been talking to about how to do different things, and they've been giving me suggestions."</em>
{% endblockquote %}

{% blockquote Course Instructor%}
<em>"I need to get them to engage with the community in a broader sense. And I think that's critical, and that's what GitHub has."</em>
{% endblockquote %}

## Gaining and Demonstrating Industry Relevant Skills and Practices
{% blockquote SE8%}
<em>"I think when you go and work in software development, you should get used to [having] lots of eyes being all over your work; that's just the way it's gonna be, so it's practice before real life."</em>
{% endblockquote %}

{% blockquote SE6%}
<em>"I think all three companies that I applied to this semester wanted me to link to my GitHub."</em>
{% endblockquote %}

## The Perils of Public Projects

{% blockquote SE6%}
<em>"It would actually be nice if [our projects] were separate or private somehow so I wouldn't have to go through everything and sanitize all the stuff... "</em>
{% endblockquote %}

{% blockquote SE6%}
<em>"The final product I'm happy to show [employers], but all those steps getting there, they're often filled with pitfalls and horrible programming and badly factored code."</em>
{% endblockquote %}


## Unfamiliarity with Git and GitHub

Many students were unfamiliar with Git & GitHub's features

The instructor's lack of experience with using GitHub made it difficult to educate the students on its features, causing frustration


## Notification Overload
{% blockquote SE10%}
<em>"It sent me a million emails... I should have just turned that off, but I was worried about missing something. Because every time someone would post, you would get another email... 
I actually did not read anyone else's feedback because it was just so many emails, to be totally honest."</em>
{% endblockquote %}

## GitHub is Not Designed for Education

GitHub struggles to meet some basic needs, e.g., gradebook and formal assignment submission features.

{% blockquote SE12%}
<em>"I think one drawback of GitHub is that you cannot actually see the diff [of ] commonly used files such as PPTs or PDFs, so you can't really use it for correcting professor's slides, or PDFs.”</em>
{% endblockquote %}

## Planning to use GitHub in your course - here are Recommendations for SE Instructors

**Promote the desired workflow**
otherwise potential benefits might be missed

**Familiarize yourself with GitHub**
know the possibilities (e.g., private vs. public repos),
take advantage of existing tools and guides (e.g., GitHub classroom, Elliot Blackburn's guide, or  Paul Hibbitts' course hub CMS package)

**Use supported formats**
such as plain text file formats (e.g., Markdown)

## What is our next step?
We began to study what **benefits** and **challanges** of using Slack in software engineering courses.