###Commands

**Show tracking branches**
$ <b>git branch -vv</b>  <em># show local tracking branches  

$ git remote show origin

$ git status -sb

$ git for-each-ref --format='%(upstream:short)' $(git symbolic-ref -q HEAD) <em># gives the upstream as an answer</em>

