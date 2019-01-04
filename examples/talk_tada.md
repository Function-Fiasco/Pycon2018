# How to Automatically Determine the Big-O of a Python Function

<!-- Both your title and this description are made public and displayed in the
conference program to help attendees decide whether they are interested in this
presentation. Limit this description to a few concise paragraphs. -->

<!-- REMINDER: Need to ensure that all paragraphs are soft-wrapped before
submission through the PyCon 2019 site. -->

## Description

Have you ever wondered about the efficiency of a function written in Python? As Ned Batchelder explained in his PyCon 2018 presentation, the Big-O of a Python function describes how the "code will slow when the input grows". Since the use of Ned's approach to determining a function's Big-O is potentially time-consuming and difficult, this talk presents TADA!, a tool for the auTomAtic orDer-of-growth Analysis of a Python function. Given a function and an easy-to-create description of its input, TADA! runs experiments that reliably suggest the function's likely Big-O. These experiments double the size of the function's input and track how its execution time increases. For instance, if the running time doubles as its input size doubles, then TADA! has evidence that its Big-O is linear. Yet, if a function's running time quadruples when its input doubles in size, this suggests that its Big-O is quadratic. Along with supporting the study of a Python function with a hard-to-derive Big-O, TADA! enables a Python programmer who follows Ned's approach to confirm their intuition about a function's efficiency.

After overviewing the fundamentals of Big-O and highlighting the application of TADA! to varied Python functions, this talk shows how the tool uses [Perf](https://github.com/vstinner/perf) to collect reliable measurements of a function's execution time. Since TADA! asks the user to describe each input that a Python function accepts, the presentation also explains how the tool adopts [JSONSchema](https://github.com/Julian/jsonschema) for this task. Along with highlighting how the tool determines when it has run enough experiments to discover the likely Big-O for a function, the presentation explains how TADA! repeatedly doubles the size of the input using [Hypothesis](https://github.com/HypothesisWorks/hypothesis) to generate meaningful data that adheres to the each user-provided parameter description. Using accessible examples, the presentation also illustrates how TADA! enables programmers to automatically understand and improve the efficiency of a Python function.

Even though TADA! builds on the simple concept of a doubling experiment and adopts well-known tools such as Perf, JSONSchema, and Hypothesis, this presentation surfaces the challenges associated with ensuring that the tool works well for real-world Python functions that accept complex inputs. Along with explaining how to tune both Perf and Hypothesis so that TADA! can efficiently arrive at the correct Big-O for a Python function, the talk presents the results from experiments assessing the tool's accuracy and performance. The presentation also highlights Python functions with tricky-to-derive Big-Os, showcasing how TADA! automatically determines the correct worst-case time complexity. In summary, people who attend this talk will learn about a general-purpose, easy-to-use, and automated approach for experimentally studying and improving the performance of the functions in real-world Python programs.

Since the speaker is not allowed to submit personally identifiable information, this talk description does not reference the GitHub repository for TADA!. If this presentation proposal advances to the next round of review, the speaker will update its description to cite TADA!'s GitHub repository.

## Audience

<!-- 1–2 paragraphs that should answer three questions: (1) Who is this talk
for? (2) What background knowledge or experience do you expect the audience to
have? (3) What do you expect the audience to learn or do after watching the
talk? -->

Even though the topic of this presentation is often thought of as "theoretical", this talk is accessible to programmers who have a basic knowledge of Python and want to learn more about how to automatically characterize and improve a program's performance. Although the talk adopts Ned Batchelder's PyCon 2018 presentation as a starting point, it is self-contained, thereby allowing audience members to understand its key points even if they did not attend Ned's presentation. The talk will also benefit Python programmers who want to learn more about how to use tools such as Perf, JSONSchema, and Hypothesis. Along with understanding the implementation and use of TADA!, people who attend this talk will know how to think about, characterize, and improve a Python function's Big-O.

## Outline

<!-- The “outline” is a skeleton of your talk that is as detailed as possible,
including rough timings or estimates for different sections. If requesting a 45
minute slot, please describe what content would appear in the 45 minute version
but not a 30 minute version, either within the outline or in a paragraph at the
end. -->

- What are the Challenges? (10 minutes)
  - The Big-O of a Python function
  - Why manual Big-O determination is difficult
  - Limitation of existing methods and tools
  - Overview of TADA!'s automated approach

- How does TADA! Work? (15 minutes)
  - Providing a Python function and an input description
  - Using Perf for reliable function timing
  - Specifying function parameters with JSONSchema
  - Using Hypothesis to automatically generate data
  - Performing doubling experiments with TADA!
  - Examples that illustrate the use of TADA!
  - Experiences with tools like Perf and Hypothesis

- What are TADA!'s Limitations and Future Work? (5 minutes)
  - Examples of functions with Big-Os that are tricky for TADA!
  - Potential pitfalls with Perf, Hypothesis, and TADA!
  - Future work that addresses these limitations
  - Invitation for the Python community to:
    - Suggest Python functions for study with TADA!
    - Try out and contribute features to TADA!

<!-- Anything else you would like to share with the committee: Please do not
submit personally identifiable information. Speaker public speaking experience.
Speaker subject matter experience. Have the speaker(s) given this presentation
before elsewhere? Links to recordings, slides, blog posts, code, or other
material. Specific needs or special requests — accessibility, audio (will you
need to play pre-recorded sound?), or restrictions on when your talk can be
scheduled. -->

## Notes

The speaker is an award-winning educator with twenty years of experience in teaching software engineering and software testing to graduate, undergraduate, and high school students. Collaborating with a diverse and highly skilled group of students and colleagues, the speaker has given presentations at a wide variety of conferences for researchers and developers, including the International Conference on Software Testing, PyOhio, PyGotham, and the PyCon Education Summit. Along with teaching courses and conducting research, the speaker implements, tests, documents, and debugs open-source software available on GitHub.

Since the speaker is not allowed to submit personally identifiable information, this content is abbreviated. If this presentation proposal advances to the next round of review, the speaker will provide more details about prior speaking experience and furnish links to relevant web sites, blog posts, and videos.
