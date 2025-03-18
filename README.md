# ZOH Git Basics Notes (COMPLETED)

This document provides step-by-step instructions for setting up Git on your PC, configuring your Git account, and connecting a local repository to a remote repository.

---

## 1. Set Up Git on Your PC

### Create an SSH Key
1. **Generate an SSH Key:**
   - Open your terminal and run:
     ```bash
     ssh-keygen
     ```

2. **Copy the SSH Key:**

   - **Linux:**
     ```bash
     xclip -sel clip < ~/.ssh/id_rsa.pub
     ```
   - **Mac:**
     ```bash
     pbcopy < ~/.ssh/id_rsa.pub
     ```
   - **Windows:**
     ```bash
     cat ~/.ssh/id_rsa.pub | clip
     ```

3. **Add the SSH Key to GitHub:**
   - In your web browser, navigate to:
     - **GitHub** > **Profile Icon** > **Settings** > **SSH and GPG Keys** > **New SSH Key**
   - Paste your SSH key and save.

---

## 2. Configure Git Account on Your Device/Project

1. **Set Global User Email:**
   - Run the following command in the terminal:
     ```bash
     git config --global user.email "kcpersonalacc@gmail.com"
     ```

2. **Set Global User Name:**
   - Run the following command in the terminal:
     ```bash
     git config --global user.name "KCprsnlcc"
     ```

3. **Verify Git User Credentials:**
   - Check the configuration with:
     ```bash
     git config --global --list
     ```

---

## 3. Connect a Local Repository to a Remote Repository

1. **Initialize a Local Git Repository:**
   - Run:
     ```bash
     git init
     ```

2. **Check File Status:**
   - See the state of your files with:
     ```bash
     git status
     ```

3. **Add a Remote Repository:**
   - Add the remote URL (replace `<your-repo-url.git>` with your repository URL):
     ```bash
     git remote add origin <your-repo-url.git>
     ```

4. **Verify the Remote Connection:**
   - Check that the remote is correctly added:
     ```bash
     git remote -v
     ```

5. **Stage Files for Commit:**
   - Stage all files:
     ```bash
     git add .
     ```

6. **Create a Commit:**
   - Commit the staged files with a message:
     ```bash
     git commit -m "Initial commit"
     ```

7. **Push Local Repository to Remote Repository:**
   - Upload your commits to the remote repository:
     ```bash
     git push origin master
     ```
