<!-- The “outline” is a skeleton of your talk that is as detailed as possible, including rough timings or estimates for different sections. If requesting a 45 minute slot, please describe what content would appear in the 45 minute version but not a 30 minute version, either within the outline or in a paragraph at the end.

Please do not include any personally identifiable information. The initial round of reviews are anonymous, and this field will visible to reviewers.

Committee note: The outline is extremely important for the program committee to understand what the content and structure of your talk will be. The timings/percentages help us compare multiple talks that might have a similar abstract. We know that they are estimates and only capture your view at this moment in time and are likely to change before PyCon. We hope that writing the outline is helpful to you as well, to organize and clarify your thoughts for your talk! The outline will not be shared with conference attendees. -->

<!-- TODO: I suggest that you only make this an outline and then put the details in
the description. -->

<!-- TODO: I judge that this is too detailed and hard to follow. -->

<!-- TODO: Avoid the use of passive voice! It is confusing! -->

- Introduction [10 min]
 - Testing
    - Process of software testing will be explained
    - Why it is an important part of the development cycle
 - Why testing is so important
    - Explain the benefits of software Testing
 - Define coverage and explain its benefits
    - What is coverage
    - How is it helpful
    - How can it be misleading

Introduction Explanation:

 - In the introduction, the process of Software testing will be explained. This
   includes how testing works, its role in the development cycle, and what unit
   testing is. This is important as it will help the attendees that are on the
   beginner level understand what the purpose of testing is.

 Next the importance of testing will be emphasized. The reasoning behind this is because testing can have a very positive impact on the stability of a system. Testing can also provide a way for developers to know if they have implemented their features correctly, as in they can check to make sure that they didn't change the way that the previous features work and that they will know if their current feature is behaving properly.

 Lastly there will be an explanation about the metric coverage. The different types of coverage will be explained including how they subsume each-other. These types all measure how much of the system is being executed by the test suite. The helpfulness of coverage will then be described. Such as it aid developers in building their test suite, this is because they can ensure that their test suite reaches all corners of the system to check that nothing is behaving improperly. Lastly, the misleading nature of coverage will be discussed. Coverage is very good at describing how much of the system is being executed, but it may not fully indicate the fault detection effectiveness of the test suite, or how good the test suite is at finding errors. The reason being is that there could be tests that execute the different portions of code, but do not effectively test them. Thus leading to a situation that creates a pseudo-tested method.

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

Pseudo-tested Methods Explanation:
 - In this section the definition of pseudo-tested method will be explained. Which is a method that is in a test that will always pass, regardless of the functionality of the method. Next it will be explained that they can be created very easily. A small code example will be used to show that a simple mistake can lead to the functionality of a method to not be tested.Please note: The code example will not be live coded, this will be accomplished through the slides.

 Next the problem that pseudo-tested methods pose will be discussed. Since it is a recent discovery, there is the potential for there to be many in large systems, that have an extensive test suite. Which means that there are portions of systems that the true behavior of code is not being tested thoroughly, and could lead to unexpected system behaviors or crashes. Another side effect of pseudo-tested methods could occur if the developer is used Test-First Development. If the test case has been written incorrectly from the start, the developer will believe that they have finished development of a feature, when in reality that behavior is not being tested. If other portions of the system rely on this method, there could be a domino effect of errors.

 Lastly, the current ways for detection will be mentioned. In the past, detecting pseudo-tested methods was very difficult, as it was really only possible manually or if the developer noticed that they made a mistake and the test suite did not accurately detect the error. The detection is made really difficult because of the nature of a pseudo-tested method. Why would a developer investigate something that is not broken. There have been steps made towards automatic detection, but in the Java programming language. Until Function-Fiasco.

Automatic Detection [5 min]
 - Function-Fiasco
  - What is it
 - Type-Checking
  - How it is made for Python in Python
 - Updated Metrics
  - Indicator of the fault detection effectiveness of the system

Automatic Detection Explanation:
 - In this section Function-Fiasco will be explained. Function-Fiasco is an automatic detection system for pseudo-tested methods in Python language that are being tested under the Pytest framework. It uses a combination of mutation testing, fuzzing, and fault injection to verify that tests are effectively testing the underlying methods of a system. It is intended to be used on the test suite of the system to ensure that the tests have been written in a way to check if the behavior of the system is being accurately detected so that unexpected errors will be caught and the test suite will fail.

 Next the reasoning that the Python language was chosen will be discussed. Python is a very loosely typed language, which means that variables can be passed around and overwritten by different data types. Function-Fiasco was written in Python for this very reason. There are going to be many types of data being passed around and tested by the system, so it needed to be able to accomplish this task without the worry of an exception. Python also has an extensive list of open source packages that aided the development of Function-Fiasco.

 Lastly, the updated metrics that Function-Fiasco produces will be mentioned. This section is to help developers understand that there is more than just coverage and mutation scores. There needed to be a metric that was the fault detection effectiveness of the test suite and this metric was skewed by the idea of pseudo-tested methods. So Function-Fiasco accounts for pseudo-tested methods and provides this metric.

Conclusion [5 min]
 - Reiterate that the detection of pseudo-tested methods may lead to test suites that have increased fault detection effectiveness
 - Provide links to the GitHub, slides, and the thesis
 - Thank you
 - Questions if time permits
 - If not, explain where I can be found.

Conclusion Explanation:
 - The conclusion is just meant to wrap up all of the topic. The beginning will be dedicated to the reiteration about the importance of detecting pseudo-tested methods. The test suite of the system is a very important piece to ensure that the behavior is what was intended, but if the tests in the suite have been written incorrectly, the testing phase of the development cycle will be less effective. This could lead to large scale systems being very unstable because of the complexity of them.

 Next I will talk about where all of the resources that were mentioned in the talk can be found. This includes the GitHub, the slides, and the full thesis that was written on the subject.

 Lastly, if there is an avenue to accept questions, this is when this would occur. Otherwise, it will be explained to people where questions an be asked outside of the talk.
