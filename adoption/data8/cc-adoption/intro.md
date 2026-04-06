# Community College(and smaller institutions) Adoption

Under [Cloudbank](https://www.cloudbank.org/) and with funding from [NSF](https://www.nsf.gov/), we are offering a resources to teach Data Science courses including the full set of materials used to teach Data-8 at Berkeley.

There are a series of steps needed to acquire the materials and solutions as well as to gain access to the compute needed for your students and finally, access to our automatic grading system.

You can expect the following:
- The Jupyter Notebooks for labs, homeworks, and projects
- The solutions to all the Jupyter Notebooks
- Lecture Slides and Videos of each lecture
- Worksheets(and solutions) used in the discussion/lab sessions
- A Canvas template customized to use the JupyterHub for your institution
- Access to a JupyterHub instance for your institution configured to your campus Single Sign-on or options
- Access to a grading service that will grade your students notebooks and return the grades in an CSV file

Your institution may need documentation related to privacy(HECVAT) and accessibility(VPAT):
- Here is a [HECVAT](https://docs.google.com/spreadsheets/d/18_Q1b0tisNkQeyj1ibEuvq2Nq7DIF99v/edit?gid=1214776280#gid=1214776280) outlining what student information is needed(just an email address) and how it is protected.
- Accessibility is on-going effort at UC Berkeley and within the Jupyter Community:
    - This [document](https://jupyter-accessibility.readthedocs.io/en/latest/resources/JupyterLab-a11y-statement.html) outlines the current state of Jupyter with regards to accessibility
    - An [extension](https://a11y.datahub.berkeley.edu/) to JupyterHub is being created assess the accessibility of notebooks

**Step 1:**  Privacy Agreement and General Information

We ask that anyone using these materials do not distribute solutions. We also need a GitHub username in order to give you access to the solutions, if you do not have one please create one [here](https://github.com)

Then, complete this [form](https://forms.gle/3gbJQcQNKkYfbW2S7)

We need a few pieces of information about your institution in order to configure the computing environment for your students. Please complete this [form](https://forms.gle/aj2KVirKRFMcQGzd6) as well.

**Step 2:** Create a copy of the student materials for yourself

[Screen Recording](https://drive.google.com/file/d/1OODEHdngTajW_kRKTMrVZw9nS4_iiZrq/view?usp=drive_link)

After you have created a GitHub username, please login and then "Fork" this [repo](https://github.com/data-8/materials-fds)

**Step 3:** Accepting the GitHub Repository Invitations

You are going to be added to the materials-fds-private solutions and resources repository as well as the Otter Service Standalone GitHub Organization used to grade your students notebooks.

You can accept the invitations by clicking each of these links:
- Solutions Repository: [materials-fds-private](https://github.com/data-8/materials-fds-private)
- Automatic Grading System(Otter Service Standalone): [otter-service-stdalone](https://github.com/orgs/otter-service-stdalone)

**Step 4:** Canvas Shell and Course Website

Here is a [screen recording](https://drive.google.com/file/d/1rBG97FUwMdV3QQas7znuH8pud-KC8yPM/view?usp=drive_link) of what you need to do to configure the Canvas shell we have set up for you.

You can download the Canvas template [here](https://drive.google.com/file/d/167mhYuq3msva3TO3agFr2jVlPMuzcusw/view?usp=drive_link)

**Updating assignment links for your JupyterHub**

The default template links assignment URLs to datahub.berkeley.edu. If your institution uses a different JupyterHub (e.g., your campus hub), you need to rewrite those links before importing. Use the [Canvas JupyterHub rewriter](https://ds-modules.github.io/canvas-jupyterhub-rewriter/) to update the zip or .imscc file:

1. **Upload** your Canvas template (zip or .imscc file) to the rewriter.
2. **Enter your JupyterHub URL** (e.g., `datahub.berkeley.edu/hub` or your institution’s hub URL).
3. **Enter the materials repository URL** — for Data 8, use `https://github.com/data-8/materials-fds`.
4. **Scan and preview** to see how links will change.
5. **Check the preview** — confirm that old links (e.g., pasadena.cloudbank.org) are being rewritten to your hub and that the repo points to `data-8/materials-fds`.
6. **Rewrite and download** the updated file, then import that file into Canvas.

[Video: Jupyter rewriter walkthrough](https://www.youtube.com/watch?v=xbvQF5HmwUw)

**Uploading the IMCC file to Canvas**

Once you have the rewritten .imscc file from the Jupyter rewriter, import it into Canvas:

1. **Create a new course** (or use an existing one) — Settings → Start a new course, name it (e.g., "Data 8 example").
2. **Go to Import course content** — In your Canvas course, open the course menu and select Import Course Content.
3. **Select Common cartridge 1.x package** as the content type.
4. **Upload** the rewritten .imscc file you downloaded from the rewriter.
5. **Choose import options** — For a fresh course, you can upload all content. If you have existing content, you can select specific content, adjust due dates, or choose to overwrite matching assessments.
6. **Wait for the import** — The status will show "queued" then "running" with a progress bar. This may take a minute or two.
7. **Verify the links** — After import, click on an assignment (e.g., Homework 1) and check the link in the bottom-left corner of your browser. It should show your JupyterHub URL (e.g., datahub.berkeley.edu), not the original template hub. Click through to confirm the notebook loads correctly.

[Video: Uploading IMCC to Canvas](https://www.youtube.com/watch?v=tsi-z_cf8Pc)

We can help you with this process as well.

This [week-to-week layout](https://www.data8.org/materials-fds/demo.html) mirrors the Canvas Course layout as well. It is a good resource to get an overview of the course as well explore alternative platforms to render Jupyter Notebooks.

**Step 5:** The Student Workflow

[Screen Recording](https://drive.google.com/file/d/1flQlOZ6ViM0S7S0k0-ZLFZsFNY5ZXMON/view?usp=drive_link)

Here is a summary of the student workflow depicted in the recording:
- Log into your Canvas course/course web page.
- Click on the link for the homework, lab or project
- Another tab opens, and the notebook they have chosen renders in Jupyter Notebook
- The student works through the notebook checking their answers as they go.
- When finished, the student downloads the notebook using the "export" cell at the bottom.
- The downloaded files are uploaded to the correct Canvas assignment or where ever you normally have work submitted.

**Step 6:** Instructor Grading Workflow

[Screen Recording](https://drive.google.com/file/d/1-r1kuUutn7ZXl3lSUgBbZAxLFuHoeFPp/view?usp=drive_link)

- Student Assignments: After the students have submitted their work, you download all the assignments onto your machine
- Solutions: Log into the GitHub repo, [materials-fds-private](https://github.com/data-8/materials-fds-private), navigate to the autograder_zips folder and find the autograder.zip file of the assignment you are grading, download it.
- Automatic Grading: Log into [grader.datahub.berkeley.edu](https://grader.datahub.berkeley.edu) with your GitHub username, and follow instructions in the screen recording above.
- If you would like to test run the grader you can use these archives:
    - [Sample HW 08 Submissions (hw-8-submissions.zip)](hw-8-submissions.zip)
    - [HW 08 Solution file (autograder.zip)](autograder.zip)
