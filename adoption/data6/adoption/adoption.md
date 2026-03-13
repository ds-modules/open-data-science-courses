# Course Adoption Guide

Under [Cloudbank](https://www.cloudbank.org/) and with funding from [NSF](https://www.nsf.gov/), we are offering resources to teach Data Science courses including the full set of materials used to teach Data 6 at Berkeley.

This guide walks you through the step-by-step process of adopting Data 6 at your institution.

## Prerequisites Checklist

Before starting, make sure you have:

- [ ] A GitHub account ([create one here](https://github.com) if needed)
- [ ] Institutional approval to use external course materials
- [ ] Contact information for your IT department (for JupyterHub setup)
- [ ] Access to your institution's LMS (Canvas or similar)
- [ ] Commitment to not distribute solutions publicly

## Adoption Timeline

```{note}
**Expected Timeline**

- **Week 1:** Complete forms, get repository access, fork materials
- **Week 2:** Set up JupyterHub (if needed), configure Canvas
- **Week 3:** Test grading infrastructure, customize materials
- **Week 4:** Final testing and preparation for students

*Timeline may vary based on your institution's IT processes.*
```

```{note}
**What You'll Receive**

You can expect the following:
- The Jupyter Notebooks for labs, homeworks, and projects
- The solutions to all the Jupyter Notebooks
- Lecture slides for each lecture
- Worksheets (and solutions) used in the discussion/lab sessions
- A Canvas template customized to use the JupyterHub for your institution
- Access to a JupyterHub instance for your institution configured to your campus Single Sign-on or options
- Access to a grading service that will grade your students notebooks and return the grades in a CSV file
```

```{important}
**Institutional Requirements**

Your institution may need documentation related to privacy (HECVAT) and accessibility (VPAT):
- Here is a [HECVAT](https://docs.google.com/spreadsheets/d/18_Q1b0tisNkQeyj1ibEuvq2Nq7DIF99v/edit?gid=1214776280#gid=1214776280) outlining what student information is needed (just an email address) and how it is protected.
- Accessibility is an on-going effort at UC Berkeley and within the Jupyter Community:
    - This [document](https://jupyter-accessibility.readthedocs.io/en/latest/resources/JupyterLab-a11y-statement.html) outlines the current state of Jupyter with regards to accessibility
    - An [extension](https://a11y.datahub.berkeley.edu/) to JupyterHub is being created to assess the accessibility of notebooks
```

**Step 1:** Privacy Agreement and General Information

*Estimated time: 15-30 minutes*

```{warning}
We ask that anyone using these materials do not distribute solutions. This protects the integrity of the course materials for all institutions.
```

1. **Create a GitHub account** (if you don't have one): [https://github.com](https://github.com)
   - We need your GitHub username to grant access to private repositories

2. **Complete the Instructor Interest Form**: [Data 6 Instructor Interest Form](https://forms.gle/2nNtbfgBtNsUHypCA)
   - This form helps us understand your needs
   - You'll receive access to solutions and resources after completion
   - Expect a response within 1-3 business days

```{tip}
**What Happens Next?**

After submitting the form, you'll receive:
- Email confirmation
- GitHub repository invitations (within 1-3 days)
- Access to private solutions repository
- Instructions for next steps
```

**Step 2:** Create a copy of the student materials for yourself

*Estimated time: 5-10 minutes*

The public student materials are available at [https://github.com/dubois-ctds/data-6-materials-student](https://github.com/dubois-ctds/data-6-materials-student).

1. **Fork the repository**: Click the "Fork" button in the top right of the repository page
   - This creates your own copy that you can customize
   - You can make changes without affecting the original

2. **Explore the materials**: Browse through labs, homeworks, and projects
   - Familiarize yourself with the structure
   - Note any materials you want to customize

```{tip}
**Why Fork?**

Forking creates your own copy of the materials. This allows you to:
- Customize content for your institution
- Keep your changes separate from the original
- Easily pull updates from the original repository
```

**Step 3:** Accepting the GitHub Repository Invitations

*Estimated time: 5 minutes*

After completing the Instructor Interest Form, you will be added to private solutions and resources repositories as well as any grading infrastructure needed for your students.

1. **Check your email**: You'll receive GitHub invitation emails
2. **Accept invitations**: Click "Accept" on each invitation
   - Private solutions repository
   - Grading infrastructure organization (if applicable)
3. **Verify access**: You should now see private repositories in your GitHub account

```{tip}
**Can't Find the Invitations?**

- Check your email spam folder
- Check your GitHub notifications (bell icon)
- If you don't receive invitations within 3 days, email us at [data6@berkeley.edu](mailto:data6@berkeley.edu)
```

**Step 4:** Canvas Shell and Course Website

*Estimated time: 1-2 hours (depending on customization)*

We can help you configure the Canvas shell we have set up for you.

1. **Download the Canvas template**: [Canvas Template Download](https://drive.google.com/file/d/1Xaw4GtlKdvEVneQZmPDfTXVjCvr00o8W/view?usp=sharing)

2. **Update assignment links for your JupyterHub**: The default template links to datahub.berkeley.edu. If your institution uses a different JupyterHub, use the [Canvas JupyterHub rewriter](https://canvas.juphub.com) to update the zip or .imscc file before importing:

   - Upload your Canvas template (zip or .imscc file) to the rewriter
   - Enter your JupyterHub URL (e.g., `datahub.berkeley.edu/hub` or your institution's hub URL)
   - Enter the materials repository URL — for Data 6, use `https://github.com/dubois-ctds/data-6-materials-student`
   - Scan and preview to see how links will change
   - Check the preview — confirm that old links are being rewritten to your hub and that the repo points to `dubois-ctds/data-6-materials-student`
   - Rewrite and download the updated file

*Video: JupyterHub rewriter*

:::{iframe} https://www.youtube.com/embed/xbvQF5HmwUw
:width: 100%

:::

3. **Import into Canvas**: Once you have the rewritten .imscc file (or the original template if using datahub.berkeley.edu):

   - Create a new course (or use an existing one) — Settings → Start a new course, name it (e.g., "Data 6 example")
   - Go to Import Course Content — In your Canvas course, open the course menu and select Import Course Content
   - Select **Common cartridge 1.x package** as the content type
   - Upload the .imscc file (the rewritten file from step 2, or the original template)
   - Choose import options — For a fresh course, upload all content; for existing content, select specific content, adjust due dates, or overwrite matching assessments
   - Wait for the import — Status will show "queued" then "running" with a progress bar
   - **Verify the links** — After import, click on an assignment (e.g., Homework 1) and check the link in the bottom-left corner of your browser. It should show your JupyterHub URL. Click through to confirm the notebook loads correctly

*Video: Uploading the Canvas template*

:::{iframe} https://www.youtube.com/embed/tsi-z_cf8Pc
:width: 100%

:::

```{note}
**Canvas Shell Features**

The Canvas shell includes:
- Reading assignments embedded as quizzes (ensures student engagement)
- Week-by-week course structure
- Pre-configured assignment links
- Gradebook setup

This template provides a complete course structure that you can customize.
```

```{tip}
**Alternative Platforms**

If you're not using Canvas, the materials work with other LMS platforms. The core notebooks are platform-independent and can be linked from any LMS.
```

**Step 5:** Understanding the Student Workflow

*Review this before your first class*

Here is how students will interact with assignments:

1. **Access**: Students log into Canvas and click on an assignment link
2. **Open Notebook**: The notebook opens in JupyterHub (in a new tab)
3. **Work**: Students complete the notebook, checking answers as they go
4. **Export**: Students use the "export" cell at the bottom to download their completed notebook
5. **Submit**: Students upload the downloaded file to Canvas

```{tip}
**Best Practices**

- Test the workflow yourself before assigning to students
- Provide clear instructions in your first assignment
- Consider a practice assignment to familiarize students with the process
- Have a backup plan (email submission) for students with technical issues
```

**Step 6:** Instructor Grading Workflow

*Estimated time: 5-10 minutes per assignment (after initial setup)*

1. **Download student submissions**: Export all submissions from Canvas as a zip file

2. **Get solutions**: 
   - Log into the private solutions repository on GitHub
   - Navigate to the `autograder_zips` folder
   - Download the `autograder.zip` file for the assignment you're grading

3. **Grade automatically**: 
   - Use one of the grading methods (see [Grading section](grading/grading.md)):
     - **Otter Service Standalone** (recommended, web-based)
     - **GradeScope** (paid service with Canvas integration)
     - **Local grading** (full control, requires setup)

4. **Import grades**: Upload the CSV file with grades back to Canvas

```{tip}
**Grading Tips**

- Test the grader with a few submissions first
- Review the log file if there are errors
- Most assignments grade in about 1 minute per 10 notebooks
- Keep backup copies of graded files

For detailed grading instructions, see the [Grading Guide](grading/grading.md).
```

## Troubleshooting

**Issue: Can't access private repositories**

- Check that you've accepted all GitHub invitations
- Verify your GitHub username matches what you provided in the form
- Contact [data6@berkeley.edu](mailto:data6@berkeley.edu) if issues persist

**Issue: JupyterHub setup taking too long**

- This is normal - IT departments often need 1-2 weeks
- We can help communicate with your IT department
- Consider temporary alternatives (Google Colab, Binder) while waiting

**Issue: Canvas import errors**

- Make sure you're using the correct Canvas version
- Check file size limits
- Try importing sections individually if the full import fails

**Need more help?** Contact us at [data6@berkeley.edu](mailto:data6@berkeley.edu)

