---
layout: post
title: Improving software quality assurance and developing better software
author: vcupac
created: 2014-10-29 21:39:48
modified: 2016-08-06 20:29:02
category: quality 
---

Most people would agree that quality is an important part of software projects. However, the question is, what is quality, which characteristics of quality should we evaluate, which characteristics matter the most?

<h2>Software testing and the car analogy</h2>

Let's firstly start off with an example that's part of everyday life - cars. There are different strategies about how are car could hypothetically be tested:
<ol>
	<li>Stick all the car components together, put the car on the road and hope for the best</li>
	<li>Test the internals of the car, verify that they work individually, join them together, verify behavior under simulated conditions which can test bounds / limitations, and then, finally, do a test drive</li>
</ol>
Option [2] seems like a logical approach, testing components (units) of a car and then testing them after integration. This enables unit-level issues to be identified and resolved before a car is assembled, and then the only test that remains is the integration-level test which is concerned with testing that the units link up and communicate correctly. Typically, unit-level testing tends to be "white-box" testing, whilst integration-level testing tends to be "black-box" testing. In the former case, the tester relies on knowledge of the internal structure of a component. In the latter case, testing relies on specifications about how something should behave.
<h2>Introduction to software quality assurance</h2>
In software development, the term "testing" typically refers to "black-box" system testing. Using the car analogy, this is akin to taking a person taking a car for a test drive. Taking a car for a test drive is a black box test because the driver is verifying that the car functions correctly (e.g. that the wheels rotate, that the car slows down when the brakes are pressed), but without opening the hub to see the components underneath. So the car is tested without the driver knowing how the car actually works inside. In contrast, "white-box" testing would be done by people who actually produce the car and who know how it internally works.

In software development, we also have those levels:
<ol>
	<li><strong>Black-box testing</strong> refers to testing the functionality of a software system. The principal question asked is: does the system work the way it is supposed to work? Does it conform to specifications? Given a particular input, does the system produce the correct output or response? There is no question about how the system actually works.</li>
	<li><strong>White-box testing</strong> refers to testing the internal structure and internal flows within a software application. The tester, in this case, must be aware of the internal structure and code. The tester identifies the paths, and flows of data and control - with the aim of choosing inputs which will simulate the flow of data and control through those paths.</li>
</ol>
<h2>Challenges in software quality assurance</h2>
At first glance, software testing sounds straightforward: get the functional specifications of software and identify flows of data and control. However, there are some questions that plague us:
<ol>
	<li>Why is software testing difficult to do properly?</li>
	<li>Why does software testing take long to perform?</li>
	<li>Why does software have poor quality despite testing?</li>
	<li>Who should be responsible for software testing?</li>
</ol>
Software testing is difficult to do properly because (1) testing requires a special mindset to be able to think up of a representative set of test cases and (2) testing requires self-discipline and repetition. Not everyone is born with the ability to think of scenarios which will cause a system to fail, yet hat is exactly the sort of skill that great testers have.

The reason why software testing requires time to perform is that as the application grows, the complexity grows too. Increased complexity is represented by an increased number of interactions between components and myriad of paths that can be traversed whilst the software is being used.

Software testing can pass internal testing, yet may appear to be low quality. Why? The reason is that in many cases, the customer is not engaged in the process, or becomes engaged towards the end of the project. The development team might do testing based on their understanding of the business scenarios, which may or may not correspond to the way that the customer sees the software being used.

Finally, the question that springs to mind is, who should do the testing. Developers? Dedicated testers? Customers? If developers don't do testing, then testing requires external simulation of various error condition, which increases test time. However, it's not enough for just developers to do testing, instead, dedicated testers are needed too. The reason for this is that developers, given the fact that they wrote the software, are much more inclined towards positive and "happy path" testing, which is why it is valuable to have someone else be involved in testing too. Finally, even having dedicated testers is not enough, customers are necessary too, since the customer is the central figure that has in-depth understanding of business processes, which is necessary to assess software quality from the perspective of the final user.
<h2>Improving the test management process</h2>
There are a number of steps that can be taken to ensure a better (or less painful) software test process.
<ul>
	<li>Hire dedicated testers to work with software developers. Can writers work without editors? Not really. Similarly, software developers are not enough, dedicated testers are needed too.</li>
	<li>Involve the customer early in the process. Enable the customer to try out using the software, and watch how they use it - it makes writing acceptance tests much more straightforward.</li>
	<li>Understand the difference between manual and automated testing and how they can be made to work together. This will be discussed in another article.</li>
	<li>Make testing part of the development process, not something that is thrown in right at the end.</li>
	<li>Provide training to improve the team's ability to write better quality code and to be able to discover bugs faster.</li>
</ul>