# Milvus Github workflow guidelines

Generally, we follow the "fork-and-pull" Git workflow.

This guide covers all the aspects about Milvus github workflow, from Git newcomers to pros, you can find something meaningful in this guide. Even if you know completely nothing about Git or Github or codes, you can still find your way into contributing to Milvus throught this guide.

Feel free to jump to the subjects that interest you.

1. [Simplest workflow for Git beginners(TODO Graphs)](#simplest-workflow-for-git-beginners)
2. [General git workflow](#general-git-workflow)

## Simplest workflow for Git beginners 

> This section is suitable for Git beginners who have never used command line tool `Git` before, also suitable for amending typos or docs . 

### Click, click, and click

Supposing you spot a typo on this file, and it'll take no more than 1 minute to fix. So, why bother the whole fork-and-pull process? There's an easier way to amend this typo on Github online. 

1. Fork this project. If forked, no need to do this again.

2. Click into the file with the typo.

3. Click the edit button (A pencil like button with `Edit the file in your fork of this project` ) at the right-top of the file.

4. Amend the typo on the edit page

5. Filling in the  `Propose changes` at the bottom of the page. This will become the commit message later, so please pay attention. **Once the commit message is proposed, it's impossible to edit on Github online.**

   1. Meaningful title **starts** with [skip-ci], like

      ````markdown
      [skip-ci]Fix typo in CONTRIBUTING.md
      ````

   2. Meaningful body with DCO, like below.  **Again, be careful with the DCO, once the commit message is proposed, it's impossible to amend online**.

      ````markdown
      Change ook into ok
      
      Signed-off-by: your-github-name <your-github-email@xxx.com>
      ````

6. Click the `Propose changes` green button (**commit message unchangeable since step 6**)

7. Check the base repository and base branch, click the  `Create pull request` green button, and enter the `open a PR`  page

8. Add `/kind improvement` in the PR body (Commit message is fixed after step 6, this is just a PR message body.) and click the `Create pull request` green button.

After step 6, if your encounter any problems, please start over from step 2. Or, [**welcome to the real Git world**](#general-git-workflow) :tada:!

### Explainations

1. About `[skip-ci]`: commit message titled with `[skip-ci]` will skip all  testing actions of Milvus in PR, usually used on PRs of documentation amends.
2. About DCO: All contributors should sign a DCO, we use a Github action to make sure of that. A PR is invalid util the DCO action passes.
3. About adding `/kind improvement`: Indicate this's an improvement PR, the @src-ci-robot will label `kind/improvement` for this PR, which is very useful when collecting release notes.

> Note: Many people mistake `PR messages` for `commit messages`. A `commit message` is fixed with a commit, a change of the `commit message` will lead to a change of the commit (commit hash changes).  `PR messages` are more of a reminder for reviewers and approvers.
>
> But when you make a PR, Github will **copy** your `commit messages` as `PR messages`, which makes you think they are identical, and makes you think justing editing the `PR messages` on Github online will change the `commit messages`. Wrong!
>
> The DCO, commit message body, and commit message title we care about **CANNOT** be changed by editing `PR messages`.  You'll have to change `commit messages` locally and force push to your Github forked repository.
>

## General git workflow
