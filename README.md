# learn-gitflow
Learn how to implement Git flow on GitHub so I can manage my project/repo versioning properly.

1. Build repo on Github
2. Clone the repo URL that you already created, then clone it with:
- git clone URL
3. CD to your clone folder and init with:
- git flow init
4. push your current branch (development) to the origin
- git push --set-upstream origin development
5. To start to add feature flow, first, you need to add first feature branch:
- git flow feature start feature_branch_name
- then ur local repo would look like this
• development
• *feature/feautre_branch
• main
6. Add some codes/features attach to this branch so you can commit and push it into this feature branch later
7. If you already complete the feature that you working on, then commit and are ready to push, type this command:
- git flow feature finish feature_branch_name
So, the feature_branch that u made it before will be deleted locally and merged into the development branch
8. Update development branch with git push origin
9. If you want to release the release version branch, you can start with
- git flow release start '0.1.0'
10. In your local git, the branch would look like this:
• development
• main
•  *release/0.1.0
11. Then u push to its origin so on your repo it has release/0.1.0 branch
- git push --set-upstream origin release/0.1.0
12. If you want to change some files in previous release branch you can do it as usual, for this case I add release-fix.html in the release/0.1.0 branch
13. After it finally FIXED release version, then merge it into development and master/main branch (optional you can delete this release branch as well):
- git flow release finish '0.1.0'
14. After the command there is pop-up notepad or text editor to edit the tag, to confirm you where this release version to merge, and write message.
15. git push origin
16. git tag -l (to check release version that merge into main branch)
