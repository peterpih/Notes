http://git-scm.com  
http://services.github.com/training

###Commands

**Show tracking branches**  

$ <b>git branch -vv</b>  <em># show local tracking branches  

$ git remote show origin

$ git status -sb

$ git for-each-ref --format='%(upstream:short)' $(git symbolic-ref -q HEAD) <em># gives the upstream as an answer</em>

###git diff   

$ <b>git diff --cached</b> <em>diff between staged and repo</em>

$ git diff SHA1 SHA2

###autosquash for when REBASING

$ git config --global rebase.autosquash true   <em># turns on</em>

$ git commit -m "squash!..."  
$ git commit -m "fixup!..."    
$ git commit -m "reword!..."   

