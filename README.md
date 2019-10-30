# Bootstrap

bootstrap 4.3.1 with basic index.html

all js files included  / no Internet required on localhost

# Test making {new-branch} master without merge

This in case {new-branch} is completely different and merge is not desired.

Making {new-branch} master:

1. Make a branch out of master and name it “master-duplicate”.
2. Make a branch out of {new-branch} and name it “{new-branch}-copy”.
3. In repository settings > branches (GitHub) change “Default branch” to point at “master-duplicate” (without this step, you will not be able to delete master - in next step).
4. Delete “master” branch - I did this step from source tree (you can do it from the CLI or Git browser)
5. On local repository, rename “{new-branch}” to “master” 
``` git branch -m {new-branch} master ```
and push to GitHub repository 
``` git push origin HEAD ```
(this will create a new “master” branch while “{new-branch}” will still exist).
6. In repository settings, change “Default branch” to point at “master”.
