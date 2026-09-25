# CSP26_OnLecture_MAUI — In-class exercises (.NET MAUI applications)

Template repository for .NET MAUI-based in-class exercises on the
**TT00BI73 Client-Side Programming** course (VAMK, autumn 2026).

Each exercise lives in its own folder (`Task1`, `Task2`, …) inside one
shared Visual Studio solution, alongside example projects (`HelloWorld`, …)
demonstrated during lectures.

## Getting started

You can set up your own copy of this repository in one of two ways.

### Option A: Fork the repository

#### 1. Fork the repository

Fork `OnLecture_MAUI` into your own account/group on git.vamk.fi,
then clone your fork:

    git clone https://git.vamk.fi/<your_username>/<your_repo>.git
    cd <your_repo>

#### 2. Add the teacher's repository as upstream

    git remote add upstream https://git.vamk.fi/CSP26/OnLecture_MAUI.git

Verify your remotes:

    git remote -v
    # origin    https://git.vamk.fi/<your_username>/<your_repo>.git (fetch)
    # upstream  https://git.vamk.fi/CSP26/OnLecture_MAUI.git (fetch)

Since your fork's `origin` already points at your own repository, `git push`
will go to your fork by default. If you ever need to make sure of that
explicitly (for example after adding another remote), set the default
push/pull target for your current branch to `origin`:

    git branch --set-upstream-to=origin/main main

You can confirm the tracking branch with:

    git branch -vv

### Option B: Clone and re-point the remotes

#### 1. Clone this repository

    git clone https://git.vamk.fi/CSP26/OnLecture_MAUI.git
    cd OnLecture_MAUI

#### 2. Rename origin and add your own remote

    git remote rename origin upstream
    git remote add origin https://git.vamk.fi/<your_username>/<your_repo>.git

Verify your remotes:

    git remote -v
    # origin    https://git.vamk.fi/<your_username>/<your_repo>.git (fetch)
    # upstream  https://git.vamk.fi/CSP26/OnLecture_MAUI.git (fetch)

### 3. Push to your own repository

    git push -u origin main

### 4. Prerequisites

Make sure you have the **.NET MAUI workload** installed for Visual Studio 2022:

    dotnet workload install maui

### 5. Implement the exercises

Open `CSP26_OnLecture_MAUI.sln` in Visual Studio 2022. Each exercise folder
contains a MAUI project (`Task1`, `Task2`, …) with `TODO` comments marking
the parts you need to implement. Select the desired startup project and
run it on the emulator/simulator or device of your choice (Android,
Windows, iOS/MacCatalyst).

### 6. Pull new exercises

When the teacher publishes a new exercise, pull it from upstream:

    git pull upstream main

This adds the new folder to your solution without affecting your existing
work (published exercises are never modified after release).

### 7. Commit and push

    git add .
    git commit -m "Complete Task1"
    git push origin main

## Project structure

The repository contains lecture example projects and exercise (task)
projects, each as its own .NET MAUI application within a shared solution.

    CSP26_OnLecture_MAUI/
    ??? CSP26_OnLecture_MAUI.sln
    ??? HelloWorld/          # example project shown during lecture
    ??? Task1/               # exercise implementation

| Folder | Description |
|--------|-------------|
| `HelloWorld/` | Example MAUI project demonstrated during lecture |
| `Task N/` | Exercise N implementation (contains `TODO` comments) |

More lecture example and task folders will appear here as the course progresses.

## License

This repository is for educational use only.