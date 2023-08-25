#GIT FLOW

##FLOW INIT
1.git flow init
=>branch name for production 							= master
=>branch name for "next release" development 			= develop
=>enter next step

2.check branch -a
3.git push origin develop

##FEATURE
1.git flow feature start mademanik_fitur_add_onprogress
2.check git branch -a
3.create file : touch feature.html
4.git add .
5.git commit -m "add new feature completed"
6.git flow feature finish mademanik_fitur_add_onprogress (feature will automatically merge to develop)
7.check git branch -a (feature branch will deleted)
8.git push origin develop

##RELEASE
1.git flow release start '0.1.0'
2.check git branch -a
3.git push origin release/0.1.0 (release will available to remote repository)
4.create file : touch relase-fix.html
5.git add .
6.git commit -m "release fix"
7.git push origin release/0.1.0
8.git flow release finish '0.1.0' (release will automatically merge to master and develop)
  => merge branch release/0.1.0 into main 		: close text editor
  => write >> new tag 							: save and close text editor
  => merge tag 0.1.0 into develop 				: close text editor
9.check git branch -a (release will automatically deleted)
10.git checkout master
11.git push origin master
12.git checkout develop
13.git push origin develop

14.back to git checkout master
15.git tag -l : will show tag 0.1.0