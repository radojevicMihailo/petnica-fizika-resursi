# Setup Guide for Signal and Image Processing Seminar (macOS)

This guide provides step-by-step instructions for setting up a uniform environment for signal and image processing. The setup will include:
- Git
- Miniconda
- Visual Studio Code
- A Git repository for the project

The project directory structure will be:
```
~/petnica_projects/project_2025/
├── data_dir/         # For storing datasets
└── project_2025/     # Git repository for the project
```

---

## Step 1: Install Git

1. Open the Terminal.
2. Install Git via Homebrew (if not installed):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   brew install git
   ```
3. Verify the installation:
   ```bash
   git --version
   ```

---

## Step 2: Install Miniconda

1. Download the Miniconda installer:
   ```bash
   curl -o miniconda-installer.sh https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
   ```
2. Install Miniconda:
   ```bash
   bash miniconda-installer.sh
   ```
3. Follow the prompts to complete the installation and restart your terminal.

## Step 3: Add Miniconda to the path

1. Type in "Edit enviroment variables" in windows bar and open it
2. In user variables, click on path, and then click edit
3. Add "C:\Users\<username>\miniconda3\Scripts" and "C:\Users\<username>\miniconda3" to the path

---

## Step 4: Install Visual Studio Code

1. Download VS Code:
   ```bash
   curl -o vscode-installer.zip https://code.visualstudio.com/sha/download?build=stable&os=darwin-universal
   ```
2. Unzip and move it to the Applications folder:
   ```bash
   unzip vscode-installer.zip -d /Applications
   ```

---

## Step 5: Create Project Directory Structure

1. Create the `petnica_projects` directory:
   ```bash
   mkdir -p ~/petnica_projects/project_2025/data_dir
   ```
2. Navigate to the project folder:
   ```bash
   cd ~/petnica_projects/project_2025
   ```

---

## Step 6: Initialize Git Repository

1. Initialize the Git repository:
   ```bash
   git init project_2025
   ```
2. Move into the repository:
   ```bash
   cd project_2025
   ```
3. Add a `.gitignore` file:
   ```bash
   echo "data_dir/" > .gitignore
   git add .gitignore
   git commit -m "Initial commit with .gitignore"
   ```
4. Add a README file:
   ```bash
   echo "# Project 2025" > README.md
   git add README.md
   git commit -m "Add README file"
   ```

---

## Step 7: Set Up Conda Virtual Environment

1. Create a new Conda virtual environment:
   ```bash
   conda create -n project_2025 python=3.10 -y
   ```
2. Activate the environment:
   ```bash
   conda activate project_2025
   ```
3. Verify the environment is active:
   ```bash
   python --version
   ```

---

## Step 8: Test the Setup

1. Check the folder structure:
   ```bash
   tree ~/petnica_projects/project_2025
   ```
   Expected structure:
   ```
   petnica_projects/
   └── project_2025/
       ├── data_dir/
       └── project_2025/ (Git repo)
   ```

---

Repeat these steps for each student's laptop to ensure uniformity. Let the tutors know the directory structure to easily locate files.