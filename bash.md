```
## assumes origin remote
set filter = 'filter'
git branch -r | grep $filter | while read rep; do git push --delete origin ${rep:7} ; done
```
