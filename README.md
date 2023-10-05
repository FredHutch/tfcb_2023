# MCB 536: Tools for Computational Biology

This document is the syllabus for this course.


- [MCB 536: Tools for Computational Biology](#mcb-536-tools-for-computational-biology)
  - [Class schedule](#class-schedule)
  - [Homework and grading](#homework-and-grading)
  - [Course description](#course-description)
  - [Resources and required materials](#resources-and-required-materials)
  - [Instructors](#instructors)
  - [Teaching Assistants](#teaching-assistants)

## Class schedule

Time: 3:30PM-4:50PM, Tue & Thu, Sep 28 - Dec 5 2023

Class Location: B1-072/074 (Weintraub Building, Fred Hutch SLU campus)

TA Office Hours: 11:00am-12:00pm Wed (Nashwa) 2:00pm-3:00pm Thu (Sarah)

TA Office Hours Location: Zoom (see Slack) or 2nd floor of Steam Plant @ Fred Hutch room S2-135

| Lecture | Date   | Instructor          | Topic                                                                                         |
| ------- | ------ | ------------------- | --------------------------------------------------------------------------------------------- |
| 1       | Sep 28 | Rasi Subramaniam    | [Introduction to Computational Biology and course](lectures/lecture01/)                       |
| 2       | Oct 3  | TA-led              | [Software installation and troubleshooting](software/README.md)                               |
| 3       | Oct 5  | Rasi Subramaniam    | [Introduction to VScode, Version Control, Data and project organization](lectures/lecture03/) |
| 4       | Oct 10 | Melody Campbell     | [Introduction to the command line](lectures/lecture04/)                                       |
| 5       | Oct 12 | Melody Campbell     | [Intro to the command line (continued)](lectures/lecture05/)                                  |
| 6       | Oct 17 | Phil Bradley        | [Introduction to Python](lectures/lecture06/)                                                 |
| 7       | Oct 19 | Phil Bradley        | [Intro to Python (continued)](lectures/lecture07/)                                            |
| 8       | Oct 24 | Maggie Russell      | [Data structures and biological analyses using Python](lectures/lecture08/)                   |
| 9       | Oct 26 | Maggie Russell      | [Data structures/biological analyses in Python (continued)](lectures/lecture09)               |
| 10      | Oct 31 | Phil Bradley        | [Modeling and machine learning in Python](lectures/lecture10)                                 |
| 11      | Nov 2  | Phil Bradley        | [Modeling/machine learning in Python (continued)](lectures/lecture11)                         |
| 12      | Nov 7  | Rasi Subramaniam    | [Data analysis using R/tidyverse](lectures/lecture12/)                                        |
| 13      | Nov 9  | Rasi Subramaniam    | [Data analysis using R/tidyverse (continued)](lectures/lecture13/)                            |
| 14      | Nov 14 | Elizabeth Humphries | [Introduction to sequencing data](lectures/lecture14/)                                        |
| 15      | Nov 16 | Elizabeth Humphries | [Genomic data in R](lectures/lecture15/)                                                      |
| 16      | Nov 21 | Elizabeth Humphries | [Biological sequences and annotations in Bioconductor](lectures/lecture16/)                   |
| 17      | Nov 28 | Maggie Russell      | [Immune repertoire sequencing and analysis](lectures/lecture17/)                              |
| 18      | Nov 30 | Manu Setty          | [Single-cell RNA-seq analysis](lectures/lecture18/)                                           |
| 19      | Dec 5  | Manu Setty          | [Single-cell RNA-seq analysis (continued)](lectures/lecture19/)                               |

Materials for each lecture will be available in this repository prior to the class session;
the link for each topic will take you to the folder containing materials for that class.
Please note that materials are considered in draft form until the beginning of the class session in which they will be presented (or if otherwise indicated).

For further assistance, TAs TBD will be available to offer assistance just after the regular class session.

## Homework and grading

- A total of 8 homework assignments will be assigned on the following dates and will be due at 1pm on the dates indicated.
  If you need to submit a homework late, please check with the instructor at least 24 hours before the due date.
- Grading criteria and instructions for submission are available in the [Canvas](http://canvas.uw.edu) site for this class.
- Submit homework solutions as Markdown text files, scripts, or PDF as appropriate for each homework through Canvas.
- You are encouraged to search online for solutions and discuss the homework with your classmates.
  However, the answers you submit should be written in your own words.
  You should also cite any online source or person that helped you arrive at your solution as inline comments in your code.
- Each homework will count for 10% of your final grade. In-class participation will count for the remaining 20%, and will be assessed from the rubric presented [here](lectures/lecture01/participation_rubric.md).
- If you have a question about homework, please post it in the Slack workspace for this course (preferred) or message an instructor directly.

| Homework | Assigned Date | Due Date | Topic                                                                  |
| -------- | ------------- | -------- | ---------------------------------------------------------------------- |
| 1        | Oct 5         | Oct 12   | [Reproducible science, Git and GitHub, Markdown](homeworks/homework01) |
| 2        | Oct 12        | Oct 19   | [Unix command line](homeworks/homework02)                              |
| 3        | Oct 19        | Oct 26   | [Programming in Python](homeworks/homework03)                          |
| 4        | Oct 26        | Nov 2    | [Python analysis](homeworks/homework04)                                |
| 5        | Nov 2         | Nov 9    | [Modeling and machine learning in Python](homeworks/homework05)        |
| 6        | Nov 9         | Nov 16   | [Data visualization and manipulation in R](homeworks/homework06)       |
| 7        | Nov 21        | Nov 30   | [Genomic data in R](homeworks/homework07)                              |
| 8        | Nov 30        | Dec 7    | [Single-cell RNA-seq analysis](homeworks/homework08)                   |

## Course description

This course is designed to introduce computational research methods to graduate students in biomedical science and related disciplines.
We expect students will have little to no previous experience in computational methods.
This course provides a survey of the most common tools in the field and you should not expect that completion of the course will make you an expert in any single programming language.
Rather, you should be equipped with foundational knowledge in reproducible computational science, and can continue learning relevant tools to suit your research interests.

**Course objectives:** By the end of the course, students should be able to:

- Code in R, Python, and Unix/bash shell scripting using appropriate syntax and code convention
- Select appropriate tools to perform specific programming and data analysis tasks
- Apply good practices for computational research, including project organization and documentation
- Analyze common forms of data generated by molecular biology experiments including high throughput sequencing,
  flow cytometry, and 96-well plate readers.

## Resources and required materials

- This course will require a laptop computer, on which you should install the [required software](software/README.md).
- Additional reading material is available [for your reference](reference.md).
- If you are a UW student who does not possess a prior affiliation with Fred Hutch: We will request a HutchNetID for you,
  which will allow access to computational resources used for this class (please note that this process
  requires a background check).
- Information about expectations for student conduct, disability resources, academic integrity, and religious
  accommodations can be found on [this page](https://registrar.washington.edu/staffandfaculty/syllabi-guidelines/).

## Instructors

For general inquiries about this course or add codes, please contact GraduateEducation@FredHutch.org

- [Phil Bradley](https://www.fredhutch.org/en/labs/profiles/bradley-phil.html)
- [Melody Campbell](https://www.fredhutch.org/en/faculty-lab-directory/campbell-melody.html)
- [Elizabeth Humphries](https://www.linkedin.com/in/elizabeth-humphries-61202a103/)
- [Maggie Russell](https://www.linkedin.com/in/magdalena-russell/)
- [Manu Setty](https://research.fredhutch.org/setty/en.html)
- [Arvind Rasi Subramaniam](http://rasilab.fredhutch.org)

## Teaching Assistants

- Nashwa Ahmed 
- Sarah Huang
