# Technical Infrastructure

This section covers the technical infrastructure needed to run Data 6 at your institution.

## Overview

Running Data 6 requires several technical components:

- **JupyterHub**: For providing students with access to Jupyter notebooks
- **Grading infrastructure**: For automated grading of assignments
- **Course website**: For hosting course materials and notes
- **Version control**: For managing course materials (typically GitHub)

## JupyterHub

JupyterHub allows students to access Jupyter notebooks through a web browser without needing to install software on their own computers. This is essential for ensuring all students have access to the same computing environment.

Key considerations:
- Integration with your institution's authentication system (SSO)
- Resource allocation (CPU, memory, storage)
- Backup and data persistence
- Accessibility compliance

## Grading Infrastructure

Data 6 uses automated grading systems to provide timely feedback to students. The primary tool used is Otter, which can grade Jupyter notebooks automatically.

Key considerations:
- Integration with your LMS (Canvas, etc.)
- Grade export capabilities
- Security and privacy of student data

## Course Website

The course website hosts:
- Course notes (online textbook)
- Syllabus and schedule
- Assignment links
- Other course materials

The Data 6 course notes are built using Quarto and hosted on GitHub Pages.

## Getting Help

For more detailed technical information, see ["The Data Science Educator's Guide to Technical Infrastructure"](https://ucbds-infra.github.io/ds-course-infra-guide/intro.html).

If you need help setting up infrastructure at your institution, please contact [data6@berkeley.edu](mailto:data6@berkeley.edu).

