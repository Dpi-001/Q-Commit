# QCommit – Developer Instant Git Assistant for VS Code

**QCommit** is a developer-first, lightweight Visual Studio Code extension that enables you to **initialize Git**, **commit only what matters**, and **collaborate with your team** — all via **keyboard shortcuts** and intuitive menus.

Whether you're launching a new repo or contributing to a fast-moving team project, **QCommit** removes Git friction so you can focus on what truly matters: **shipping great code**.

---

## Key Features

| Feature                | Description                                                                                   |
|------------------------|-----------------------------------------------------------------------------------------------|
| **Git Detection**      | Detects if the current workspace is a Git repository                                          |
| **Auto Git Init**      | Initializes Git if no .git folder exists                                                    |
| **Smart File Staging** | Detects file changes and prompts for staging: auto if 1, selectable if many                   |
| **Stage One or Many**  | Commit a single file or choose multiple with a "Select All" option                            |
| **Commit Prompt**      | Ask for a commit message or apply a smart default                                             |
| **Auto Push**          | Pushes to the current checked-out branch (if a remote is set)                                |
| **Shortcut Workflow**  | Ctrl+Shift+Q / Cmd+Shift+1 – Quick Commit                                                |
| **Admin Menu**         | Ctrl+Shift+A / Cmd+Shift+2 – Main-only branch actions                                    |
| **Team Menu**          | Ctrl+Shift+T / Cmd+Shift+6 – Team Git features (commit, branch, pull, etc.)              |
| **One-Command Flow**   | All Git operations handled via Command Palette and smart prompts                              |

---

## Why Use QCommit?

- **Zero-Setup Git Start** – Initialize a new Git repo instantly  
- **Commit Only What Matters** – Especially useful in large codebases  
- **Smart Commit Logic** – Stage one, many, or all changed files  
- **Push Without Distractions** – No need to open terminal  
- **Stay in Control** – Choose your files, your message, your branch  

---

## Requirements

- Git is installed and added to your system PATH  
- You have created a GitHub repository (required for pushing in main mode)  

---

# 📘 How It Works — Step-by-Step

| Shortcut (Windows)  | Shortcut (Mac)  | Action                            | Jump to Section                                                                                 |
|--------------------|-----------------|----------------------------------|-----------------------------------------------------------------------------------------------|
| Ctrl+Shift+Q       | Cmd+Shift+1     | 🚀 Quick Commit                  | [Quick Commit](#quick-commit)                                                                 |
| Ctrl+Shift+A       | Cmd+Shift+2     | 🛠️ Admin Git Menu *(main only)*  | [Admin Git Workflow](#admin-git-workflow)                                                     |
| Ctrl+Shift+T       | Cmd+Shift+6     | 👥 Team Git Menu *(custom only)* | [Team Collaboration Workflow](#team-collaboration-workflow)                                   |

---

## [Quick Commit](#quick-commit)  

### 📁 [STEP 1] Create & Open an Empty Folder in VS Code  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### 🆕 [STEP 2] VS Code activates (shows Welcome / Untitled tab)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### 🎯 [STEP 3] Press Cmd+Shift+1 (Mac) / Ctrl+Shift+Q (Windows)  

### 🔍 [STEP 4] Branch Type Setup (Only on First Use)

If no Git is initialized, you’ll be prompted to select a branch type:

| Branch Option       | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| 🌟 **Main Branch**   | ✅ **Recommended for professional GitHub users**<br>- Setup new project<br>- Create README.md, init Git, enter project name<br>- Add remote URL<br>- First commit → Push to GitHub<br>- Marker created: .qcommit/.main.qcommit |
| 🌿 **Custom Branch** | For local-only feature/experimental work<br>- Create project-specific branch<br>- Marker created: .qcommit/.custom.qcommit<br>⚠️ Cannot push directly to GitHub |

> ✅ **If Git is already initialized** (e.g. existing repo or you’ve run git init before),  
> this step is **skipped** and the shortcut takes you **straight to commit options**.

### ✍️ [STEP 5] Write Code → Save Your File(s)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### 🎯 [STEP 6] Press the Shortcut Again (Cmd+Shift+1 / Ctrl+Shift+Q)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### 📤 [STEP 7] Choose Commit Type:

| Option               | Description                                        |
|----------------------|----------------------------------------------------|
| 📄 **Only This File** | Commit only the currently open and saved file *(Main only)* |
| 🗃️ **All Changes**    | Commit all modified and new files *(Main & Custom)* |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### 📝 [STEP 8] Enter Your Commit Message  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### 🚀 [STEP 9]  
- 🌟 **Main** → Commit & **Push** to GitHub  
- 🌿 **Custom** → Commit **Locally Only**  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
### ✅ [DONE] Git Workflow Complete!

---

### 🧠 Pro Tip:  
> **Always choose 🌟 Main Branch** when starting a new project.  
> It supports **GitHub integration**, **remote pushing**, and is perfect for team collaboration.

> 🌿 Custom branches are best for:  
> - Local-only work  
> - Feature/testing code  
> - Offline development

---

## [Admin Git Workflow](#admin-git-workflow)

# 🛠️ Admin Git Workflow — Ctrl+Shift+A / Cmd+Shift+2

When the admin triggers the command, the extension auto detects the branch type (main or custom) and shows options accordingly.

---

### 🔄 Workflow for Main Branch (.main.qcommit)

Admin presses **Ctrl+Shift+A / Cmd+Shift+2**  
→ Extension auto detects .main.qcommit marker.

Admin chooses:

- ⭐ **Show Current Branch** — View the current active branch (usually main).  
- 🌿 **Switch to Branch** — Switch to any local or remote branch (e.g., origin/feature-xyz) to review team members’ changes.  
- 🔄 **Fetch Remote Branches** — Update the list of branches from the remote repo (GitHub).  
- 🔀 **Merge Team Branch into Main & Push** —  
  - Select a remote team branch (origin/branchname) to merge.  
  - Merge the chosen branch into main.  
  - Push the updated main branch back to GitHub (origin).  
  - Delete the merged remote branch from GitHub after successful merge.

After merge & deletion, team members pull the updated main branch on their local machines to get the latest integrated code.

---

### 🌿 Workflow for Custom Branch (.custom.qcommit)

Team sees limited options:

- ⭐ **Show Current Branch**  
- 🌿 **Switch to Branch**

Custom branches are for local/experimental work, so no merging or pushing is available.

---

## [Team Collaboration Workflow](#team-collaboration-workflow)

# Team Collaboration Workflow — Step by Step — Ctrl+Shift+T / Cmd+Shift+6

### Initial Setup & Cloning (Admin → Team)

1. Admin sends collaborator invitations to the team repository.  
2. Collaborators accept the invitation.  
3. Team member prepares to clone the repository:  
   - Check if the current folder is empty.  
   - **If the folder is NOT empty or is inside an existing .git repo, do NOT clone here.**  
   - Instead, create a new folder in the parent directory for cloning.  
4. Team member copies the repository URL from the admin's repo.  
5. Team member pastes the URL and clones the repository successfully.  
6. After cloning:  
   - Press Esc once to go back in dialogs/menus if needed.  
   - Press Esc twice quickly (double Esc) to exit completely.  
   - Confirm exit when prompted to avoid accidental closure.

---

### Setting Up Custom Branch (Team Member)

7. Press Ctrl+Shift+Q (or Cmd+Shift+1) to open the custom branch menu.  
8. Choose or create a custom branch — this creates the .qcommit/.custom marker locally.  
9. Press Ctrl+Shift+T (or Cmd+Shift+6) to open the team Git action menu.  
10. Switch to the desired branch for working on features or fixes.  
11. Commit changes **only through** the Ctrl+Shift+T (or Cmd+Shift+6) menu.  
    - **Important:** Committing is NOT allowed via the custom branch menu (Ctrl+Shift+Q / Cmd+Shift+1).  
12. After committing, the system automatically switches the branch back to main after approximately 5 seconds.

---

### Admin Workflow & Post-Commit Steps

13. Admin uses Ctrl+Shift+A (or Cmd+Shift+2) to manage branches with limited options for custom branches:  
    - Show Current Branch  
    - Switch to Branch  
14. Team members pull the updated main branch from the remote repository.  
15. After merging, team members are prompted to delete their custom branches locally because:  
    - Merged branches are no longer needed.  
    - Deleting branches frees their names for future use.  
16. Team members may create new branches with the same name if necessary.

---

### Important Notes & Restrictions

- Cloning must be done **outside** any existing .git repository folders.  
- .qcommit folders and marker files are used locally to track branch types.  
- Commits must only be performed via the team Git menu (Ctrl+Shift+T / Cmd+Shift+6).  
- The custom branch menu (Ctrl+Shift+Q / Cmd+Shift+1) does NOT allow committing.  
- Use single Esc to go back in menus; use double Esc to exit with a confirmation prompt.

This step-by-step workflow helps keep the team’s Git workflow clean, avoids conflicts, and ensures admins maintain control over merges and branch management.

---

# Resources & Next Steps

- Learn how to use QCommit in real-world scenarios  
- See [How It Works – Step by Step](#how-it-works-step-by-step)

---

# Developers

- 👨‍💻 **Sudeep Lamichhane**  
- 👩‍💻 **Nishma Lamichhane**

---

# Contributors & Support

- 🏢 [**Bitmap IT Solution**](https://www.bitmapitsolution.com)  
  _Early inspiration and project direction._

---

# License

Licensed under the **LICENSE.md** — free to use for personal or commercial projects.  
❗ Modification or redistribution of any part of the source code is strictly prohibited without written permission from **Sudeep Lamichhane**

---

# Support the Project

If **QCommit** saves your time or improves your Git workflow:

- ⭐ Star the GitHub repo  
- 🐛 Report issues or suggest new features  
- 📢 Share with your dev friends or team  

---

> ✨ Let **QCommit** handle the Git routine.  
> 🚀 You stay focused and ship faster.
