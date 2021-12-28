---
layout: essay
type: essay
published: true
title: Athletic Software Engineering--Initial Results
date: 2013-12-16
labels:
  - Athletic Software Engineering
---

Last summer, I speculated about an "athletic" approach to teaching software engineering, including:

* A [flipped](http://en.wikipedia.org/wiki/Flip_teaching) classroom: lectures are online, freeing up class time for other activities.
* A primary focus on *skill* acquisition, and a secondary focus on *concept* acquisition. For example, rather than assess the ability of students to explain the difference between white box and black box testing, the approach assesses their ability to implement white box (or black box) testing.
* An emphasis on *fluency*, as measured by the time to complete tasks correctly. For example, given the task of writing a test case to verify that a system exhibits a specific behavior, students are evaluated on their ability to implement it *quickly*, as well as their ability to implement it *correctly*. This elevation of speed to a first class component of the pedagogy gives the class its "athletic" feeling.

For a lengthy discussion of the ideas and motivation for athletic software engineering, please see my [July, 2013 blog post](http://philipmjohnson.wordpress.com/2013/07/12/athletic-software-engineering-education/). Today I want to explain what happened when I tried it out in my undergraduate software engineering course.  If you like, you can take a quick look at my [course website](http://ics314f13.wordpress.com/) before reading further.  I will link to specific pages in this site below.

## Logistics 

So, how do you actually make a software engineering class "athletic"?  My solution involves several techniques.

**Logistic #1: WODs.** The first, and most important technique is the "WOD", or "Workout of the Day" (a term I borrowed from [CrossFit](http://www.crossfit.com/cf-info/faq.html#General0).  In my class, "WOD" refers to a software development problem that can be solved by an experienced practitioner in a pre-specified, short period of time.  In addition to specifying the problem, each WOD specifies four time intervals: Rx, Av, Sd, and DNF.  Rx (as prescribed) is less than or equal to the time required for the experienced practitioner to solve the problem; Av (advanced)  and Sd (standard) are longer intervals but still acceptable, and DNF (Did Not Finish) defines an unacceptable length of time. For example, a WOD might have:

* an Rx time of &lt;14 minutes,
* an Av time of 14-20 minutes, and
* an Sd time of 20-25 minutes, and
* a DNF time of 25+ minutes.


To determine the Rx time for the WODs, and to provide a reference solution, I made <a href="http://www.youtube.com/playlist?list=PL-iE2lvAri0RQo_NmVQmu-MduBwZZtyL8">screencasts of myself solving the problems</a>.  The screencasts enable students to see a solution in Rx time and learn how to efficiently solve a particular problem.  DNF indicates the "point of no return".  For homework assignments, reaching DNF indicates they should stop trying to solve the problem and watch my reference solution, then try again.  For in-class assignments, reaching DNF means they failed and will receive little to no credit for the assignment.

The primary instructional technique was the WOD.  During Fall, 2013. I designed a total of 59 WODs: 39 "practice" WODs assigned as homework, 10 "group" WODs attempted during class in small groups, and 10 "in-class" WODs attempted individually and graded.  Not counting the first and last week of class, there were approximately 13 weeks (65 days) during the semester, so "workout-of-the-day" comes dangerously close to an accurate description.

For the in-class WOD, I wanted to record accurate time data for each of the 20+ students, and provide some degree of privacy regarding their results over the course of semester. My solution was to keep  an envelope for each student containing an index card with their WOD data on it.   Before each in-class WOD, I distributed their envelopes, and each student filled out a line on the index card with the date and the WOD name. When the WOD began, I started a timer on my watch. Students were told to raise their hand when they were finished. I told them how much time had elapsed, then watched them record their time on their index card and collected it.  All students emailed me their work at the end of the class so I could verify the correctness of their solution. This approach enabled me to obtain accurate timing data for each student, verify that they solved the problem correctly, and kept their cumulative WOD data somewhat private.

See the <a href="http://ics314f13.wordpress.com/course-info/wod/">WOD Page </a>for more details.

**Logistic #2: Modules and the weekly rhythm.** I organized the material into <a href="http://ics314f13.wordpress.com/course-info/modules/">a sequence of 18 "modules"</a>, each generally requiring a week to complete.  The course presented software engineering concepts using the domain of web application development.  The class met on Mondays and Wednesdays. Most weeks, the class had the following "rhythm":

* *Thursday:* The week's module is released via a web page providing access to resources (online lectures, readings, and practice WODs).
* *Thursday - Monday:* students study resources, begin work on practice WODs.
* *Monday (in class):* Students do a timed, non-graded WOD in small groups. This helps them assess their current understanding and learn about the material.
* *Tuesday:* Students submit a blog posting discussing their experience carrying out the practice WODs.
* *Wednesday (in class):* Students do a timed, graded individual WOD.


The <a href="http://ics314f13.wordpress.com/course-info/course-rhythm/">Course Rhythm page</a> provides more details.

**Logistic #3: HEBS (Homework, Exercise, Breakfast, Sleep) Score.**  High performance athletes take into account a variety of physiological factors when preparing for an event.  To help the students think in a similar fashion, I designed the "HEBS Score", which asked students to self-assess four factors on a scale of 0-2 before each in-class WOD:

1. how well they completed the practice WODs
2. whether or not they exercised in the past 24 hours
3. the nutritional quality of their Breakfast (the class was at 10:30am)
4. how many hours of sleep they obtained the previous night.

The <a href="http://ics314f13.wordpress.com/course-info/hebs/">HEBS page</a> provides more details.

**Logistic #4: Data collection.** To better understand the approach, I looked at a variety of data.


1. <a href="http://ics314f13.wordpress.com/course-info/portfolios/">Student portfolios</a> provide a self-reported record of their experiences during the class, including blog postings reporting the number of times they attempted each practice WOD and what they learned from each module.
2. The <a href="http://ics314f13.wordpress.com/course-info/practice-wod-repetitions/">Practice WOD repetitions page</a> presents the results of a simple analysis of student postings in order to see whether or not students would repeat practice WODs in order to increase their fluency and/or understanding of the material.
2. I created <a href="http://ics314f13.wordpress.com/course-info/in-class-wod-results/">aggregate in-class WOD results</a> to show the relative number of Rx, Av, Sd, and DNF times for each in-class WOD.
2. Students filled out a questionnaire near the end of class. The <a href="http://ics314f13.wordpress.com/course-info/wod-end-of-semester-reflection/">WOD End-of-Semester Reflection page</a> presents insights about the course from a student perspective.

By following these links, you can see that a substantial amount of data about the class is available.  The next section attempts to highlight the most important results.

## Initial Results

**Result #1: Students like WODs.**  The questionnaire results were unequivocal: <a href="http://ics314f13.wordpress.com/course-info/wod-end-of-semester-reflection/#which-approach">100% of the students prefer WODs to a traditional course structure</a>.  I was a bit surprised at the unanimity, as the WOD approach created a new form of pressure on students: not only were they supposed to learn new techniques each week, but they also needed to learn to do them quickly.   The flip side is that WODs gave students a clear target for "mastery" that is not necessarily present in a traditional course structure.

**Result #2: The instructor likes WODs (but they involve new and time-intensive efforts).** Presenting software engineering as an athletic endeavor is, well, fun. After the first WOD, when <a href="http://ics314f13.files.wordpress.com/2013/08/wod-fizzbuzz2.png">over half the class DNF'd</a>, I reacted (to my surprise) not as a "professor" (which for me would have meant admonishing them to study harder), but rather as a "coach" (which meant I advised them to "shake it off", that "tomorrow is another day", and that "you'll get used to the pressure by the end of the <span style="text-decoration:line-through;">season</span> semester".)

WODs required me to redesign my former "flipped" curriculum. I created <a href="http://www.youtube.com/playlist?list=PL-iE2lvAri0Sl3s456hLrvUiBk1xGXJFP">approximately 80 videos</a> for the class, and about 60 of them were entirely new content. This was about twice as many videos as I created for my prior flipped software engineering curriculum. It was often challenging to figure out a way to present software engineering concepts in a manner amenable to WOD-based practice and assessment.

Finally, WODs required me to create a video that documented a reference <em>process</em> for solving a programming problem, as well as the reference solution.

**Result #3: If at first you DNF, WOD, WOD again.** Before this semester, I would not have thought it would be useful to assign the same programming assignment twice, and I would not have thought students could be convinced to repeat one. The data proves me wrong.  First, analysis of self-reported data in student blog postings shows <a href="http://ics314f13.wordpress.com/course-info/practice-wod-repetitions/">substantial repetition of practice WODs</a>.  In fact, over half of the students repeated a WOD three times.  The questionnaire data shows that <a href="http://ics314f13.wordpress.com/course-info/wod-end-of-semester-reflection/#repeating">two thirds of the students found repeating WODs to be useful</a>. Fluency requires practice, and students found fluency to be a motivating goal.

**Result #4: WODs help students focus.** Twitter, Facebook, text messages, Instagram, SnapChat: these are only a few of the distractions confronting the modern undergraduate. WODs appear to provide at least a partial remedy:  <a href="http://ics314f13.wordpress.com/course-info/wod-end-of-semester-reflection/#focus">80% of the students reported that WODs helped them to focus.</a>  It is not clear whether this experience helped them to focus outside of WODs.

**Result #5: You can't MOOC a WOD.** <a href="http://en.wikipedia.org/wiki/Massive_open_online_course">Massively open online courses</a> are an interesting recent innovation in pedagogy.  My initial experience suggests it would be difficult to provide the WOD experience within the MOOC paradigm.  For one thing, <a href="http://ics314f13.wordpress.com/course-info/wod-end-of-semester-reflection/#helped-learning">95% of the students felt an in-class WOD was important to the learning experience</a>. That said, cloud-based IDEs such as <a href="https://www.nitrous.io/">nitrous.io</a> could potentially lead to an online, verifiable WOD experience.

**Result #6: Git is great.** Well, I already knew that, but it was useful in two unexpected ways in the class. First, git branches make it extremely easy for students to repeat WODs: they create a branch off master, do the WOD in the branch and commit the end results, then switch back to master to immediately reset to their starting point for their next attempt. Second, making a commit at the start and end of a WOD created timestamps that could verify the actual time elapsed.

**Result #7: HEBS didn't work.** Having students record their homework, exercise, breakfast, and sleep data seemed like a promising idea, but I was unable to find any consistent relationship between the HEBS data and student WOD scores, and <a href="http://ics314f13.wordpress.com/course-info/wod-end-of-semester-reflection/#hebs">the students weren't able to either</a>.

## Future directions

**Direction #1: Improve the module sequence.** Both the students and I agree that testing should have been introduced far earlier in the semester.  In my next iteration, I also want to introduce git and github at the very beginning of the semester, since they provide such great infrastructure for WODs.

**Direction #2: Non-Lockstep Modules.**  This semester, all students marched in "lock step" through the sequence of 18 modules. This made it easier for me to manage the course, and easier to create collaborations, but: (a) a few students seemed to be "coasting" at times; and (b) a few other students seemed to be obviously unprepared for the in-class WOD.  It would be interesting to present most, if not all, of the modules on the first day of class, and then let students progress through the curriculum at varying rates.   This would also enable students to re-take an in-class WOD if they DNF'd it, rather than having them simply move on to the next module.

A related expansion would be to organize the modules as a lattice rather than a linear list, and allow students to take different paths through the curriculum, emphasizing different aspects based upon their interests.

**Direction #3: Practice WOD validation.** This semester, the practice WODs were effectively optional: there was nothing to prevent a student from taking the in-class WOD without any prior preparation (and this did appear to occur a few times).   Online IDEs such as nitrous.io could potentially lead to"validated practice WODs", where one could ensure that students complete the practice WODs before they are allowed to take the in-class WOD.

**Direction #4: Forkable Curriculum.**  Most of the modules have two aspects: a <em>concept</em> (such as "version control", "testing", "web application framework") along with a specific <em>technology</em> ("git", "fluentlenium", "play framework").  This semester, I used WordPress to organize the content, which makes reuse and modification for future semesters somewhat difficult.

Next time, I want to manage the content using markdown files in  <a href="https://github.com/">GitHub</a> along with a static site generator such as <a href="http://jekyllrb.com/">Jekyll</a> to produce the web interface. My goal is to create a simple way for others to build upon this curriculum by either: (a) modifying the set of concepts presented in their course from mine (for example, providing a new module on continuous integration); or (b) keeping the same concept, but changing the technology (for example, changing the web application framework from the play framework to ruby on rails).

Your thoughts? Please email me with your comments.