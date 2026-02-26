# From zero to hero with git, GitHub, and remote development environments

## Outline

### 1. Getting started with GitHub

- Go to https://github.com/
- Click "Sign up for GitHub"
- Follow the steps

**Done when**: You can navigate to your GitHub profile at `https://github.com/<your-username>`

### 2. Our first repository

- Go to https://github.com/, find the "+" button on the top-right, click "New repository"
    - Alternatively, go to https://github.com/new
- When asked, use your username as the repository name
    - 👀 You should see a blue sign starting with _"[...] is a ✨special ✨ repository that you can use to add a README.md"_
- Enable "Add README"
- Click "Create repository"

**Done when**: Your GitHub profile shows the contents of your personal README at the top
(use the URL from the previous step)

### 3. Get started with Firebase Studio

> [!WARNING]
> This assumes you have a Google account. If you don't, go to https://accounts.google.com/ to get a **personal** one.

- Go to https://firebase.studio/
- Click "Try Firebase Studio"
- Log in with your Google account, and accept the terms of service
- Click the "Import Repo" button at the bottom
- Paste your GitHub profile URL from step 1
- Use "personal-readme" for the workspace name
- Wait for the workspace to be set up

Now, make an edit and push it:

- Open your `README.md`
- Make a small edit
- Open the "Source Control" panel on the left
    - 👀 You should see README.md under "Changes" on the top left, with a blue "M" mark
- Type "Update README" in the "Message" box
- Click "Commit", and when the dialog says "There are no staged changes to commit", click "Yes"
- Click "Sync Changes", and when the dialog says "This action will pull and push commits from and to "origin/main"", click "Yes"
- When the dialog says "The extension 'GitHub' wants to sign in using GitHub", click "Allow"
- Click "Copy and Continue to GitHub", paste the 8-character code that appeared in the dialog, and click "Continue"
- Click "Authorize Visual-Studio-Code"

**Done when**: Your GitHub profile shows the _updated_ contents of your personal README at the top

### 4. Get started with the git command-line interface (CLI)

Still on Firebase Studio:

- Open your `README.md`
- Make a small edit
- Open the hamburger menu on the top-left, View, Terminal
- When the terminal is ready (you should see a line ending with `$`), type `git status`, then hit the Enter/Return key
    - 👀 You should see "Changes not staged for commit" and `modified: README.md` highlighted in **red**
- Type `git add README.md`, hit Enter/Return, and then repeat `git status`
    - 👀 You should see "Changes to be committed" and `modified: README.md` highlighted in **green**
- Type `git commit -m 'Update README from the terminal'`, hit Enter/Return, and then repeat `git status`
    - 👀 You should see "Your branch is ahead of 'origin/main' by 1 commit" and "nothing to commit, working tree clean"
- Type `git push`, hit Enter/Return, and then repeat `git status`
    - 👀 You should see "Your branch is up to date with 'origin/main'" and "nothing to commit, working tree clean"

**Done when**: Your GitHub profile shows the _updated_ contents of your personal README at the top

### 5. Contribute to somebody else's repository

- Open https://github.com/astrojuanlu/from-zero-to-hero-git-github/
- Click the "Fork" button on the top-right
- Click the "Create fork" button on the bottom-right
    - You should now be redirected to `https://github.com/<your-username>/from-zero-to-hero-git-github`
- Go to https://studio.firebase.google.com/
- Click the "Import Repo" button at the bottom
- Paste the URL of your newly created fork

> [!WARNING]
> For simplicity, use the URL of the repo and _not_ the URL of the official repository!
> Otherwise, the steps below will need a few changes.

- Wait for the workspace to be set up

Now, make an edit and push it to your fork:

- Go to the directory corresponding to the event you are in
- Follow the instructions from the README in that directory
- Use the VS Code interface _or_ the git CLI to make a commit and push it

Now, the final step: create a pull request!

- Navigate to your fork (the URL from the previous step)
- Click the "Contribute" button, then "Open pull request"
- Click "Create pull request"
- Wait for the pull request to be merged

**Done when**: Your pull request is merged 🎉

### 6. Make a second contribution to somebody else's repository

> [!WARNING]
> This looks silly but it isn't. _After_ the first contribution is merged, some cleanup steps are needed
> to be able to continue working. This section will guide you through them.

> [!INFO]
> Similar steps can be followed using the UI. It is left as an exercise to the reader.

- Go to the terminal, type `git fetch`, hit Enter/Return, and repeat `git status`
    - 👀 You should see "Your branch is behind `origin/main` by 2 commits, and can be fast-forwarded" and "nothing to commit, working tree clean"
- Type `git merge --ff-only`, hit Enter/Return, and repeat `git status`
    - 👀 You should see "Your branch is up to date with 'origin/main'" and "nothing to commit, working tree clean"

Ready! Now make your second contribution, but using a separate _branch_:

- Type `git switch --create second-contribution`, hit Enter/Return, and repeat `git status`
    - 👀 You should see "Switched to a new branch 'second-contribution'"
- Make a change to your file and commit it using the steps from the previous sections
- Type `git push -u origin second-contribution`, hit Enter/Return, and repeat `git status`
    - 👀 You should see "Your branch is up to date with 'origin/second-contribution'" and "nothing to commit, working tree clean"
- Follow the steps from the previous section to open a pull request, and wait for it to be merged
- Type `git switch main`, hit Enter/Return, and follow the cleanup steps from this section
- Type `git branch --delete second-contribution` and hit Enter/Return

**Done when**: Your second pull request is merged, your local `main` branch is up to date with `origin/main`, your `second-contribution` branch doesn't exist anymore.

If you made it this far, congratulations! 🏆

## Resources

### git

![Triangular workflows](https://github.blog/wp-content/uploads/2015/07/5dcdcae4-354a-11e5-9f82-915914fad4f7.png)

- https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository

### GitHub for Education

- https://github.com/education/
- https://education.github.com/pack/ (includes GitHub Pro!)
- https://docs.github.com/en/education/about-github-education/github-education-for-students/apply-to-github-education-as-a-student
- https://github.com/settings/education/benefits
- https://education.github.com/experiences/foundations_certificate
- https://education.github.com/experiences/primer_codespaces (only for verified students)

### Canonical

- Ubuntu Community https://ubuntu.com/community
- Canonical Academy https://canonical.com/academy
