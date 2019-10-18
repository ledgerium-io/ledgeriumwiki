# How to Contribute
When submitting a pull request (PR), please use the following guidelines:
* Make sure your code respects existing formatting conventions. In general, follow the same coding style as the code that you are modifying.
* Do add/update documentation appropriately for the change you are making.
* If you are introducing a new feature you may want to first write about your idea for feedback to developers@ledgerium.io . Or create an issue using "Feature/Change" template. Non-trivial features should include unit tests covering the new functionality. Open a "Proposal" issue for large changes.
* Bugfixes should include a unit test or integration test reproducing the issue.
* Do not use author tags/information in the code.
* Try to keep pull requests short and submit separate ones for unrelated features, but feel free to combine simple bugfixes/tests into one pull request.
* If you are adding or updating a dependency, be sure to update the version, license, or notice information in ___.yaml as appropriate to help ease LICENSE and NOTICE management for ASF releases.

# GitHub Workflow
1. Fork the ledgerium-io/<repo_name> repository into your GitHub account

    `https://github.com/ledgerium-io/<repo_name>/fork`
2. Clone your fork of the GitHub repository
    ```
    git clone git@github.com:<username>/<repo_name>.git 
    ```
    replace <username> with your GitHub username and <repo_name> with repository name.
3. Add a remote to keep up with upstream changes
    ```
    git remote add upstream https://github.com/ledgerium-io/<repo_name>.git
    ```
    If you already have a copy, fetch upstream changes
    ```
    git fetch upstream master
    ```
4. Create a lb branch to work in
    ```
    git checkout -b lb-xxx remotes/upstream/master
    ```
5. Before submitting a pull request periodically rebase your changes (but don't do it when a pull request is already submitted)
    ```
    git pull --rebase upstream master
    ```
6. Before submitting a pull request, combine ("squash") related commits into a single one
    ``` 
    git rebase -i upstream/master
    ```
    This will open your editor and allow you to re-order commits and merge them:
    * Re-order the lines to change commit order (to the extent possible without creating conflicts)
    * Prefix commits using `s` (squash) or `f` (fixup) to merge extraneous commits.
7. Submit a pull-request
    ``` 
    git push origin lb-xxx
    ```
    Go to your Ledgerium fork main page
    ``` 
    https://github.com/<username>/<repo_name>
    ```
    If you recently pushed your changes GitHub will automatically pop up a `Compare & pull` request button for any branches you recently pushed to. If you click that button it will automatically offer you to submit your pull-request to the ledgerium-io/<repo_name>.
    * Give your pull-request a meaningful title.
    * In the description, explain your changes and the problem they are solving.
8. Addressing code review comments

    Address code review comments by committing changes and pushing them to your lb branch.
    ``` 
    git push origin lb-xxx 
    ```
## If your pull request shows conflicts with master
If your pull request shows conflicts with master, merge master into your lb branch:
```
git merge upstream/master
```
and resolve the conflicts. After resolving conflicts, push your branch again:
```
git push origin lb-xxx
```
Avoid rebasing and force pushes after submitting a pull request, since these make it difficult for reviewers to see what you've changed in response to their reviews. The Ledgerium committer that merges your change will rebase and squash it into a single commit before committing it to master.
# FAQ   
## Help! I merged changes from upstream and cannot figure out how to resolve conflicts when rebasing!

Never fear! If you occasionally merged upstream/master, here is another way to squash your changes into a single commit:    
1. First, rename your existing branch to something else, e.g. ``lb-xxx-unclean`
    ``` 
    git branch -m lb-xxx-unclean
    ```

2. Checkout a new branch with the original name `lb-xxx` from upstream. This branch will supercede our old one.
    ```
    git checkout -b lb-xxx upstream/master
    ```
3. Then merge your changes in your original feature branch `lb-xxx-unclean` and create a single commit.
     ```
    git merge --squash lb-xxx-unclean
    git commit
    ```
4. You can now submit this new branch and create or replace your existing pull request.
    ```
    git push origin [--force]lb-xxx:lb-xxx
    ```
