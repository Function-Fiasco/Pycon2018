<!-- Both your title and this description are made public and displayed in the conference program to help attendees decide whether they are interested in this presentation. Limit this description to a few concise paragraphs.

Please do not include any personally identifiable information. The initial round of reviews are annonymous, and this field will visible to reviewers. -->

# What are Pseudo-Tested Methods?
One of the most important phases of the development cycle is the testing phase. This is where a developer will be able to know if they have implemented what they are working on correctly. One major question though is "Are the tests written correctly?" Developers can rely on coverage as a metric to determine how much of the system is being executed during the testing phase, but it may not always be a good indicator of the fault detection effectiveness of a test suite. A reason that this could be the case is because a test has not been written very well and creates a scenario that is called a pseudo-tested method. A pseudo-tested method, simply put, is a method that is being used in a test that will never fail. Meaning that the method is being executed, but not tested effectively.

# Current State of the Field
A pseudo-tested method as an idea was only recently defined in 2016. So, unfortunately there are many systems that could have them without knowing. Since this is a relatively knew idea, there really are not many ways to detect them, the largest way being that of detection by hand. There is a system that can detect them automatically, but it is written for Java systems. Therefore, I have created Function-Fiasco, an automatic detection system for pseudo-tested methods.

# What is Function-Fiasco and Why did I create it?
Function-Fiasco uses Python and Pytest to automatically detect whether or not a method is being pseudo-tested. It was created because of the loosely-typed nature of the Python programming language. Its main function though is to show that there is always a way to make implementation better, and that understanding that building the test suite is part of that implementation could lead to more stable systems with a lower chance of crashes.
