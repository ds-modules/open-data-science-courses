# Data 6 Adoption Guide

This guide walks you through the step-by-step process of adopting Data 6 at your institution.

## Step 1. GitHub account and instructor interest form

*Estimated time: 15–30 minutes*

1. **Create a GitHub account** (if you don't have one): [https://github.com](https://github.com)
   - We need your GitHub username to grant access to private repositories

2. **Complete the Instructor Interest Form**: [Data 6 Instructor Interest Form](https://forms.gle/2nNtbfgBtNsUHypCA)
   - This form helps us understand your needs
   - You'll receive access to solutions and resources after completion
   - Expect a response within 24 hours

```{tip}
**What happens next**

After submitting the form, you'll receive:
- Email confirmation
- GitHub repository invitations (within 24 hours)
- Access to private solutions repository
- Instructions for next steps
```

## Step 2. Fork the student materials

*Estimated time: 5–10 minutes*

The public student materials are available at [https://github.com/dubois-ctds/data-6-materials-student](https://github.com/dubois-ctds/data-6-materials-student).

1. **Fork the repository**: Click the "Fork" button in the top right of the repository page
   - This creates your own copy that you can customize
   - You can make changes without affecting the original

2. **Explore the materials**: Browse through labs, homeworks, and projects
   - Familiarize yourself with the structure
   - Note any materials you want to customize

```{tip}
**Why fork**

Forking creates your own copy of the materials. This allows you to:
- Customize content for your institution
- Keep your changes separate from the original
- Easily pull updates from the original repository
```

## Step 3. Accept GitHub invitations

*Estimated time: 5 minutes*

```{warning}
We ask that anyone using these materials do not distribute solutions. This protects the integrity of the course materials for all institutions.
```

After completing the Instructor Interest Form, you will be added to private repositories and to grading infrastructure as needed. Accepting invitations in the browser is usually faster than hunting through email.

1. **Solutions repository**: Open [dubois-ctds/data-6-materials-solutions](https://github.com/dubois-ctds/data-6-materials-solutions) while logged into GitHub. If you have a pending invitation, GitHub will prompt you to accept it.
2. **Otter grading service org**: Open the [otter-service-stdalone](https://github.com/orgs/otter-service-stdalone) organization page and accept the invitation if prompted (see the [Grading section](grading.md) for how to use the service).
3. **Verify access**: You should see the private solutions repository and any related repos in your GitHub account.

```{tip}
**Can't find the invitations**

- Check your email spam folder
- Check your GitHub notifications (bell icon)
- Use the links above after you have been added — GitHub often surfaces an "Accept" action on the repo or org page
- If you still cannot get access within 24 hours, email [ds-help@berkeley.edu](mailto:ds-help@berkeley.edu) with the GitHub username you submitted on the form
```

## Step 4. Canvas shell and course website

*Estimated time: 1–2 hours (depending on customization)*

We can help you configure the Canvas shell we have set up for you.

### Download the Canvas template

[Canvas template download](https://drive.google.com/file/d/1ioxchiwz1PPDJk6A5X-HVJeIR0n4rMRl/view?usp=sharing)

### Point assignments at your JupyterHub

The default template links to datahub.berkeley.edu. If your institution uses a different JupyterHub, use the [Canvas JupyterHub rewriter](https://ds-modules.github.io/canvas-jupyterhub-rewriter/) to update the zip or .imscc file before importing:

- Upload your Canvas template (zip or .imscc file) to the rewriter
- Enter your JupyterHub URL (e.g., `datahub.berkeley.edu/hub` or your institution's hub URL)
- Enter the materials repository URL — for Data 6, use `https://github.com/dubois-ctds/data-6-materials-student`
- Scan and preview to see how links will change
- Confirm that old links are being rewritten to your hub and that the repo points to `dubois-ctds/data-6-materials-student`
- Rewrite and download the updated file

#### Video: JupyterHub rewriter

:::{iframe} https://www.youtube.com/embed/xbvQF5HmwUw
:width: 100%

:::

### Import into Canvas

We recommend importing the cartridge into a **new** Canvas course. After the first import, **copy that course inside Canvas** from term to term instead of re-importing the cartridge into an existing shell (re-importing can duplicate items that do not share the same internal IDs).

- Create a new course — Settings → Start a new course, name it (e.g., "Data 6")
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

This template provides a complete course structure that you can customize.
```

```{tip}
**Other LMS platforms**

If you're not using Canvas, the materials work with other LMS platforms. The core notebooks are platform-independent and can be linked from any LMS.
```

## Step 5. Student workflow

*Review this before your first class*

Here is how students will interact with assignments:

1. **Access**: Students log into Canvas and click on an assignment link
2. **Open notebook**: The notebook opens in JupyterHub (in a new tab)
3. **Work**: Students complete the notebook, checking answers as they go
4. **Export**: Students use the "export" cell at the bottom to download their completed notebook
5. **Submit**: Students upload the downloaded file to Canvas

```{tip}
**Best practices**

- Test the workflow yourself before assigning to students
- Provide clear instructions in your first assignment
- Consider a practice assignment to familiarize students with the process
- Have a backup plan (email submission) for students with technical issues
```

## Step 6. Instructor grading workflow

*Estimated time: 5–10 minutes per assignment (after initial setup)*

1. **Download student submissions**: Export all submissions from Canvas as a zip file

2. **Get solutions**:
   - Log into the private solutions repository on GitHub
   - Navigate to the `autograder_zips` folder
   - Download the `autograder.zip` file for the assignment you're grading

3. **Grade automatically**:
   - Use one of the grading methods (see [Grading section](grading.md)):
     - **Otter Service Standalone** (recommended, web-based)
     - **GradeScope** (paid service with Canvas integration)
     - **Local grading** (full control, requires setup)

4. **Import grades**: Upload the CSV file with grades back to Canvas

```{tip}
**Grading tips**

- Test the grader with a few submissions first
- Review the log file if there are errors
- Most assignments grade in about 1 minute per 10 notebooks
- Keep backup copies of graded files

For detailed grading instructions, see the [Grading Guide](grading.md).
```

## Troubleshooting

### Can't access private repositories

- Check that you've accepted all GitHub invitations
- Verify your GitHub username matches what you provided in the form
- Open [dubois-ctds/data-6-materials-solutions](https://github.com/dubois-ctds/data-6-materials-solutions) and the [otter-service-stdalone org](https://github.com/orgs/otter-service-stdalone) while logged in — GitHub may show an accept prompt there
- Contact [ds-help@berkeley.edu](mailto:ds-help@berkeley.edu) if issues persist

### JupyterHub not ready yet

- If hub access is still in progress (for example Cloudbank provisioning), we will give you a realistic timeline when you contact us
- For piloting, consider temporary alternatives (Google Colab, Binder) while your hub is prepared

### Canvas import errors

- Make sure you're using the correct Canvas version
- Check file size limits
- Try importing sections individually if the full import fails

**Need more help?** Contact us at [ds-help@berkeley.edu](mailto:ds-help@berkeley.edu)
