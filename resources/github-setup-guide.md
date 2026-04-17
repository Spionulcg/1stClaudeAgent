# GitHub Setup Guide — Push a Local Folder to GitHub

A step-by-step guide to initialize a local folder as a git repo and push it to your GitHub account using GitHub CLI (`gh`).

## Prerequisites

- **Git** installed → [git-scm.com](https://git-scm.com/)
- **GitHub CLI** installed → [cli.github.com](https://cli.github.com/)
- **Authenticated** with GitHub CLI → run `gh auth login` if not done yet

To verify everything is ready:

```
git --version
gh --version
gh auth status
```

## Step-by-Step Instructions

### 1. Open a terminal and navigate to your folder

```
cd "F:\YourFolderPath"
```

Replace `F:\YourFolderPath` with the actual path to the folder you want to push.

### 2. Initialize the git repository

```
git init
```

### 3. Create a .gitignore file (optional but recommended)

```
echo .claude/ > .gitignore
```

Add any other files or folders you want to exclude, one per line. For example:

```
echo node_modules/ >> .gitignore
echo *.tmp >> .gitignore
```

### 4. Stage all files

```
git add .
```

### 5. Make your first commit

```
git commit -m "Initial commit"
```

### 6. Create the repo on GitHub and push

For a **public** repo:

```
gh repo create YourRepoName --public --source=. --remote=origin --push
```

For a **private** repo:

```
gh repo create YourRepoName --private --source=. --remote=origin --push
```

Replace `YourRepoName` with whatever you want the repo to be called on GitHub.

## After Setup — Daily Workflow

Once the repo is set up, pushing new changes is just three commands:

```
git add .
git commit -m "describe what you changed"
git push
```

## Useful Commands

| Command | What it does |
|---|---|
| `git status` | See what files have changed |
| `git log --oneline -5` | See last 5 commits |
| `git remote -v` | Check which GitHub repo is linked |
| `git diff` | See detailed changes before committing |
| `gh repo view --web` | Open the repo in your browser |

## Example — Full Setup in One Go

```
cd "F:\!Claude\MyNewProject"
git init
echo .claude/ > .gitignore
git add .
git commit -m "Initial commit - MyNewProject"
gh repo create MyNewProject --public --source=. --remote=origin --push
```

## Troubleshooting

- **"not a git repository"** → Make sure you ran `git init` in the folder first.
- **"gh: command not found"** → Install GitHub CLI from [cli.github.com](https://cli.github.com/).
- **Authentication errors** → Run `gh auth login` and follow the prompts.
- **"repository already exists"** → The repo name is taken on your account. Choose a different name or use `git remote add origin https://github.com/YourUsername/ExistingRepo.git` then `git push -u origin master`.
