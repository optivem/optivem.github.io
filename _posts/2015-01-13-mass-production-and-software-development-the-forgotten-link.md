---
layout: post
title: Mass production and software - the forgotten link
author: vcupac
created: 2015-01-13 20:14:36
modified: 2016-08-06 20:30:46
category: management 
---

Software development. Mass production. Efficiency, scalability, profit maximization. Can mass production be applied to software development?

Mass production is an excellent example of pipeline parallelism in action: work split among assembly workers such that large scale quantities can be produced with minimal waiting time. This was an attractive idea, to the extent that it had also inspired software development. However, it turned into a broken dream. 

<h2>Why we fail to realize the benefits of mass production in software development</h2>

Recall Brooks' law: "adding manpower to a late software project makes it later."
Let's also not forget that "Nine women can't make a baby in one month."

It soon became common knowledge that software development is <em>not</em> factory production, and that software development isn't civil engineering either.

There are certain factors in software development process that make it slightly painful to manage. Here are some differences:
<ul>
	<li>Factories produce standardized products, whilst most software development teams do not</li>
	<li>Assembly work is divided in smallest parts so that different workers can work in parallel, whilst this appears to be more difficult in software due to dependency complexity</li>
	<li>Assembly work tasks tend to be divided such that one worker does not need to know about all the other tasks done by the other workers, yet in software development the situation is such that it becomes necessary for developers' to understand other developers' tasks which leads to communication overhead as number of developers increases</li>
</ul>

<h2>There is still hope for mass production in software development</h2>

The above situation sounds bleak. However, there are some solutions to the above problems:

Firstly, we need to recognize that whilst we often talk about custom software, we forget that software solutions are more alike than they are different and that quite often the differences are more in language rather than underlying functionality performed. 

Secondly, we need to recognize that it is in fact possible to split tasks such that software development can proceed in parallel - by using design patterns such inversion of control (one technique is <a href="http://www.optivem.com/software-development/dependency-injection-in-plain-english/" title="Dependency injection in plain English">dependency injection</a>) which enable mock implementations of surrounding systems so that a developer does not have to wait on another developer, but instead both can work at the same time.

Thirdly, communication overhead can be minimized using common well-accepted design patterns rather than re-inventing the wheel, and writing code which exhibits low coupling, which has the wonderful side-effect that a developer is not forced to trace paths through the whole codebase but instead can focus on their task.

Hopefully the theory sounds interesting, but what can we do to make it work in practice? That's coming up - stay tuned!