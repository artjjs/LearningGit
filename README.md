# :tropical_fish: :fish: :tropical_fish: Learning GIT :tropical_fish: :fish: :tropical_fish:
> [!NOTE]
> figure 1.
## Git structure ::

      ┌──────────────┐         ┌──────────────┐
      │ local        │ push ─> │ remote       │
      │ repo         │ <- pull │ repo         │
      └──────────────┘         └──────────────┘
      check │  ↑↓ commit / reset
      out   │ ┌──────────────┐
            │ │ staging area │
            │ └──────────────┘
            ▽  ↑↓ add / restore
      ┌──────────────┐
      │ working tree │
      │ .            │
      │ ├── go.mod   │
      │ └── main.go  │
      └──────────────┘

> [!NOTE]
> Sourced from https://antonz.org/git-by-example/:

## Simple overview :
1. Create a repo with a user email and name, All offline
   - Make a local repo
      - git init
   - git config user.email@mail.com
      - git congif user.name Name
2. Create a branch of the project to edit
   - Create a branch
      - git branch jackbranch
   - Switch to your new branch
      - git switch jackbranch
   - then you can look at the branch
      - git log --oneline --graph --decorate
3. Create a new text file in the branch
   - first create using..
      - nano text.txt
   - or create using..
      - echo Hello world > text.txt
   - look at your file's content using..
      - cat text.txt
4. Add your file
   - push into the 'staging area : figure1'
      - git add text.txt
   - look at the 'staging area : figure1'
      - git diff --cached
   -Add your file into your branch
      - git commit -m "Note about commit here."
      - If you are going to change this file over and over again,
      - you can skip doing git add file.txt and just do git commit -a
      - the -a indicates you loaded the file previously just wanna commit it again no loading.
5. Switch back to your main and merge the branch
   - Switch back to main
      - git switch main
   - Merge your edited branch back into main
      - git merge jackbranch
6. Now for projects made online you can replace step 1 with
   - Login
      - gh auth login
   - Clone your repo you wanna work on
      - git clone https://github.com/artjjs/LearningGit.git
   - Cd into your cloned project
      - cd NAMEOFPROJECT
   - Follow steps
      - 2
      - 3
      - 4
      - 5
   - Do a pull to update your local repo copy to the latest update as of this moment
      - git pull
   - If you have a Commit Conflit, Check what is conflicting and resolve it
      - git status
   - Update your github account
      - git push
7. Couple extra things learned from this first tutorial
   - Show contents of commit
      - git show HEAD or HEAD~1 or HEAD~2 or HEAD~ect...
   - Search for text
      - git grep hello
