# Contributing Guidelines

Hello 👋. We are glad to have you here.

| Index                                                         |
| ------------------------------------------------------------- |
| [Contributing to this repo](#contributing-to-this-repository) |
| [Basic of Git & GitHub](#basics-of-git-and-github)            |

## Contributing to this repository

GWOC encourages individuals to share their knowledge and ideas to develop technical skills and gain valuable experience in the field of tech education. We are creating a content repository which is full of valuable resources. Folders for different domains like Android Development, Web Development have been created and contribution to a specific domain will go to that folder only. Inside each directory there will be subdirectories for sub-topics of that particular domain. **There is a specific branch for each of the domains and participants need to contribute to that branch only**. Eg, if someone is contributing to Web Development or any sub topic of it, contribution to that domain should go to the specific branch only.

### Types of contribution you can make

We are focussing on 3 types of contributions as of now.

1. Documentation

- Content such as codes or tutorials
- Preferred language should be English
- Accepted via [Google Colab](https://colab.research.google.com/)
- Clear, Consise and Complete

2. Video

- Animations, screen-recordings, presentations and regular explanatory films are all possibilties
- Video length should not exceed more than 25 min
- Presentable and Clear
- Accepted via Google drive link

3. Audio

- Should be in mp3 format
- Includes speech clarity,concise ,low distortion
- Presentation can also be submitted along with audio [Optional]
- Accepted via Google drive

Note: For video and audio files, only link should be added to the repository with details of the video/audio.

✔ Participants are requested to give regular updates regarding their progress to the mentors.

✔ If the participant is not able to contribute to the assigned issue due to any reason, kindly let the mentors know so that the issue is assigned to some other participant.

<br />

---

<br />

## Basics of Git and GitHub

### Git & GitHub

Before continuing we want to clarify the difference between Git and Github. Git is a version control system(VCS) which is a tool to manage the history of our Source Code. GitHub is a hosting service for Git projects.

We assume you have created an account on Github and installed Git on your System.

Now tell Git your name and E-mail (used on Github) address.

`$ git config --global user.name "YOUR NAME"`
` $ git config --global user.email "YOUR EMAIL ADDRESS"`
This is an important step to mark your commits to your name and email.

<br />

### Fork a project

You can use github explore - https://github.com/explore to find a project that interests you and match your skills. Once you find your cool project to workon, you can make a copy of project to your account. This process is called forking a project to your Github account. On Upper right side of project page on Github, you can see -

<p align="center">  <img  src="https://i.imgur.com/P0n6f97.png">  </p>
Click on fork to create a copy of project to your account. This creates a separate copy for you to work on.

<br />

### Finding a feature to work on

Open Source projects always have something to work on and improves with each new release. You can see the issues section to find something you can solve or report a bug. The project managers always welcome new contributors and can guide you to solve the problem. You can find issues in the right section of project page.

<p align="center">  <img  src="https://i.imgur.com/czVjpS7.png">  </p>

<br />

### Clone the forked project

You have forked the project you want to contribute to your github account. To get this project on your development machine we use clone command of git.

`$ git clone https://github.com/<your-account-username>/<your-forked-project>.git`
Now you have the project on your local machine.

<br />

### Add a remote (upstream) to original project repository

Remote means the remote location of project on Github. By cloning, we have a remote called origin which points to your forked repository. Now we will add a remote to the original repository from where we had forked.

`$ cd <your-forked-project-folder>`
`$ git remote add upstream https://github.com/<author-account-username>/<project>.git`
You will see the benefits of adding remote later.

<br />

### Synchronizing your fork

Open Source projects have a number of contributors who can push code anytime. So it is necessary to make your forked copy equal with the original repository. The remote added above called Upstream helps in this.

`$ git checkout master`
`$ git fetch upstream`
`$ git merge upstream/master`
`$ git push origin master`
The last command pushes the latest code to your forked repository on Github. The origin is the remote pointing to your forked repository on github.

<br />

### Create a new branch for a feature or bugfix

Normally, all repositories have a main branch which is considered to remain stable and all new features should be made in a separate branch and after completion merged into main branch. So we should create a new branch for our feature or bugfix and start working on the issue.

`$ git checkout -b <feature-branch>`
This will create a new branch out of master branch. Now start working on the problem and commit your changes.

`$ git add --all`
`$ git commit -m "<commit message>"`
The first command adds all the files or you can add specific files by removing -a and adding the file names. The second command gives a message to your changes so you can know in future what changes this commit makes. If you are solving an issue on original repository, you should add the issue number like #35 to your commit message. This will show the reference to commits in the issue.

<br />

### Rebase your feature branch with upstream

It can happen that your feature takes time to complete and other contributors are constantly pushing code. After completing the feature your feature branch should be rebase on latest changes to upstream master branch.

`$ git checkout <feature-branch>`
`$ git pull --rebase upstream master`
Now you get the latest commits from other contributors and check that your commits are compatible with the new commits. If there are any conflicts solve them.

<br />

### Squashing your commits

You have completed the feature, but you have made a number of commits which make less sense. You should squash your commits to make good commits.
`$ git rebase -i HEAD~5`
This will open an editor which will allow you to squash the commits.

<br />

### Push code and create a pull request

Till this point you have a new branch with the feature or bug fix you want in the project you had forked. Now push your new branch to your remote fork on github.

`$ git push origin <feature-branch>`
Now you are ready to help the project by opening a pull request means you now tell the project managers to add the feature or bug fix to original repository. You can open a pull request by clicking on green icon -

<p align="center">  <img  src="https://i.imgur.com/aGaqAD5.png">  </p>

Remember your upstream base branch should be master and source should be your feature branch. Click on create pull request and add a name to your pull request. You can also describe your feature.

Awesome! You have made your first contribution.

#### BE OPEN!

#### Happy Coding 👩‍💻👩‍💻