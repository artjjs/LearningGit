# :tropical_fish: :fish: :tropical_fish: Learning GIT :tropical_fish: :fish: :tropical_fish:
> [!NOTE]
> figure 1.
## Git structure :::

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

## Learning the ropes ::
# Simple overview :
- Create a repo with a user email and name, All offline
      - git init
      - git config user.email@mail.com
      - git congif user.name Name
- Create a new text file in the repo
      - first create using..
            - nano text.txt
      - or create using..
            - echo Hello world > text.txt
      - then verify..
            - cat text.txt
- Add your file into the 'staging area : figure1'
