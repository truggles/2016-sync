# 2016-sync
2016 incarnation of synchronisation

See here for instructions how to produce sync trees: https://twiki.cern.ch/twiki/bin/view/CMS/HiggsToTauTauWorking2016#Synchronisation

Please create a subfolder for a given analysis team, and add txt files (and sym links if you deem them useful) containing the latest sync files for a given channel and a short description (e.g. what's missing, what changed, etc)


# Some Git Pointers
Fresh checkout of this repository:
```
git clone -b azhSync git@github.com:truggles/2016-sync.git
```

Add a text file like described above, making changes to it is the same as intially committing it:
```
mkdir UW
cd UW
vi azh300_eemt_sync.txt # Edit it
git commit azh300_eemt_sync.txt -m "Newest sync file with great updates"
```

Before pushing your commit to GitHub, you need to make sure that you have all the current commits/work from azhSync
```
git pull --rebase
```
This will pull in all changes from GitHub and will apply your new commit after them (you can also do this just to get updates if you haven't made a commit recently).  Now that you have the latest version of what's online:

```
git push
```

If you have checked out multiple branches, you might have to:
```
git push origin azhSync
```

