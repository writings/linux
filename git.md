Deleting and backdating tags
----------------------------

Fetch all from github (note, I never call it 'origin'):

`git fetch github --tags`

Delete a tag locally, then tell github we deleted it:

`git push github :TAG_NAME`

Backdate a tag:

`GIT_COMMITTER_DATE="2013-09-23 18:50" git tag -a v1.1.5 15a238`

