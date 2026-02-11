# 🧬 TDP-43 Project - Complete GitHub Guide

**For:** Rahma, Ahmed, Omar, Zahra  
**By:** Almokhtar  
**Updated:** February 11, 2026

---

## 📋 Table of Contents

1. [One-Time Setup](#one-time-setup)
2. [Daily Workflow](#daily-workflow)
3. [Where to Put Your Files](#where-to-put-your-files)
4. [Practice Exercise](#practice-exercise)
5. [Common Commands](#common-commands)
6. [Troubleshooting](#troubleshooting)

---

## 🔧 ONE-TIME SETUP

### Step 1: Check if You Have Git

Open Terminal and run:
```bash
git --version
```

**If you see version number** (like `git version 2.39.0`):  
✅ You have git! Skip to Step 2.

**If you see "command not found":**  
Install git:
- **Mac/Linux:** `brew install git`
- **Windows:** Download from https://git-scm.com

---

### Step 2: Install GitHub CLI & Login
```bash
# Install GitHub CLI
brew install gh

# Login to GitHub
gh auth login
```

**When it asks questions:**
1. What account? → **GitHub.com** (press Enter)
2. Protocol? → **HTTPS** (press Enter)
3. Authenticate? → **Yes** (press Enter)
4. How? → **Login with a web browser** (press Enter)

**Follow prompts:**
- Copy the code shown (8 characters like `ABCD-1234`)
- Press Enter (browser opens)
- Paste code in browser
- Click "Authorize"

**You should see:** ✓ Logged in as [your-username]

---

### Step 3: Configure Git (Tell it who you are)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

**Example:**
```bash
git config --global user.name "Rahma"
git config --global user.email "rahma@example.com"
```

---

### Step 4: Clone the Project
```bash
# Go to Desktop
cd ~/Desktop

# Download the project
git clone https://github.com/almokhtar8-stack/tdp43-dysfunction-score.git

# Enter the folder
cd tdp43-dysfunction-score

# Check you're in the right place
pwd
```

**Should show:** `/home/[yourname]/Desktop/tdp43-dysfunction-score` or similar

---

### Step 5: Test Your Access
```bash
# Make a small test
echo "- Your Name (tested successfully!)" >> CONTRIBUTORS.md

# Add it
git add CONTRIBUTORS.md

# Commit
git commit -m "test: add my name to contributors"

# Push
git push origin main
```

**If this works without errors → You're all set!** ✅

---

## 🔄 DAILY WORKFLOW

**Every time you work, follow these steps:**

---

### BEFORE You Start Working
```bash
# 1. Navigate to project folder
cd ~/Desktop/tdp43-dysfunction-score

# 2. Get latest changes from team
git pull origin main
```

**This downloads any work your teammates pushed.**

---

### WHILE You're Working

#### Option A: Edit Existing File
```bash
# Open file in editor
nano scripts/03_differential_expression/my_script.R

# Make your changes
# Press Ctrl+O to save
# Press Enter to confirm
# Press Ctrl+X to exit
```

#### Option B: Create New File
```bash
# Create new script
nano scripts/05_ml_modeling/my_new_script.py

# Write your code
# Press Ctrl+O to save
# Press Enter
# Press Ctrl+X to exit
```

---

### Test Your Code Works!
```bash
# For R scripts
Rscript scripts/03_differential_expression/my_script.R

# For Python scripts
python scripts/05_ml_modeling/my_script.py
```

**⚠️ IMPORTANT: Only push code that works!**

---

### AFTER You Finish Working
```bash
# 1. Check what you changed
git status

# 2. See detailed changes (optional)
git diff

# 3. Add your files
git add .

# OR add specific files:
# git add scripts/03_differential_expression/my_script.R
# git add results/figures/my_plot.png

# 4. Commit with a descriptive message
git commit -m "add genome-wide DESeq2 analysis - found 247 DEGs"

# 5. Push to GitHub
git push origin main
```

---

### Notify Team

**Post in WhatsApp:**
```
✅ Finished [task name]!

Pushed to GitHub:
- scripts/03_differential_expression/genome_wide_deseq2.R
- results/figures/volcano_plot.png

Found 247 significant DEGs!
```

---

## 📁 WHERE TO PUT YOUR FILES

### RAHMA (Data Analysis Lead)

**Your scripts go in:**
```
scripts/03_differential_expression/
  - genome_wide_deseq2.R
  - quality_checks.R

scripts/04_visualization/
  - volcano_plot.R
  - heatmap.R
  - pca_plot.R
```

**Your results go in:**
```
results/tables/
  - genome_wide_degs.csv
  - normalized_counts.csv

results/figures/
  - volcano_plot.png
  - heatmap.png
  - pca_samples.png
```

---

### AHMED (ML Modeling)

**Your scripts go in:**
```
scripts/05_ml_modeling/
  - build_dysfunction_model.py
  - evaluate_models.py
  - predict_scores.py
```

**Your results go in:**
```
results/tables/
  - model_performance.csv
  - dysfunction_scores.csv
  - feature_importance.csv

results/figures/
  - roc_curves.png
  - confusion_matrix.png

results/models/
  - (large model files go to Google Drive, not GitHub)
```

---

### OMAR (Pathway Analysis)

**Your scripts go in:**
```
scripts/06_enrichment_analysis/
  - go_enrichment.R
  - kegg_pathways.R
  - visualize_enrichment.R
```

**Your results go in:**
```
results/tables/
  - go_enrichment_results.csv
  - kegg_pathways.csv

results/figures/
  - go_barplot.png
  - pathway_diagram.png

docs/
  - gene_biological_interpretation.md
```

---

### ZAHRA (Documentation & Writing)

**Your files go in:**
```
docs/
  - methods.md
  - results.md
  - discussion.md
  - references.bib

notebooks/
  - manuscript_draft.Rmd
```

---

### ALMOKHTAR (Project Lead)

**Your files go in:**
```
scripts/integration/
  - combine_chromosomes.R
  - final_integration.R

docs/
  - meeting_notes.md
  - project_timeline.md
```

---

## 🎯 PRACTICE EXERCISE

**Let's practice the workflow with a test edit!**

### Exercise: Edit the README
```bash
# 1. Navigate to project
cd ~/Desktop/tdp43-dysfunction-score

# 2. Get latest
git pull origin main

# 3. Open README
nano README.md

# 4. Scroll to the very bottom (use arrow keys)

# 5. Add this line at the end:
#    - [Your Name] - Completed GitHub setup ✅

# 6. Save and exit
#    Press Ctrl+O, then Enter, then Ctrl+X

# 7. Check what changed
git status

# 8. Add the file
git add README.md

# 9. Commit
git commit -m "test: add my name to README practice section"

# 10. Push
git push origin main

# 11. Check on GitHub website!
#     Go to: https://github.com/almokhtar8-stack/tdp43-dysfunction-score
#     Scroll to bottom of README
#     You should see your change!
```

**If you see your change on the website → SUCCESS!** 🎉

---

## 📚 COMMON COMMANDS CHEAT SHEET

### Navigation
```bash
cd ~/Desktop/tdp43-dysfunction-score    # Go to project
pwd                                     # Where am I?
ls                                      # List files
ls -la                                  # List all (including hidden)
```

### Git Basics
```bash
git status                              # What changed?
git pull origin main                    # Get latest from team
git add .                               # Add all changes
git add path/to/file.R                  # Add specific file
git commit -m "message"                 # Save changes locally
git push origin main                    # Upload to GitHub
```

### Git Information
```bash
git log                                 # See commit history
git log --oneline                       # See short history
git diff                                # See what you changed
git diff filename.R                     # See changes in specific file
```

### File Editing
```bash
nano filename.R                         # Open/create file
# Inside nano:
#   Ctrl+O = Save
#   Ctrl+X = Exit
#   Ctrl+K = Cut line
#   Ctrl+U = Paste line
```

### Conda
```bash
conda activate genomics                 # Activate environment
conda deactivate                        # Deactivate
conda env list                          # List environments
```

---

## 🆘 TROUBLESHOOTING

### Problem: "Permission denied"

**Solution:**
```bash
gh auth login
# Go through authentication again
```

---

### Problem: "Your branch is behind 'origin/main'"

**Solution:**
```bash
git pull origin main
# This gets the latest changes
# Then try your push again:
git push origin main
```

---

### Problem: "Merge conflict"

**What happened:** You and someone else edited the same lines in the same file.

**Solution:**
```bash
# 1. Open the conflicted file
nano conflicted_file.R

# 2. Look for these markers:
#    <<<<<<< HEAD
#    Your changes
#    =======
#    Their changes
#    >>>>>>> origin/main

# 3. Decide what to keep:
#    - Keep your version, OR
#    - Keep their version, OR
#    - Keep both (merge them)

# 4. Delete the markers (<<<, ===, >>>)

# 5. Save the file (Ctrl+O, Enter, Ctrl+X)

# 6. Add, commit, push
git add conflicted_file.R
git commit -m "resolve merge conflict"
git push origin main
```

**OR ask in WhatsApp:** "Hey, I got a merge conflict in [filename], can someone help?"

---

### Problem: "Nothing to commit"

**What it means:** No changes detected.

**Check:**
```bash
git status
```

**Make sure:**
- You saved your file (Ctrl+O in nano)
- You're in the right directory (`pwd`)

---

### Problem: "Failed to push"

**Possible causes:**

1. **No internet connection**
   - Check your wifi

2. **Someone else pushed first**
```bash
   git pull origin main
   git push origin main
```

3. **Authentication expired**
```bash
   gh auth login
```

---

### Problem: "I pushed wrong code by mistake!"

**Don't panic! You can fix it:**

**Option 1: Fix and push again**
```bash
# Edit the file to fix it
nano scripts/my_script.R

# Add, commit, push the fix
git add scripts/my_script.R
git commit -m "fix: correct error in my_script"
git push origin main
```

**Option 2: Ask Almokhtar to help**
Post in WhatsApp: "I pushed broken code, can you help me fix it?"

---

## ✅ GOOD PRACTICES

### ✅ DO:
- Pull before you start working
- Test your code before pushing
- Write clear commit messages
- Push regularly (don't wait weeks)
- Ask questions in WhatsApp
- Help teammates when they're stuck

### ❌ DON'T:
- Push code that doesn't work
- Use vague commit messages ("update", "fix", "work")
- Work for weeks without pushing
- Edit files directly on GitHub website (use terminal)
- Panic if something goes wrong (we can fix it!)

---

## 💬 COMMIT MESSAGE EXAMPLES

### Good Messages ✅
```bash
git commit -m "add genome-wide DESeq2 analysis script"
git commit -m "fix normalization bug in DESeq2"
git commit -m "add volcano plot for 247 DEGs"
git commit -m "draft methods section"
git commit -m "update README with new team roles"
```

### Bad Messages ❌
```bash
git commit -m "update"           # What was updated?
git commit -m "fix"              # What was fixed?
git commit -m "work"             # What work?
git commit -m "changes"          # What changed?
git commit -m "asdf"             # Not descriptive at all
```

---

## 🎓 LEARNING RESOURCES

### Quick References
- This guide (you're reading it!)
- Git documentation: https://git-scm.com/doc
- GitHub guides: https://guides.github.com

### Video Tutorials
- Git & GitHub for Beginners: https://www.youtube.com/watch?v=RGOj5yH7evk
- GitHub Desktop tutorial: https://www.youtube.com/watch?v=8Dd7KRpKeaE

### Practice
- Try editing different files
- Practice the full workflow multiple times
- Help teammates when they get stuck (teaching helps you learn!)

---

## 📞 GETTING HELP

### Where to Ask:
1. **WhatsApp group** (fastest!)
2. **Almokhtar** (project lead)
3. **This guide** (search for your problem)

### What to Include When Asking:
- What command you ran
- What error message you got (copy-paste exact text)
- Screenshot if helpful

**Example good question:**
```
"Hi! I tried to push but got this error:
'error: failed to push some refs'

I already tried git pull. What should I do?"
```

---

## 🎉 YOU'RE READY!

**Checklist:**
- ✅ Git installed
- ✅ GitHub CLI authenticated
- ✅ Project cloned
- ✅ Test push successful
- ✅ Know where to put your files
- ✅ Practiced the workflow

**Now start working on your actual tasks!**

Remember:
- Pull before you work
- Test your code
- Push when done
- Help each other
- Ask questions!

**Happy coding! 🚀**

---

**Questions? Ask in WhatsApp group!**

**Found a mistake in this guide? Tell Almokhtar!**
