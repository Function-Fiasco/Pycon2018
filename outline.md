<!-- The “outline” is a skeleton of your talk that is as detailed as possible, including rough timings or estimates for different sections. If requesting a 45 minute slot, please describe what content would appear in the 45 minute version but not a 30 minute version, either within the outline or in a paragraph at the end.

Please do not include any personally identifiable information. The initial round of reviews are annonymous, and this field will visible to reviewers.

Committee note: The outline is extremely important for the program committee to understand what the content and structure of your talk will be. The timings/percentages help us compare multiple talks that might have a similar abstract. We know that they are estimates and only capture your view at this moment in time and are likely to change before PyCon. We hope that writing the outline is helpful to you as well, to organize and clarify your thoughts for your talk! The outline will not be shared with conference attendees. -->

Introduction [10 min]
 - Testing
    - Process of software testing will be explained
    - Why it is an important part of the development cycle
 - Why testing is so important
    - Explain the benefits of software Testing
 - coverage
    - What is coverage
    - How is it helpful
    - How can it be misleading

Introduction Explanation:
 - In the introduction, the process of Software testing will be explained. This includes how testing works, its role in the development cycle, and what unit testing is. This is important as it will help the attendees that are on the beginner level understand what the purpose of testing is.

 Next the importance of testing will be emphasized. The reasoning behind this is because testing can have a very positive impact on the stability of a system. Testing can also provide a way for developers to know if they have implemented their features correctly, as in they can check to make sure that they didn't change the way that the previous features work and that they will know if their current feature is behaving properly.

 Lastly there will be an explanation about the metric coverage. The different types of coverage will be explained including how they subsume each-other. These types all measure how much of the system is being executed by the test suite. The helpfulness of coverage will then be described. Such as it aid developers in building their test suite, this is because they can ensure that their test suite reaches all corners of the system to check that nothing is behaving improperly. Lastly, the misleading nature of coverage will be discussed. Coverage is very good at describing how much of the system is being executed, but it may not fully indicate the fault detection effectiveness of the test suite, or how good the test suite is at finding errors. The reason being is that there could be tests that execute the different portions of code, but do not effectively test them. Thus leading to a situation that creates a pseudo-tested method.

Pseudo-testedMethods [10 min]
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
 - Provide links to the github, slides, and the thesis
 - Thank you
 - Questions if time permits
 - If not, explain where I can be found.
