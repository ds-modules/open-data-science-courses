# Grading

This section covers grading approaches and tools used in Data 6.

## Overview

Data 6 uses a combination of automated and manual grading to provide timely feedback to students while ensuring quality assessment. 

```{tip}
**Three Grading Options**

There are three main ways to grade otterized notebooks:

- [Otter Service Standalone](#otter-service-standalone) - Web-based, easiest to get started
- [GradeScope](#grading-with-gradescope) - Paid service with Canvas integration
- [Grading Locally](#grading-locally) - Full control, requires local setup
```

## Automated Grading

The primary tool for automated grading in Data 6 is Otter, which can grade Jupyter notebooks automatically. Otter supports:

- Code execution and output checking
- Test-based grading
- Manual grading components
- Grade export to CSV

## Grading Workflow

The typical grading workflow involves:

1. **Assignment Distribution**: Assignments are distributed to students through JupyterHub or the course website
2. **Student Submission**: Students complete assignments and submit them through Canvas or another LMS
3. **Automated Grading**: Otter grades the submissions automatically
4. **Grade Export**: Grades are exported to CSV format
5. **Grade Upload**: Grades are uploaded to the LMS

## Manual Grading

Some components of assignments may require manual grading, such as:
- Written responses
- Code style and documentation
- Project presentations

## Otter Service Standalone

```{tip}
**Recommended for Most Users**

The Otter Service Standalone is a web-based service for grading notebooks - no local installation required! The service is available at [https://grader.datahub.berkeley.edu/](https://grader.datahub.berkeley.edu/)

[Screen Recording Tutorial (5 min)](https://drive.google.com/file/d/1-r1kuUutn7ZXl3lSUgBbZAxLFuHoeFPp/view?usp=sharing)
```

**Step 1:** Authorization

In order to access the service, we need to add your GitHub username to our otter service organization. Once you have been added and accepted the invitation by clicking [here](https://github.com/orgs/otter-service-stdalone) you can use the grader service by logging into your GitHub account.

**Step 2:** Download your student submissions

You can grade a folder of notebooks by compressing the folder into a zip file and then uploading that zip file or you can grade one notebook at a time by uploading the notebook itself.

**Step 3:** Download solution files (autograder.zip)

If you visit the private solutions repository (access provided after completing the [Instructor Interest Form](https://forms.gle/2nNtbfgBtNsUHypCA)), and browse to the folder `autograder_zips`, you will find the solutions to your assignment. Download the autograder.zip file for the assignment you are grading.

If you do not have access to this repository, please complete the [Instructor Interest Form](https://forms.gle/2nNtbfgBtNsUHypCA) or email us at [data6@berkeley.edu](mailto:data6@berkeley.edu) for access.

**Step 4:** Upload the student notebooks and autograder.zip to the service

In the "Grade" section, upload your autograder.zip and the student submissions from the previous step and press the "Grade Notebooks" button.

After you press the "Grade Notebooks" button, a "download" code appears under the button. You will need this code for the next step.

**Step 5:** Downloading your results

```{note}
**Processing Time**

At this point, you have to wait for the notebooks to be graded. The system takes about one minute per ten notebooks but this can vary.
```

Once you have waited, you will enter the code from Step 4 into the "Results" section on the right-side of the page and a folder with a log file and csv file will be downloaded. The csv file contains the grades by notebook. 

```{tip}
**Troubleshooting**

If you have problems, the log file may indicate what the problem is. Check the log file first before contacting support.
```

## Grading with GradeScope

```{important}
**Paid Service Required**

GradeScope is a **paid** service that allows instructors to tie assignments back to Canvas. Your institution will need a GradeScope license.
```

**Step 1: Institutional License, GradeScope and Canvas**

Once an assignment is created in Canvas and in GradeScope, a student uploads their completed notebook to GradeScope, GradeScope grades the notebook and pushes the scores back to the LMS.

**Step 2: Documentation: Canvas and GradeScope Assignment Configuration**

This documentation from [GradeScope](https://help.gradescope.com/article/y10z941fqs-instructor-canvas) details how to configure a GradeScope course and assignments with Canvas.

**Step 3: Documentation: GradeScope Programming Assignments**

This documentation from [GradeScope](https://help.gradescope.com/article/ujutnle52h-instructor-assignment-programming) illustrates how to tie the autograder.zip file to a GradeScope assignment to enable automatic grading. There is also a section on combining manual and autograded questions.

```{tip}
**Quick Setup**

We have all the autograder.zip files needed for the programming assignments, so the configuration of these assignments should be very straightforward.
```

## Grading Locally

You can grade notebooks on your own machine. The configuration and packages you need to install otter-grader are detailed in the documentation:

- [Installation of otter-grader](https://otter-grader.readthedocs.io/en/latest/index.html#installation)

```{important}
**Version Requirement**

Data 6 notebooks are configured with otter-grader version 6.1.6, so when you install otter-grader you must install version 6.1.6.
```

Install the required version using:

```bash
pip install otter-grader==6.1.6
```

You will also need to install Docker:
- [Installation of Docker](https://otter-grader.readthedocs.io/en/latest/index.html#docker)

Once you have installed the components above, we recommend you move through this [tutorial](https://otter-grader.readthedocs.io/en/latest/tutorial.html). The final step illustrates how to grade.

Finally, the [command line reference](https://otter-grader.readthedocs.io/en/latest/cli_reference.html#otter-grade) for the command `otter grade` details the various options you have related to grading.

## Grade Management

Grades are typically managed through your institution's LMS (Canvas, etc.), with automated grades imported from the grading system.

For more information about setting up grading infrastructure, see the [Infrastructure section](../infrastructure/infrastructure.md).

