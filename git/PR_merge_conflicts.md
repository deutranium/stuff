# Review a PR and fix merge conflicts

`git`

Assume a PR from `source` to `destination`

``` git
git fetch origin
git checkout -b source origin/source
git merge destination
```

In case of no merge conflicts, your `source` branch will remain the same

but..(lol welcome to git)

you got merge conflicts and all the files with such conflicts will have something like

``` git
<<<<<<<
the current code from source branch
=======
the incoming code from destination branch
>>>>>>>
```

A good idea to check which all files have been affected is to do a `git status` and look at the untracked files. These will be the ones where the above looking stuff has been added

Check all these files, fix the code in any way you want anndd..

``` git
git merge destination
git push origin source
```

Your `source` branch will be updated and pushed to `origin` with all the fixes. Now you can merge PR normally

Tada!
