---
layout: post
title: "Better CS"
date: 2019-12-26 12:00 -0700
categories: CS
tags: education teaching
---

## What I've Learned From Writing My Own Course
---

Firstly, allow me to acknowledge the elephant in the room: I haven't posted for a while. I know this.
Last quarter kind of took me for a ride (we livin' tho). That said, now that I'm on break I'm gonna
try to crank out a couple posts and then settle back into a regular schedule. We'll see how long that resolve
lasts.
<br><br>
In any case, I'm finally back with the second post of the "Better CS" series. I know that on the last post in this series
<a href="https://nate-browne.github.io/innermachinations/cs/2019/08/19/Learning-PL.html" target="_blank">(click here if you missed it)</a>,
I said the next post would be about proofs. Well, two things have happened since that post which have changed my mind:

1. I don't feel like writing about proofs right now.
2. I just finished one of my longest side projects and need a place to talk about it.

With that said, let's dive right in, shall we?
<br><br>
As many of you know, I'm a tutor (really, an undergraduate TA) in the CSE department at UCSD. In my time tutoring, I've tutored
a wide range of courses from our first intro class to our last lower division undergraduate class and have worked my way up
from a new tutor to one of the head tutors for two courses: our basic data structures course (CSE 12) and our software tools course (CSE 15L). Over time, I started to wonder why the course itself hadn't changed much over the years. I mean, it's very, very similar to the version that other students had taken and tutored and it has been a *while*, so why not update it?
<br><br>
Naturally, I decided that the best thing to do to answer this question was to attempt to re-write the course myself and
turn it into what I would want to teach. I initially thought, "Eh this should be quick, maybe a couple days worth of work and I'll be donezo."
<br><br>
Oh boy, was I wrong.
<br><br>
What started as a couple days of work turned into an eight month ordeal of writing assignments, lecture notes,
designing websites, coming up with a style guide, asking for feedback, and fiddling around with plugins.
To be fair, I did take quite a long gap from working on it due to school, but the point still remains that it took a while.
<br><br>
Now, here are the biggest lessons I learned from embarking on and finishing this project. I hope some of these
can be applicable to you in your own endeavors; just do a bit of extrapolation:

1. __Writing a class is *hard*, yo__.

   I don't think I would have realized just how difficult it is to do each portion of the
   teaching process had I not tried it. Everything from the seemingly mundane task of picking course topics
   to the surprisingly hard part of pruning information out books and resources to make lecture notes to writing assignments/write ups
   came with their own set of surprises.
   <br><br>
   One thing that I struggled with was gaguing the difficulty of the assignments. Since I was the one writing them,
   things that seemed trivially easy to me may end up being much harder to someone taking the class, especially since
   most students at UCSD would take this class as their second or third CS course. Writing writeups was a similar ordeal,
   since they involve balancing the fine line between giving away too much and being completely useless.
   <br><br>
   In the end, I tried adopting a model of making things get progressively harder as the course goes along, which leads to...

2. __Judging how hard/useful something is without an outsider's opinion is nearly impossible__.

   Seriously though, have you tried doing this recently? Since I wrote it all, everything I would write would feel completely managable.
   After all, "if I can do it, so can they", right? Nope. Getting someone who hasn't seen your stuff to read over it and
   give you their thoughts is *crucial* to creating a good experience.
   I still think my course may be a bit too hard all told, but I'm grateful to those who read through my stuff and
   provided feedback. That gives a nice segue into...

3. __Actually listen to feedback__.

   An example of this for this project was with PA5. That assignment is an implementation of a Binary Search Tree as well
   as an AVL tree, but the original plans involved also implementing a red-black tree. I thought it'd be doable; they just had
   to use the resources given to them.
   <br><br>
   Upon discussing this with a friend, she helped me to realize that no, a red-black tree implementation for a bunch of very beginner CS students wasn't just impractical, it was pretty cruel to expect. I didn't want to admit it at first, but with this direct
   and honest feedback, the assignment was trimmed down into what it is now.
   <br><br>
  
4. __I understand why teachers tend not to modify courses too much__.

   No smooth transition into this point, sorry. I remember realizing in a lot of my courses that the material
   either was the exact same as previous years, or only had slight modifications/updates. I used to think to myself,
   *why isn't the stuff up to date? It can't be __that__ hard to do, right?*
   <br><br>
   Well as it turns out, updating/changing anything is **really** annoying. To change a PA, at a minimum I'd have to modify
   the `README.md` file, the student's `Makefile`, the solution code, the solution code's `Makefile`, the given student code,
   and probably the test driver as well. It definitely seems easier to just handle AI cases as they come up than to re-write
   new things every quarter, so special shout out to the professors/teachers I had over the years who embarked on that monumental
   task of keeping things new semester after semester, quarter after quarter. To those who didn't, I now understand your pain.

5. __Finding the balance between not enough and too much information is tough__.

   For lectures, I often struggled between putting enough information to get going but not quite understand
   and putting enough information to understand at the risk of confusing the students. The line between those two states
   is razor thin, and I still think that my lecture notes could use some improvement in this area.
   <br><br>
   Overall though, I tended to err on the side of too much information, and I tried linking to other resources that could
   explain things better than me whenever possible.

6. __Writing PAs is fun__.

   This is something I knew already from tutoring for CSE 15L, but it was *really* fun getting
   to write my own data structure assignments. Seeing how I would implement things and writing solution code to do so
   was honestly a blast, even though writing `Makefiles` and drivers was pretty... not fun.

<br><br>

Overall, though the experience took quite a while, I'm happy with the end result. I don't think the class as I've
written it will ever be taught (maybe it will), but the experience of doing this project was well worth it regardless.
<br><br>
If you'd like to check out the project, it's live <a href="https://nate-browne.github.io/CSE12_Redesign/" target="_blank">on this site.</a> The PAs
and other materials (including Solution code) are available <a href="https://github.com/nate-browne/CSE12_Redesign" target="_blank">on the project's Github page</a>. Just
don't look at the solutions if you're planning on doing the PAs!
<br><br>
That's all I have for this topic; thanks for reading! The next "Better CS" post will be about proofs, but I'm not sure
if that'll be the next post here. I have some other stuff I wanna talk about too, so we'll just
see what I'm in the mood for.

---
[Go back](/innermachinations)