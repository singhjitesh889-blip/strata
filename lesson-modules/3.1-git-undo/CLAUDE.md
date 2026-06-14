# Lesson 3.1: Git — The Undo Button

We're about to install things that touch your files automatically.

Before we do that — you need to understand undo.

[G3: you know git — type /start-3-2]

---

## Git in Plain Language

Git is not a developer tool. It's a time machine for your files.

Every time you "commit," you're saving a snapshot. You can always go back to any snapshot.

In geology: every commit is a layer in the stratigraphic column. The record of what happened, preserved, readable, in order.

STOP: Let's set it up. Ask me to initialize git in the strata folder and make the first commit.

USER: Asks for git setup

ACTION: Run:
```bash
git init
git add .
git commit -m "initial strata setup — inherited chaos + all analysis files"
```
Show the output. Explain: "You just created your first stratigraphic layer. Everything in this folder is now saved."

---

STOP: [QUIZ] You just made a commit. Vikram deletes a file by accident. What do you type to get it back?

USER: Anything — git checkout / restore / I don't know

"Here's the move:
```bash
git log              # see all commits
git checkout [hash]  # go back to that snapshot
```
You don't need to memorize the commands. Just know: every commit = a snapshot you can return to."

---

## The Two Git Commands You Need

```bash
git add .           # stage everything
git commit -m "description of what changed"   # save the snapshot

git log             # see your history
git checkout [hash] # go back to any point
```

That's it. That's all you need for this course.

STOP: Make a test commit right now. Ask me to create a test file, then commit it.

USER: Asks / does it

ACTION: Create a file called test-commit.txt with one line: "This is a test commit to practice git." Then run git add . && git commit -m "test: practice commit". Then delete the file and show how to get it back with git checkout.

---

**Next up:** 3.2 — fault lines. Where the system starts moving itself.

STOP: Ready? Type /start-3-2

USER: /start-3-2

---

## Success Criteria
- [ ] git initialized in strata/
- [ ] First commit made with all existing files
- [ ] Student understands commit = snapshot = undo point
- [ ] Student practiced at least one commit
- [ ] Student ready to install hooks safely
