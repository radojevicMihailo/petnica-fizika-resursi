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


1. Open Command Prompt (`cmd`) or PowerShell.
2. Download the Git installer:
   ```powershell
   curl -L -o git-installer.exe https://github.com/git-for-windows/git/releases/download/v2.47.1.windows.2/Git-2.47.1.2-64-bit.exe
3. Run installer:
   ```powershell
   start git-installer.exe
   ```
4. Follow the installation prompts (default settings are fine).
5. Update github to the latest version:
   ```powershell
   git update-git-for-windows
   ```
6. Verify the installation:
    ```powershell
    git --version
    ```
---

## Step 2: Install Miniconda

1. Download the Miniconda installer:
   ```powershell
   curl -o miniconda-installer.exe https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe
   ```
2. Install Miniconda:
   ```powershell
   start miniconda-installer.exe
   ```
3. Follow the prompts and select "Add Miniconda to PATH" during installation.

---

## Step 3: Install Visual Studio Code

1. Download VS Code:
   ```powershell
   curl -L -o vscode-installer.exe "https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user"
   ```
2. Run installer:
   ```powershell
   start vscode-installer.exe
   ```

---

## Step 4: Create Project Directory Structure

1. Create the `petnica_projects` directory:
   ```powershell
   mkdir C:\Users\<username>\petnica_projects\project_2025\data_dir
   ```
2. Navigate to the project folder:
   ```powershell
   cd C:\Users\<username>\petnica_projects\project_2025
   ```

---

## Step 5: Initialize Git Repository

1. Initialize the Git repository:
   ```powershell
   git init project_2025
   ```
2. Move into the repository:
   ```powershell
   cd project_2025
   ```
3. Add a `.gitignore` file:
   ```powershell
   echo "data_dir/" > .gitignore
   git add .gitignore
   git commit -m "Initial commit with .gitignore"
   ```
4. Add a README file:
   ```powershell
   echo "# Project 2025" > README.md
   git add README.md
   git commit -m "Add README file"
   ```

---

## Step 6: Set Up Conda Virtual Environment

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

## Step 7: Test the Setup

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