# DakotaParker3.github.io

## Introduction

## Code Review

## Enhancement One: Software Design and Engineering

### Repository Links
[Original Artifact](https://github.com/DakotaParker3/CS-300/tree/main)

[Updated Artifact]

## Enhancement Two: Algorithms and Data Structures

### Description
The artifact I have selected for the second enhancement in the category of algorithms and data structures is my project from CS 300 Data Structures and Algorithms that I created in August of 2025. The project was to develop a course planning application that loads course information from a CSV file into a binary search tree and allows users to view an alphanumerically sorted list of courses or search for information about an individual course. Each course contains its course ID, title, and any prerequisites associated with it.

### Justification
I selected this artifact to be enhanced and included in my ePortfolio because it provided a strong opportunity to show my ability to apply algorithms and data structures to solve a problem involving relationships between data. The original artifact already showed my understanding of a binary search tree through the insertion, searching, and in-order traversal of course data. However, the original program only displayed the immediate prerequisites of a selected course rather than every prerequisite needed. Enhancing the artifact gave me an opportunity to build on the existing data structure and create an algorithm capable of following an entire chain of prerequisites.

The primary improvement I made to the artifact was adding functionality to identify and display the complete prerequisite chain for a course. The original program’s PrintCourse function searched for the selected course and then displayed the prerequisite IDs stored in its coursePrerequisites vector, meaning that if a course required a course that then required another course, that additional prerequisite would not be displayed. I changed this by adding a recursive prerequisite chain function to the BinarySearchTree class. The function searches for a prerequisite and adds it to the list of discovered prerequisites before then recursively searching for each prerequisite that belongs to that course, allowing the program to follow prerequisite relationships until all available prerequisites are discovered. The binary search tree provided the structure for locating individual courses, while the recursive algorithm uses searches to move through the prerequisite relationships. This allows the application to display prerequisites beyond the first level, following the chain and displaying courses in the order they are discovered, offering a significant improvement over the original program because it provides a more complete representation of the requirements needed for a course.

I also added a set to track courses that have already been visited during the prerequisite traversal. The visitedCourses set is passed through each recursive call and is checked before processing a course. If a course has already been visited, the function stops processing that course instead of searching through it again, preventing the same prerequisite from being added multiple times. It also provides protection against an accidental circular prerequisite relationship causing the recursive function to continue indefinitely. Using a set for this purpose gave me experience considering not only the primary algorithm but also how a supporting data structure can improve the reliability of that algorithm.

To make this new functionality easier to use, I added a DisplayPrerequisiteChain function that handles the process of searching for the requested course, creating the tracking structures, collecting the prerequisites, and displaying the results. The existing PrintCourse function was then simplified so that it converts the user’s input to uppercase and calls this new function. This separates the user interface from the logic responsible for calculating the prerequisite chain and makes the new functionality easier to understand and maintain. I also made a small improvement to the CSV data-loading process. The original program added every value after the course title to the prerequisite vector, including empty values that could occur when a course didn’t have a prerequisite. The enhanced version of the program now checks whether each prerequisite token is empty before adding it to the vector. This keeps the stored course data cleaner and prevents empty prerequisite entries from being treated as actual prerequisites.

The existing binary search tree was also an important aspect of the enhancement. The original program already made use of a binary search tree to store courses and provided recursive insertion and in-order traversal. Rather than replacing it, I retained this data structure because it is well suited to organizing the courses by their IDs and locating individual courses through a search function. The prerequisite enhancement builds on this existing structure by repeatedly using the tree’s search operation as the recursive algorithm follows relationships between courses, allowing me to demonstrate how algorithms and data structures can work together to solve a more complex problem.

### Course Outcomes
The enhancements I planned in Module One were meant to show skills in binary search trees, tree traversal, recursion, searching, and algorithm design. The recursive prerequisite search was planned to expand the existing use of the binary search tree by allowing the program to follow the relationships between courses, while tracking visited courses would allow the program to account for duplicate or circular relationships and prevent unnecessary processing. These enhancements were planned to align with outcomes one, three, four, and five.

I believe I successfully achieved these course outcomes noted in my Module One plan. The enhancement supports outcome one, employing strategies for building collaborative environments, by making prerequisite information easier to understand and use when students or advisors need to make course planning decisions. The original program could show the prerequisites directly required by a course, but didn’t show the additional courses required by that prerequisite. Displaying the complete prerequisite chain provides more useful information to users as they can see the sequence of courses that may need to be completed rather than having to search for each prerequisite individually. Additionally, separating the user interface from the logic responsible for calculating the prerequisite chain allows for better readability and reusability that potential collaborators could make use of.

The enhancement most directly supports outcome three, which focuses on designing and evaluating computing solutions using algorithmic principles and data structures. The recursive prerequisiteChain function required me to design an algorithm that could follow relationships between courses and continue searching until the available prerequisite chain had been processed. The binary search tree provides the data structure used to locate courses, while the recursive algorithm determines how those courses should be processed. This enhancement gave me experience considering how different components of an algorithm work together to solve a computing problem.

Outcome four is also supported through the use of C++, binary search trees, recursion, vectors, and sets to expand an existing computing solution. Instead of replacing the original program, I built on its existing functionality and reused the search method of the binary search tree within the new prerequisite algorithm. This allowed me to improve the value of the application while maintaining its original course loading and searching functionality. The enhancement also supports outcome five by considering unexpected or problematic relationships within the course data. The visitedCourses set prevents a course from being processed repeatedly when it appears in multiple prerequisite paths and also prevents the algorithm from continuously following a circular relationship if one is present. I also modified the CSV loading process so that empty prerequisite values aren’t added to a course’s prerequisite vector, keeping the data much cleaner. These changes reduce the possibility of unexpected data affecting the application and make the program more reliable.

### Reflection

Working on enhancing this artifact gave me a better understanding of how algorithms and data structures work together to solve problems. When I originally created the project, I understood the binary search tree primarily as a way to store and search for courses and understood recursion as a technique used by functions such as addNode and inOrder. Upon revisiting the project to expand on its functionality, I have been able to look at these concepts differently and understand how they come together. Rather than just storing course information, the enhanced program uses the binary search tree and its search functionality as part of an algorithm that can follow relationships between courses, for example.

One of the most important things I learned was how recursion can be used to process data when the number of steps depends on the relationships within that data. The original project already used recursion for inserting nodes and performing an in-order traversal, but the prerequisiteChain function required me to use recursion to follow relationships between courses. When the function finds a prerequisite for a course, that prerequisite can have its own prerequisites so instead of manually searching through each level, the function calls itself using the course that was just found. That new call then searches for the prerequisites of that course and repeats the process for any additional courses it discovers until a course has no more prerequisites to follow. This helped me better understand how recursion can be used to solve a problem where the number of steps can’t be known ahead of time as each result can lead to another related result.

Another important part of the process was learning to consider what could happen when the algorithm encounters the same course more than once. Without tracking visited courses, a prerequisite that appeared through multiple paths could be added to the results more than once, which can both clutter the results and potentially lead to a circular relationship that would cause the recursive function to continue indefinitely. Adding the visitedCourses set allowed me to account for these situations by checking whether a course had already been processed before continuing the search. This helped instill the importance of considering how the algorithm should behave when the data contains unexpected relationships, as designing an algorithm involves more than making it work with just the expected input.

### Repository Links
[Original Artifact](https://github.com/DakotaParker3/CS-320/tree/main)

[Updated Artifact]

## Enhancement Three: Databases

### Repository Links
[Original Artifact](https://github.com/DakotaParker3/cs465-fullstack/tree/module7)

[Enhanced Artifact](https://github.com/DakotaParker3/cs465-fullstack/tree/update1)
