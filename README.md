# Exercise: Creating Branches and Merging

This example will show you how to create branches to work on different features and how to merge changes from these branches into the main branch. Repeat this exercise to better understand and practice creating branches and merging.

## Step 1
Initialize a new Git repository and create a main branch:

```bash
mkdir exercise_05_branches
cd exercise_05_branches
git init
echo "Initial content" > main.txt
git add main.txt
git commit -m "Initial commit"
```

## Step 2
Create a new branch named *feature1*:

```bash
git branch feature1
```

## Step 3
Switch to the `feature1` branch and create a new file:

```bash
git checkout feature1
echo "Feature 1 content" > feature1.txt
git add feature1.txt
git commit -m "Added feature 1"
```

## Step 4
Switch back to `main` and create another branch from there:

```bash
git checkout main
git branch feature2
```

## Step 5
Switch to the `feature2` branch and create a new file:

```bash
git checkout feature2
echo "Feature 2 content" > feature2.txt
git add feature2.txt
git commit -m "Added feature 2"
```

## Step 6
Switch back to the main branch and add changes:

```bash
git checkout main
echo "Additional content in main" >> main.txt
git add main.txt
git commit -m "Updated main branch"
```

## Step 7
Merge the changes from `feature1` into the main branch:

```bash
git merge feature1
```

## Step 8
Merge the changes from `feature2` into the main branch:

```bash
git merge feature2
```

## Step 9
Check the commit history and the status of the files:

```bash
git log --oneline --graph --all
ls
```
