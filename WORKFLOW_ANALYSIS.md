GitHub Actions Workflow Analysis
## 1. What triggers this workflow to run?

This workflow runs when someone pushes code to the main branch or creates or updates a pull request going into the main branch.

## 2. What are the four main steps this workflow performs?

The four main steps are:

1. Checkout code
2. Validate HTML
3. Check links
4. Upload artifact

## 3. What does the "Checkout code" step do and why is it necessary?

The "Checkout code" step gets the files from the GitHub repository so the workflow can use them. This step is necessary because the workflow needs the website files to check the HTML, check the links, and prepare the files for deployment.

## 4. What is the purpose of the environment configuration?

The environment configuration connects the deployment to the github-pages environment. It also provides the URL for the deployed website, which makes it easier to find the live website.

## 5. How does this automated deployment improve reliability compared to manual deployment?

Automated deployment makes the process more reliable because the same checks are done each time. It checks the HTML, checks for broken links, and uploads the website automatically. This helps prevent mistakes and saves time compared to manual deployment.
This also makes it easier to catch problems before the website is updated.

## 6. What would happen if you pushed code to a different branch, not main?

If I pushed code to a branch other than main, the workflow would not run from the push because it is only set up to run on pushes to main. A pull request from another branch into main could still run the workflow for testing. The website would only be deployed after the changes are merged into main. Essentially, you have to go through main or merge into main or else it won't run.