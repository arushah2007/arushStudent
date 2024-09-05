---
layout: page
title: Tools and Setup
description: Tools and Setup Page
hide: true
---

### 1. Terminal and File Management
   - I started with using the macOS Terminal to manage files and directories while using shell commands
   - I created a project directory `nighthawk` and cloned the repository using the command:
     `git clone https://github.com/nighthawkcoders/portfolio_2025.git`

### 2. Installing Developer Tools with Homebrew
   - I installed Homebrew using the command:
     `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
   - I confirmed the installation with `brew --version`

### 3. Setting Up Python Environment
   - I made a virtual environment using the `venv.sh` script given in the project
   - Activated the virtual environment with:
     `source venv/bin/activate`

### 4. Installing Python Packages
   - Once the environment was set up, I installed all the needed Python packages using:
     `pip install -r requirements.txt`

### 5. Ruby and Jekyll Setup
   - Since Jekyll is used for the GitHub Pages, I installed the Ruby packages with:
     `bundle install`

### 6. Launching the Local Server
   - To test my changes locally, I ran the command `make`, which started a local server. I verified my website by opening `http://127.0.0.1:4100/portfolio_2025/` in my browser

### 7. Syncing with GitHub
   - After making changes and testing locally, I used VSCode to commit and push my changes to GitHub
   - GitHub Pages automatically updated my site with the latest changes



