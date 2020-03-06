---
layout: post
comments: true
title: "Computer Science != Software Engineering"
date: 2019-07-14 10:26 -0700
categories: CS
tags: CS software-engineering
---
<br>
*This story was originally published on my Medium account (which I've since stopped using)*
<br>
> [Computer science] is not really about computers - and it's not about computers in the same sense that physics is not really about particle accelerators, and biology is not about microscopes and Petri dishes…and geometry isn't really about using surveying instruments. Now the reason that we think computer science is about computers is pretty much the same reason that the Egyptians thought geometry was about surveying instruments: when some field is just getting started and you don't really understand it very well, it's very easy to confuse the essence of what you're doing with the tools that you use."
*- Hal Abelson, Professor of Computer Science at MIT*

<br><br>
*Firstly, I want to offer a disclaimer. This article is not indicative of everyone who is majoring in CS, It's simply an observation, not a full on case study. It is also my opinion, not gospel. Take it with a grain of salt. Also, I acknowledge that there are indeed schools with majors in software engineering (like [Cal Poly](https://csc.calpoly.edu/)), so this article doesn't apply to those programs*
<br>

---

In the springtime of 2018, I enrolled in a class at UCSD called "Theory of Computation". This upper-division CSE class is (as the name suggests) a course that focuses on the some of the theory that underlies computer science, with a few practical applications sprinkled in. The class was fantastic, but I noticed a disturbing trend. Frequently, and increasingly so as the course progressed, I heard more and more students uttering phrases similar to the following:

> "This isn't even applicable to industry and is way too hard; why should we waste time learning this?"

That got me thinking: why were we learning about Turing machines, creating finite automata by hand, and using Cantor's Diagonalization Argument to prove that some languages<sup>1</sup> are undecidable? For that matter, why would we learn how to code in assembly if for the majority of software engineering jobs, we'd never have to touch anything that low-level? Why learn about anything other than how to negotiate contracts, pass interviews, and do typical web development?
<br><br>
The answer to those questions is the title of this post: computer science is not software engineering. In my opinion, reasons for wanting to study computer science will (and should) be different than reasons for wanting to become a software engineer. To be fair though, wanting to study CS to get a cushy tech job isn't a bad thing, per se. Honestly, it's not. The problem comes when someone is doing CS for that tech job but forgets that studying computer science is not studying solely software engineering. To emphasize this point, here's a helpful chart that showcases many fields of computer science that I found with a quick Google search:
<br>
<img src="https://c1.staticflickr.com/5/4387/36231833334_3252f05552_b.jpg" alt="A (non-complete) map of the fields of Computer Science" style="width: 90%;">
<br>
Why is forgetting that detail a problem? Approaching CS classes (and other things, for that matter) with the "I only care if it will be relevant to my career" defeats the purpose of learning computer science by reducing it from that large web of topics and unsolved problems into a simplistic "give me money for typing on a computer" gig. **Computer science degree programs should produce computer scientists, not software engineers.** Any computer scientist worth their salt can become a "successful" (however you choose define that word) software engineer because the degree in computer science lays a foundation on which the rest of the software engineering skills are built. In terms of set theory, SWE ⊆ CS.
<br><br>
Even though not everything learned in a CS degree directly translates to a career as a SWE, all of it is necessary to build that foundation I mentioned earlier. Not all classes need to be adored, either; I can personally say that I did not really enjoy my discrete maths class, but there was still value in learning the material even if I never write a proof by contradiction for proving the irrationality of the square root of 2 ever again.
<br>
<img src="https://i.imgur.com/gHmbCIB.png" alt="The bane of my existence" style="width: 90%;">
<br>
Likewise, learning the inner workings of IEEE-754 floating point format for 32-bit numbers is something I didn't have to think twice about as an intern, but is valuable to know nonetheless. Understanding assembly, though irrelevant on the surface, has real-world ramifications for optimization of code written. Knowing how logic gates work is crucial for understanding small subtleties behind why some things are more secure than others in terms of implementing cryptography. At the end of the day, the point of computer science isn't to write code; rather, *we solve problems* in the study of computation to gain a better understanding of how the world works using computers as the tools of choice, which is what the degree (should) train you to do.
<br><br>
With that in mind, let's revisit that Theory of Computation class I mentioned earlier. A class like that doesn't have a ton of practical SWE relevance, so why is it important? Understanding the basic models of computational thinking and ways to frame problems is crucial for being able to better understand the limits of computer science and the current realm of possibility for the field. Courses like those expose those limits by introducing concepts like problems that have solutions that cannot be solved efficiently but can be verified very quickly (like finding true/false values that make a given equation made up of variables that can take on only those values to evaluate to true, a class of problems known as NP Complete problems) or problems that are so difficult that they're impossible to solve (like knowing if a given program will stop running for any input, a problem known as the Halting Problem). *The relevance here comes from the fact that knowing exactly what you can't do gives you a good framework for what you can do* (and finding ways to estimate solutions for problems you can't do is a fascinating research field in CS; entire dissertations have been devoted to this topic). From the frame of mind of the aspiring computer scientist, taking a course like this is absolutely critical to their education in a similar way that taking a course in human anatomy and physiology is crucial for an aspiring doctor: it (kind of) defines the entire scope of the field and what it tries to accomplish and understand.
<br><br>
Another point to note is that the background gained from studying computer science is what allows the field of software engineering to exist as we know it today. As easy as it is to get lost behind the layers of abstraction, everything from the linters used in JavaScript development to the programming languages and data structures used in everyday SWE (like C++ and red-black trees<sup>2</sup> for instance) weren't invented by themselves. They were the result of computer scientists and mathematicians applying the theory they had learned to create better ways to code, thereby advancing both software engineering in specific and computer science in general! By focusing solely on the "practicality" of software engineering and ignoring the rest, we run the risk of blocking out the potential for the next great breakthrough in computation.
<br><br>
Now, if you're reading this and thinking "well dang, I don't know if I want to study computer science but I know I want to be a software engineer", I recommend you look into alternate routes to reach that goal. Maybe a degree in software engineering is for you, or maybe you'll want to find a school where you can put an emphasis on your interest in the software engineering aspect of computer science. Bootcamps get a lot of flack, but good ones are still rigourous and will make you industry ready if you put in the time<sup>3</sup>. If you're a CS student reading this and you feel like you're doing it for the money, remember that you're becoming a computer scientist so that you can support your software engineering endeavors, and not the other way around.
<br><br>
I should clarify: I do not dislike software engineers. I also aspire to work as a software engineer, albeit more of an academia focused one. I am also not saying that the only true purpose in studying CS is to become a researcher working in academia. What I am saying is that studying computer science solely for the money and potential career prospects may end up leaving you dissatisfied.
<br><br>
Why study computer science? Why care about the theory behind it all? Why learn assembly, discrete math, PLT, the principles behind logic gates and computer architectures, database theory, the heavy duty linear algebra/multivariable calculus/statistics that powers modern machine learning, random algorithms that don't come up in industry much, and all of those other topics? Because in doing so, we gain the option to learn more about the world around us by framing it in the context of computational problems to solve, setting us up for making breakthroughs for humanity in a bunch of different fields (software engineering included). At the end of the day, computer science != software engineering. And that's okay.
<br><br>

---

[1] The word "languages" is being used here in terms of the context of Formal Languages, a context used in mathematics, computer science, and linguistics.
<br><br>
[2] Here's the original research paper outlining the red-black tree: http://professor.ufabc.edu.br/~jesus.mena/courses/mc3305-2q-2015/AED2-13-redblack-paper.pdf
<br><br>
[3]Some sources for this: https://www.coursereport.com/blog/are-coding-bootcamps-worth-it, http://blog.indeed.com/2017/05/02/what-employers-think-about-coding-bootcamp/
<br><br>
*Special thanks to my friend Beth for helping me edit this opinion piece, to Owen for having the conversation that helped to inspire this essay, to Daniel and Evan for bringing up a point that I had missed initially, and to Geoffrey for the proof transcription. You all are great!*
<br>

[Go back](/innermachinations)
