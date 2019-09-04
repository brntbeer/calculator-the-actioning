# Demo Guide
This repo is meant to serve as an isolated repo once forked and not to continue to receive updates from the upstream repo.

To get started, Fork this repository to the location of your hearts desire to run through an Actions and or Security vulnerability demo

## Actions
- Click on actions tab
- Select NodeJS template
  - Bring attention to the structure of the .yml file that's generated and talk through it's simplicity.
  - Mention the documentation on the right side of the page as well if desired
- Open PR
  - Ensure it's directed at your own repository and not the upstream octodemo/calculator repo.
- Show off the Checks tab as it's running
  - Matrix build
  - Linking to log file lines and showing timestamps (... button in upper right hand corner)
- Merge!

## Security Vulnerability
- Once Actions has been configured, navigate over to the settings tab to enable Data Services (Allowing read-only of repository, dependency graph, and security alerts)
- Navigate to the security tab, by then you should see some security vulnerabilities
- Select the dropdown for "Automated Security fixes" and enable it. After a minute or two, dependabot will open a pull request or show that a pull request is being generated.
- When a pull request is created, navigate to it, (optionally show off actions running again)
- Merge away!

**Note:** If dependabot ever has a issue generating a security fix because of another dependency, merge one Pull Request and re-visit that vulnerability and click the green "Generate automated security fix" button to give it another try

## Resetting the demo
When the demo is complete, you ultimately will want to reset your demo back before all of these fixes.

- **If you dont want security fixes to run right away, you should disable the "Automated Security Fixes" on the Security tab or disable Data Services entirely from the settings page.**
- When ready, in the terminal run `script/reset`.
  - This will prompt for a y / n response to continue
- **NOTE**: As mentioned in the prompt, it will reset your origin, which _should_ be your fork.
- Once you force push, you may need to revisit the security page to ensure github is creating the build for you.
