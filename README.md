# 2026 FED - a first GitHub round trip

Follow these steps to learn the lifecycle of creating a GitHub repo, cloning it to your local computer, making changes to the project, and synchronising them back up to GitHub.


NOTE: You will need “git” installed at the command line for your operating system
(it is installed on the all the college computers already, like Node)
- Get Git from:
  - https://git-scm.com/downloads
- Video walkthrough of installing Git for Windows:
  - https://go.screenpal.com/watch/cOn6QTn0etq

## Summary of GitHub/Git round trip workflow

Summary for working at the CLI:
- Create new empty PRIVATE project on GitHub (with a `README.md` & appropriate `.gitignore`)
- Copy URL to clipboard
- At Terminal clone project to local computer
  - `git clone <url>`
- "cd" into cloned folder
- Create/copy the files to be uploaded into cloned folder 
- Track all new files 
  - `git add .`
- Commit tracked files to repository “snapshot”
  - `git commit –m “added files to project”`
- Upload new commit contents to GitHub website
  - `git push`
- Add `dr-matt-smith` as collaborator

## Steps for GitHub round trip

1. Log into your GitHub account

2. Create a new repository
   - select the **Repositoroes** tab
   - click the green **New** button
   - ![](/images/1_new_repo_button.png)

3. Enter details for new repository
    - give the repository a meaningful name
    - choose PRIVATE visibility (if the project is for assessed university work!)
    - click button to reate a README file
    - choose an appropriate `.gitignore`, e.g. for **Node** JavaScript project
    - click the button to create the new repo
   - ![](/images/2_new_repo_details.png)

4. Copy the repo URL into the computer's cliboard
    - from the green Code dropdown, you can click the icon to copy the repo's URL into the clipboard
    - (or you can just copy the repo's URL from your web brower's address bar)
   - ![](/images/3_url_to_clipboard.png)
   - ![](/images/4_url_for_cloning.png)


Step 5 NOTE: 
  If you get an error talking about "git@github.com: Permission Denied (publickey)" when you try the next step, you can find the solution steps (and video walkthrough) to setting up and sharing an SSH key on your Windows computer here:
  - https://github.com/dr-matt-smith/windows-github-ssh-communications-key

5. On your local computer **clone** a copy of the repo
   - work in your Terminal / CLI Command console window
   - "cd" into the folder where to work (temporarily) on your GitHub project (e.g. `Downloads` or perhaps `github`)
     - `matt> cd Downloads`
   - cd into your temporary folder
     - `matt/Downloads>  git clone <url>`
   - now you can cd into the newly download GitHub project folder (same name
   as your project - in this example the repo is named `php-project`)
     - `matt/Downloads> cd github-node-project-demo`
   - you can now see a copy “clone” of the Github files on your local computer,
   including the special .git hidden folder (which contains the entire history of
   changes made to your project!)
     -  `matt/Downloads/github-node-project-demo>ls -alF` (or `dir` for windows!)
   - ![](/images/5_cli_cloning.png)

6. Create/Copy/Edit project files and directories
    - make chances to the project directory contents
      - such as created a new file `example.txt`, or copying files from a project elsewhere on disk
   - ![](/images/6_new_file_added.png)

7. Use `git status` to check status of your project
    - `git status`
    - files in red are changes to previous 'snapshot (commit)'
      - e.g. new files / changed files / deleted files
   - ![](/images/7_git_status.png)

8. Use `git add` to add untracked files to staging area (for next snapshot/commit)
    - `git add .`
    - since we have the appropriate `.gitignore`, we can safely add all untracked files to staging for the next snapshot/commit
    - running `git status` again, we see the previously untracked red file(s) are now green
   - ![](/images/8_git_add_green.png)

9. Use `git commit -m "<message>"` to create a new project snapshop/commit
    - `git commit -m "<message>"`
    - enter a short message to summarise changes for this snapshot/commit, such as "new text file created"
    - you'll see a summary of the added/deleted/changed files
   - ![](/images/9_git_commit.png)

10. View your projects remote "origin" to which we can push changes
    - use `git remote -v` to see the URL this project on your computer is linked to
    - these details are part of the contents of the hidden `.git` folder
    - ![](/images/10_git_remote_origin.png)

11. Use `git push` to push files to the remote **origin**
    - `git push`
    - ![](/images/11_push_to_github.png)

    - NOTE: If this is the first time you have pushed to a remote repo, you may have to enter some GitHub user authentication details

12. View updated repo (with new commit) at GitHub.com
    - visit the repo URL at GitHub
    - you should see the enw files, and a new commit
    - ![](/images/11_push_to_github.png)


## Congratulations!
You have now cloned a repo to your machine, made changes, created a new snapshop/commit, and pushed that commit up to GitHub, to sychronise the project files both locally and remotely.
