# Git Submodules – Simple README

## What is a Submodule?

A **Git submodule** is a Git repository **inside another Git repository**.

👉 Used when you want to reuse another project/library.

---

## When to Use Submodules?

* Common library shared by many projects
* External dependency you don’t want to copy

---

## Add a Submodule

```bash
git submodule add <repo-url> <folder-name>
```

Example:

```bash
git submodule add https://github.com/user/lib.git libs/lib
```

Then commit:

```bash
git commit -m "Add submodule"
```

---

## What Gets Added?

* A folder for the submodule
* A file called `.gitmodules`

---

## Clone Repo with Submodules

```bash
git clone --recurse-submodules <repo-url>
```

---

## Initialize Existing Submodules

```bash
git submodule init
git submodule update
```

---

## Update Submodule Code

```bash
cd submodule-folder
git pull origin main
cd ..
git add submodule-folder
git commit -m "Update submodule"
```

---

## Remove a Submodule (Basic)

```bash
git rm submodule-folder
git commit -m "Remove submodule"
```

---

## Key Points

* Submodules track a **specific commit**
* Parent repo doesn’t track submodule files
* You must update submodules manually

---
