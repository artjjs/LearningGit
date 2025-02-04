# :tropical_fish: :fish: :tropical_fish: Learning GIT :tropical_fish: :fish: :tropical_fish:
> [!NOTE]
> Sourced from https://antonz.org/git-by-example/:

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

## Shows file systems and memory used while creating and editing projects.
1. Tool commands
      - nano text.txt
      - echo text > file.txt or .py or .ect...
      - cat text.txt
      - gh auth login
2. Git commands
   - Rename file
      - git mv file.txt message.txt
   - Show working tree/dir
      - git status
   - Show commit logs
      - git log --onefile or/and --graph, --decorate
   - Show contents of commit
      - git show HEAD or HEAD~1 or HEAD~2 or HEAD~ect...
   - Search for text
      - git grep hello
   - Push file into staging area
      - git add file.txt
   - Create a repo with a user email and name
      - git init
      - git config user.email@mail.com
      - git congif user.name Name

  ### Example ::
    //Create a repo with a user email and name
      -git init
      -git config user.email@mail.com
      -git congif user.name Name
    //You can create a file and push it
      -echo hello > message.txt
    //review
      -cat message.txt
    //push file into staging area
      -git add file.txt
    //Check out staging area
      -git diff --cached
    //push change into branch
      -git commit -m or/and -a
    //Create a new branch
      -git branch stick
    //Switch to the stick branch
      -get switch stick
    //You can create a file and push it
      -echo hello > messageInStick.txt
    //push file into staging area
      -git add messageInStick.txt
    //push change into branch
          //-a only works when you wanna edit the same file again
      -git commit -m or/and -a
    //Switch back to master
      -git switch master
    //Change the master branch the same way the stick branch has been changed
      -git merge stick
    //Take a look at the log
      -git log --oneline --graph --decorate
### Example - online::
      //Get logged in to edit from terminal
            -gh auth login
      //Now we clone the project 
            -git clone https://github.com/artjjs/LearningGit.git
      //We can now cd into the folder and start editing the project.
      //When we are all done we can push the changes.
            -git push
