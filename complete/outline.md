<!-- The “outline” is a skeleton of your talk that is as detailed as possible, including rough timings or estimates for different sections. If requesting a 45 minute slot, please describe what content would appear in the 45 minute version but not a 30 minute version, either within the outline or in a paragraph at the end.

Please do not include any personally identifiable information. The initial round of reviews are anonymous, and this field will visible to reviewers.

Committee note: The outline is extremely important for the program committee to understand what the content and structure of your talk will be. The timings/percentages help us compare multiple talks that might have a similar abstract. We know that they are estimates and only capture your view at this moment in time and are likely to change before PyCon. We hope that writing the outline is helpful to you as well, to organize and clarify your thoughts for your talk! The outline will not be shared with conference attendees. -->

Introduction [10 min]
 - Testing
    - Process of software testing will be explained
    - Why it is an important part of the development cycle
 - Why testing is so important
    - Explain the benefits of software Testing
 - Define coverage and explain its benefits
    - What is coverage
    - How is it helpful
    - How can it be misleading

Pseudo-tested Methods [10 min]
 - What is a pseudo-tested method
    - A method that is being used in a test that will never fail.
    - Can be created very easily
    - Small code example
 - How it poses a problem to the stability of systems
    - There are inputs that the system is not fully prepared for
    - Leads to scenarios that may crash the system and behaviors that the developers do not know about
 - Ways to detect
    - By hand
    - One tool if you are using Java

Automatic Detection [5 min]
 - Function-Fiasco
    - What is it
 - Type-Checking
    - How it is made for Python in Python
 - Updated Metrics
    - Indicator of the fault detection effectiveness of the system

Conclusion [5 min]
 - Reiterate that the detection of pseudo-tested methods may lead to test suites that have increased fault detection effectiveness
 - Provide links to the GitHub, slides, and the thesis
 - Thank you
 - Questions if time permits
 - If not, explain where I can be found.
