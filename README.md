# exercicio01
MBA Cloud Computing &amp; Devops

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ echo 01 > arquivo.txt

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        arquivo.txt

nothing added to commit but untracked files present (use "git add" to track)

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git add .
warning: LF will be replaced by CRLF in arquivo.txt.
The file will have its original line endings in your working directory

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arquivo.txt

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git commit -m "git add example - arquivo.txt"
[main 790ea9e] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git diff arquivo.txt
warning: LF will be replaced by CRLF in arquivo.txt.
The file will have its original line endings in your working directory
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git add arquivo.txt
warning: LF will be replaced by CRLF in arquivo.txt.
The file will have its original line endings in your working directory

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git diff --staged arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git diff arquivo.txt
warning: LF will be replaced by CRLF in arquivo.txt.
The file will have its original line endings in your working directory
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git restore --staged arquivo.txt

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git commit -m "Adds restored arquivo.txt file from staging"
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git log --oneline
790ea9e (HEAD -> main) git add example - arquivo.txt
377e2ab (origin/main, origin/HEAD) Initial commit

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ echo "*.txt" > .gitignore

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git add .gitignore
warning: LF will be replaced by CRLF in .gitignore.
The file will have its original line endings in your working directory

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git commit -m "Adds .gitignore to ignore .txt files"
[main cacbc25] Adds .gitignore to ignore .txt files
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ echo "Step M new file" > novo.txt

maciel@DESKTOP-OVBQCIJ MINGW64 ~/OneDrive/Documentos/Cloud Computing & Devops/Workspace/Continuous-Integration-and-Continuous-Delivery/exercicio01 (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

