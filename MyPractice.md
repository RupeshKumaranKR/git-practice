Microsoft Windows [Version 10.0.26200.8655]
(c) Microsoft Corporation. All rights reserved.

C:\Users\Rupesh>cd D:\git-practice

C:\Users\Rupesh>ls
'ls' is not recognized as an internal or external command,
operable program or batch file.

C:\Users\Rupesh>cd /d D:\git-practice

D:\git-practice>git init
Initialized empty Git repository in D:/git-practice/.git/

D:\git-practice>echo "print('Hello, Git!')" > app.py

D:\git-practice>git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        app.py

nothing added to commit but untracked files present (use "git add" to track)

D:\git-practice>git add .

D:\git-practice>git commit -m "Initial commit: Added app.py"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'Rupesh@DESKTOP-C8G14PG.(none)')

D:\git-practice>git config --global user.email "rupeshkumaran@gmail.com"

D:\git-practice>git config --global user.name "RupeshKumaranKR"

D:\git-practice>git commit -m "Initial commit: Added app.py"
[master (root-commit) 07d2011] Initial commit: Added app.py
 1 file changed, 1 insertion(+)
 create mode 100644 app.py

D:\git-practice>git remote add origin https://github.com/RupeshKumaranKR/git-practice.git

D:\git-practice>git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/RupeshKumaranKR/git-practice.git'

D:\git-practice>git branch -M main

D:\git-practice>git push -u origin main
info: please complete authentication in your browser...
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 252 bytes | 84.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/RupeshKumaranKR/git-practice.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

D:\git-practice>git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

D:\git-practice> git add .

D:\git-practice>git commit -m "Updated app.py with new features"
[main 449da1b] Updated app.py with new features
 2 files changed, 2 insertions(+), 1 deletion(-)
 create mode 100644 new feauture added.txt

D:\git-practice>git push
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 389 bytes | 389.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/RupeshKumaranKR/git-practice.git
   07d2011..449da1b  main -> main

D:\git-practice>git clone https://github.com/RupeshKumaranKR/machone.git
Cloning into 'machone'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (6/6), done.

D:\git-practice>git pull
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 1003 bytes | 9.00 KiB/s, done.
From https://github.com/RupeshKumaranKR/git-practice
   449da1b..73e12fb  main       -> origin/main
Updating 449da1b..73e12fb
Fast-forward
 app.py | 1 +
 1 file changed, 1 insertion(+)

D:\git-practice>git log
commit 73e12fb370fd5e1e9fb3cf70cf17890d5efea6d4 (HEAD -> main, origin/main, origin/HEAD)
Author: RupeshKumaranKR <rupeshkumaran@gmail.com>
Date:   Sun Jun 14 17:03:47 2026 +0530

    Add print statement for GitHub edit message

commit 449da1b29a75e250c81942899fc431c8dee3f20d
Author: RupeshKumaranKR <rupeshkumaran@gmail.com>
Date:   Sun Jun 14 16:54:53 2026 +0530

    Updated app.py with new features

commit 07d2011131fa26ec05b3f1b460ede69086889b4f
Author: RupeshKumaranKR <rupeshkumaran@gmail.com>
Date:   Sun Jun 14 16:28:09 2026 +0530

    Initial commit: Added app.py

D:\git-practice>
