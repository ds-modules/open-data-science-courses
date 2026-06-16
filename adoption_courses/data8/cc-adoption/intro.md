# Community College (and smaller institutions) Adoption

Under [Cloudbank](https://www.cloudbank.org/) and with funding from [NSF](https://www.nsf.gov/), we offer resources to teach Data Science courses, including the full set of materials used to teach Data 8 at Berkeley.

There are a series of steps needed to acquire the materials and solutions, gain access to compute for your students, and set up our automatic grading system.

You can expect the following:

- The Jupyter Notebooks for labs, homeworks, and projects
- The solutions to all the Jupyter Notebooks
- Lecture slides and videos of each lecture
- Worksheets (and solutions) used in discussion and lab sessions
- A Canvas template customized to use JupyterHub for your institution
- Access to a JupyterHub instance for your institution, configured to your campus single sign-on or other options
- Access to a grading service that grades student notebooks and returns grades in a CSV file

Your institution may need documentation related to privacy (HECVAT) and accessibility (VPAT):

- Here is a [HECVAT](https://docs.google.com/spreadsheets/d/18_Q1b0tisNkQeyj1ibEuvq2Nq7DIF99v/edit?gid=1214776280#gid=1214776280) outlining what student information is needed (just an email address) and how it is protected.
- Accessibility is an ongoing effort at UC Berkeley and within the Jupyter community:
  - This [document](https://jupyter-accessibility.readthedocs.io/en/latest/resources/JupyterLab-a11y-statement.html) outlines the current state of Jupyter with regard to accessibility
  - An [extension](https://a11y.datahub.berkeley.edu/) to JupyterHub is being created to assess the accessibility of notebooks

## Choose your adoption version

We offer two adoption packages. Both use the same adoption workflow below; the main differences are which materials repository and Canvas template you use.

| | **Version 1** | **Version 2 (recommended)** |
| --- | --- | --- |
| **Materials repo** | [materials-fds](https://github.com/data-8/materials-fds) | [materials-fds-v2](https://github.com/data-8/materials-fds-v2) |
| **Semester basis** | Spring 2022 and earlier adoption track | Fall 2025 |
| **Worksheets** | Discussion/lab worksheets (via private repo) | Tutoring worksheets now included in the adoption package |
| **Assignments** | Original datasets | Updated datasets on assignments |
| **Curriculum** | Classic Data 8 sequence | Introduces **multiple linear regression** |
| **Canvas shell** | Original template | UI improvements and an accessibility (a11y) pass |

```{tip}
**Which version should I choose?**

- **New adopters:** Use **Version 2** (`materials-fds-v2`) for the most current Fall 2025 materials, updated assignments, and improved Canvas experience.
- **Returning adopters:** Stay on **Version 1** (`materials-fds`) if you are already running that track and want continuity. You can migrate to Version 2 when you are ready.
```

Throughout this guide, look for **Version 1** and **Version 2** callouts where steps differ.

## Step 1. Privacy agreement and general information

*Estimated time: 15–30 minutes*

We ask that anyone using these materials do not distribute solutions. We also need a GitHub username to give you access to the solutions; if you do not have one, please create one [here](https://github.com).

Then, complete this [form](https://forms.gle/3gbJQcQNKkYfbW2S7). Indicate which adoption version you plan to use so we can grant access to the correct resources.

We need a few pieces of information about your institution in order to configure the computing environment for your students. Please complete this [form](https://forms.gle/aj2KVirKRFMcQGzd6) as well.

## Step 2. Fork the student materials

*Estimated time: 5–10 minutes*

[Screen recording: forking the repository](https://drive.google.com/file/d/1OODEHdngTajW_kRKTMrVZw9nS4_iiZrq/view?usp=drive_link)

After you have created a GitHub username, log in and **Fork** the repository for your chosen version:

- **Version 1:** [materials-fds](https://github.com/data-8/materials-fds)
- **Version 2:** [materials-fds-v2](https://github.com/data-8/materials-fds-v2)

## Step 3. Accept GitHub repository invitations

*Estimated time: 5 minutes*

```{warning}
We ask that anyone using these materials do not distribute solutions. This protects the integrity of the course materials for all institutions.
```

You will be added to the private solutions repository and to the Otter Service Standalone GitHub organization used to grade student notebooks. Accept the invitations by clicking each of these links:

- **Solutions repository:** [materials-fds-private](https://github.com/data-8/materials-fds-private) (solutions for both adoption versions)
- **Automatic grading system (Otter Service Standalone):** [otter-service-stdalone](https://github.com/orgs/otter-service-stdalone)

## Step 4. Canvas shell and course website

*Estimated time: 1–2 hours (depending on customization)*

[Screen recording: configuring the Canvas shell](https://drive.google.com/file/d/1rBG97FUwMdV3QQas7znuH8pud-KC8yPM/view?usp=drive_link)

We can help you with this process as well.

### Download the Canvas template

Download the template for your adoption version:

- **Version 1:** [Canvas template (materials-fds)](https://drive.google.com/file/d/167mhYuq3msva3TO3agFr2jVlPMuzcusw/view?usp=drive_link)
- **Version 2:** Use the Fall 2025 Canvas template provided after you complete the adoption form (updated layout, tutoring worksheets, and accessibility improvements). Contact [ds-help@berkeley.edu](mailto:ds-help@berkeley.edu) if you need the link again.

### Point assignments at your JupyterHub

The default template links assignment URLs to datahub.berkeley.edu. If your institution uses a different JupyterHub (for example, your campus hub), use the [Canvas JupyterHub rewriter](https://ds-modules.github.io/canvas-jupyterhub-rewriter/) to update the zip or .imscc file **before** importing:

- Upload your Canvas template (zip or .imscc file) to the rewriter
- Enter your JupyterHub URL (e.g., `datahub.berkeley.edu/hub` or your institution's hub URL)
- Enter the materials repository URL for your version:
  - **Version 1:** `https://github.com/data-8/materials-fds`
  - **Version 2:** `https://github.com/data-8/materials-fds-v2`
- Scan and preview to see how links will change
- Confirm that old links are being rewritten to your hub and that the repo points to the correct repository (`data-8/materials-fds` or `data-8/materials-fds-v2`)
- Rewrite and download the updated file

#### Video: JupyterHub rewriter

:::{iframe} https://www.youtube.com/embed/xbvQF5HmwUw
:width: 100%

:::

### Import into Canvas

We recommend importing the cartridge into a **new** Canvas course. After the first import, **copy that course inside Canvas** from term to term instead of re-importing the cartridge into an existing shell (re-importing can duplicate items that do not share the same internal IDs).

- Create a new course — Settings → Start a new course, name it (e.g., "Data 8")
- Go to **Import Course Content** from the course menu
- Select **Common cartridge 1.x package** as the content type
- Upload the .imscc file (the rewritten file from the rewriter step, or the original template if using datahub.berkeley.edu)
- Upload **all** content for this initial import
- Wait for the import — Status will show "queued" then "running" with a progress bar
- **Verify the links** — After import, click on an assignment (e.g., Homework 1) and check the link in the bottom-left corner of your browser. It should show your JupyterHub URL. Click through to confirm the notebook loads correctly

#### Video: Uploading the Canvas template

:::{iframe} https://www.youtube.com/embed/tsi-z_cf8Pc
:width: 100%

:::

```{note}
**What's in the Canvas shell**

The Canvas shell includes:

- Reading assignments embedded as quizzes (ensures student engagement)
- Week-by-week course structure
- Pre-configured assignment links
- Gradebook setup

**Version 2** adds tutoring worksheets, updated assignment datasets, and UI and accessibility improvements to this structure.
```

### Course calendar overview

These week-to-week layouts mirror the Canvas course layout and are useful for getting an overview of the course and exploring alternative platforms to render Jupyter notebooks:

- **Version 1:** [materials-fds demo calendar](https://www.data8.org/materials-fds/demo.html)
- **Version 2:** [Fall 2025 course site](http://data8.org/fa25/)

## Step 5. Student workflow

*Review this before your first class*

[Screen recording: student workflow](https://drive.google.com/file/d/1flQlOZ6ViM0S7S0k0-ZLFZsFNY5ZXMON/view?usp=drive_link)

Here is how students will interact with assignments:

1. **Access:** Students log into Canvas and click on an assignment link
2. **Open notebook:** The notebook opens in JupyterHub (in a new tab)
3. **Work:** Students complete the notebook, checking answers as they go
4. **Export:** Students use the "export" cell at the bottom to download their completed notebook
5. **Submit:** Students upload the downloaded file to Canvas

## Step 6. Instructor grading workflow

*Estimated time: 5–10 minutes per assignment (after initial setup)*

[Screen recording: grading workflow (5 min)](https://drive.google.com/file/d/1-r1kuUutn7ZXl3lSUgBbZAxLFuHoeFPp/view?usp=drive_link)

1. **Download student submissions:** Export all submissions from Canvas onto your machine
2. **Get solutions:** Log into [materials-fds-private](https://github.com/data-8/materials-fds-private), navigate to the `autograder_zips` folder, and download the `autograder.zip` file for the assignment you are grading
3. **Grade automatically:** Log into [grader.datahub.berkeley.edu](https://grader.datahub.berkeley.edu) with your GitHub username and follow the instructions in the screen recording above
4. **Import grades:** Upload the CSV file with grades back to Canvas

If you would like to test run the grader, you can use these archives:

- [Sample HW 08 Submissions (hw-8-submissions.zip)](hw-8-submissions.zip)
- [HW 08 Solution file (autograder.zip)](autograder.zip)

For more detail, see the [Grading section](../grading/intro.md).

**Need more help?** Contact us at [ds-help@berkeley.edu](mailto:ds-help@berkeley.edu)
