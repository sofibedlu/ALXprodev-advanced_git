# ALXprodev-advanced_git

This repository demonstrates advanced Git techniques and GitFlow best practices:

## 1. GitFlow Initialization
- **Install Git Flow**  
   ```bash
   sudo apt-get update
   sudo apt-get install git-flow

- **Initialize GitFlow**
    ```bash
    git flow init -d
- This creates and configures the master and develop branches and sets default prefix names for features, releases, and hotfixes.

## 2. Feature Branch Workflows
- **Create a Feature Branch**
    ```bash
    git flow feature start implement-feature

- Work on the Feature (e.g., create directories, edit files)
- **Publish the Feature to Remote**
    ```bash
    git flow feature publish implement-feature

- **Finish and Merge the Feature into develop**
    ```bash
    git flow feature finish implement-feature

## 3. Release Branch Workflows
- **Start a Release**
    ```bash
    git flow release start 1.0.0

- **Make Changes and Push**
    ```bash
    git add .
    git commit -m "Commit release changes"
    git flow release publish 1.0.0

- **Finish the Release**
    ```bash
    git flow release finish 1.0.0

- This merges the release into main and develop, creates a tag, and removes the release branch locally.

## 4. Git Hooks
- **Pre-Commit Hook**: Checks for specific conditions (e.g., each directory has a README).

- **Post-Merge Hook**: Logs activity whenever a merge completes into main.

## Commands Summary
-
    ```bash
    # Initial Setup
    git flow init -d
    
    # Feature Branch
    git flow feature start <feature-name>
    git flow feature publish <feature-name>
    git flow feature finish <feature-name>
    
    # Release Branch
    git flow release start <version>
    git flow release publish <version>
    git flow release finish <version>
    
    # Tag and Push
    git push origin --tags