# Git Commands Cheat Sheet

| Command | Explanation (Hindi-English) |
|---------|------------------------------|
| `git init` | नया Git repo शुरू करता है (Initialize new repository). |
| `git clone <url>` | Remote repo की copy local machine पर लाता है (Download repo). |
| `git status` | Current branch की स्थिति दिखाता है (Changes, staged files). |
| `git add <file>` | File को staging area में डालता है (Prepare for commit). |
| `git commit -m "msg"` | Staged changes को repo में save करता है (Snapshot with message). |
| `git log` | Commit history दिखाता है (Timeline of changes). |
| `git diff` | Changes का अंतर दिखाता है (Compare working vs staged). |
| `git branch` | Branches की list दिखाता है / नई branch बनाता है (Manage branches). |
| `git checkout <branch>` | किसी branch पर switch करता है (Move to branch). |
| `git merge <branch>` | दूसरी branch के changes को current branch में जोड़ता है (Combine work). |
| `git remote -v` | Remote repos की list दिखाता है (Connected remotes). |
| `git push origin <branch>` | Local commits को remote repo पर भेजता है (Upload changes). |
| `git fetch origin` | Remote से नया data लाता है, लेकिन merge नहीं करता (Safe update). |
| `git pull origin <branch>` | Remote से data लाता है और तुरंत merge कर देता है (Update + merge). |
| `git reset <file>` | File को staging area से हटाता है (Unstage changes). |
| `git reset --hard <commit>` | Repo को किसी commit पर reset करता है (Discard changes). |
| `git revert <commit>` | किसी commit को undo करता है, नया commit बनाकर (Safe undo). |
| `git tag <name>` | किसी commit को tag करता है (Mark version). |
| `git stash` | Current changes को अस्थायी रूप से save करता है (Temporary save). |
| `git stash pop` | Stashed changes वापस लाता है (Restore work). |
| `git status` | Check if anything to commit/add. |
| `git log` | Check commit history. |
| `git revert <commit-id>` | Creates new commit that undoes changes made by given commit (e.g. `git revert 4ae73`). |
| `git reset <commit-id>` | Reset head back till given commit id (e.g. `git reset 4ae73`). |

---

# Advanced Git Commands Cheat Sheet

| Command | Explanation (Hindi-English) |
|---------|------------------------------|
| `git cherry-pick <commit-id>` | किसी specific commit को current branch में apply करता है (Pick single commit). |
| `git rebase <branch>` | Current branch को दूसरी branch के ऊपर reapply करता है (Rewrite history, cleaner merges). |
| `git rebase -i <commit-id>` | Interactive rebase → commits को squash, edit, reorder कर सकते हैं (History cleanup). |
| `git reflog` | HEAD और branch movements का पूरा log दिखाता है (Recover lost commits). |
| `git bisect start` | Bug खोजने के लिए binary search करता है (Find bad commit). |
| `git bisect good <commit-id>` | Marks a commit as good (Bug not present). |
| `git bisect bad <commit-id>` | Marks a commit as bad (Bug present). |
| `git submodule add <url>` | Repo के अंदर दूसरा repo जोड़ता है (Nested repo). |
| `git blame <file>` | File की हर line किस commit से आई है दिखाता है (Track authorship). |
| `git show <commit-id>` | किसी commit का detail दिखाता है (Changes + metadata). |
| `git clean -fd` | Untracked files और directories हटाता है (Clean workspace). |
| `git config --global user.name "Name"` | Global username सेट करता है (Identity setup). |
| `git config --global user.email "Email"` | Global email सेट करता है (Identity setup). |
| `git shortlog -sn` | Contributors की summary दिखाता है (Count commits per author). |
| `git archive --format=zip HEAD > repo.zip` | Current repo को zip archive बनाता है (Export snapshot). |
| `git bundle create repo.bundle HEAD` | Repo को bundle file में export करता है (Portable repo). |
| `git grep "pattern"` | Repo में किसी text को search करता है (Code search). |
| `git tag -a v1.0 -m "msg"` | Annotated tag बनाता है (Versioning with message). |
| `git push --tags` | सभी tags को remote पर भेजता है (Publish versions). |
| `git remote prune origin` | Remote branches जो delete हो चुके हैं उन्हें local से हटाता है (Clean remotes). |
| `git fsck` | Repo की integrity check करता है (Find corruption). |
| `git gc` | Garbage collection करता है (Optimize repo). |

---

## Quick Notes
- **`git rebase` vs `git merge`** → Rebase history को rewrite करता है, Merge नया commit बनाता है।  
- **`git cherry-pick`** → Useful जब सिर्फ एक commit चाहिए, पूरी branch नहीं।  
- **`git bisect`** → Debugging के लिए powerful tool है, bad commit जल्दी ढूँढने में मदद करता है।  
- **`git reflog`** → Lost commits recover करने का सबसे अच्छा तरीका।  

