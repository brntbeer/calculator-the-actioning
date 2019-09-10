# :1234: Demo guide

This repository is meant to serve as an isolated repository once forked, and is not meant to continue to receiving updates from the upstream repository.

To get started, fork this repository to the location of your heart's desire to run through a simple [Actions](https://help.github.com/en/categories/automating-your-workflow-with-github-actions) and or [security vulnerability](https://help.github.com/en/categories/managing-security-vulnerabilities) demo.

## :arrow_forward: Actions

- Click on the **Actions** tab.

- Select the **Node.js** workflow template.

  - Bring attention to the structure of the `.yml` file that's generated and talk through its simplicity.

  - Mention the documentation on the right side of the page as well if desired.

- Open a pull request.

  - Ensure it's directed at your own repository and not the upstream `octodemo/calculator` repository.

- Immediately toggle to the **Actions** tab to highlight the key Actions features and values as it's running:

  - Live logs

  - Matrix builds

  - Linking to log file lines

  - Timestamps (the `...` button in the upper right hand corner)

- Toggle back to your pull request to show the Actions checks running/completing and passing/failing.

  - Optionally click one of the [Details]() link next to a check, to show how it takes you directly to the check _in the same UI_.

- Merge your pull request!

### Showing CI failures

- If you would like to show CI job failures, follow the steps [in this video](https://www.youtube.com/watch?v=vlBuNM6Wzic&feature=youtu.be&t=624) to make a change to the [`arithmeticController.js`](https://github.com/octodemo/calculator/blob/demo-instructions/api/controllers/arithmeticController.js) that will cause the CI test jobs to fail.

## :unlock: Security vulnerabilities

- Once Actions has been configured, navigate over to the **Settings** tab to enable **Data services**, by selecting the checkboxes for:

  - Allow GitHub to perform read-only analysis of this repository

    - Dependency graph

    - Security alerts

- Navigate to the **Security** tab; you should see some security alerts.

- Select the dropdown for **Automated Security fixes** and enable it.

- After a minute or two, [Dependabot](https://help.github.com/en/articles/configuring-automated-security-fixes) will open a pull request or show that a pull request is being generated.

- When a pull request is created, navigate to it, (optionally show off Actions running again).

- Merge away!

**NOTE:** If Dependabot ever has an issue generating a security fix because of another dependency, merge one pull request and re-visit that vulnerability and click the green **Create automated security fix** button to give it another try.

## :rewind: Resetting the demo

When the demo is complete, you ultimately will want to reset your demo back to its state before all of the above activities and changes.

**NOTE:** If you do not want security fixes to run right away, you should disable the **Automated security fixes** on the **Security** tab, or disable **Data services** entirely from the **Settings** tab.

- When ready, in the terminal run `script/reset`.

  - This will prompt for a `[y/n]` response to continue.

**NOTE**: As mentioned in the prompt, it will reset your `origin`, which _should_ be your fork.

- Once you force push, you should revisit the **Security** tab to ensure GitHub is not fixing the vulnerability. It should tell you that GitHub is unable to tell you vulnerability data because you disabled **Data Services**.
