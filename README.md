Hope you all doing well, by the end of this post you will have complete knowledge to start with git and also familiar on it,

⚡ **Git**
_It is a version control tool in short this maintains your code history_, you can take a real time scenario , Browser is a tool which stores your Browsing history

keep reading and you will know everything you need to know...

Create a Newfolder give it a name as you like and open in Git Bash or you can go with Command propmt,

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/p5jgb2db9sxe7ar9661r.png)

your bash will look something like this

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/30oha658dt9aoxxu9jwa.png)

If you are in command prompt make sure your are working in right directory.

Initialize git in this folder `git init`, it will create a empty repository in your local device

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sczojc4l7hh73mychigh.png)
Create a new file and open it with vscode ,it is my opinion you can also do it with atom, sublime, it's completely up to you, you will see master, It is a branch no need to worry about this now, I will explain in a while,
To create a file in command prompt use `echo >fileName`
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mtdb7n59o68qr9m79m85.png)
It will look similar to this,

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/84e3kn0ddtt12k8jr7r2.png)
Make some changes in the file and don't forget to save it

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2qzms3626gavmwkklo52.png)
sometimes we are the situation to make our bash looks clean, type `clear` and hit enter. For command prompt use `cls` and give enter

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qnvq9rn3c46h5enhttpf.png)

To check the status of our commits ,the info of file use `git status` it will show you the file which is tracked or untracked,
tracked denotes our file is staged and untracked denotes the file is not yet staged, Obviously we didn't commit anything so no commits will appear.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mhimncz88deyrk0sw0hu.png)
Now the real part begins, to make our changes as a history there are two steps:

1. staging the change

2. commit the change

To bring our changes to the staging area use `git add .`, you can replace period simple **.** with your file name to be staged, generally the period simple includes all the changes in to staging area

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2mm1ayqk9m1a2mx5524b.png)
To commit the changes of the staged file use `git commit -m "your commit message"` and it will show the number of changes and type of changes that are insertion or deletion to the file

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/20i54r8qth5sumait1vn.png)

> _This is similar to photo taking scenario in marriage reception, the people who want to take photo should come to stage , after taking photo it will save in the marriage album, **changes we need to save as history should be staged first and then commit .**_

Again we check our status it show you working tree clean ,

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/l8kaj2jvrwxb3yyaabgm.png)
Create another file and make changes check the status

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vmha8gn1nwtdpvvpfl73.png)

stage the changes

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8wwdfg7fjxlrptnltw93.png)
Type `git stash`, check the status of your commits again , it shows _nothing to commit working tree clean_,

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3tyv5ohp67hpr4mmjs7f.png)

Take a realtime scenario, if you are working on some kind of logical code in project and you commit the changes that might have issues, so you decide not to lose the changes but also keep it for future purpose, here we use `git stash`, stash is a hidden place where we can store our commits until it really needs.

Incase now you need the commits in stash area now, we need to bring it in staging area again using `git stash pop`

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m0fgdlo8quu2s0iicak7.png)

Now we can commit those changes and check status of our commits if you want,

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/86rz1bxypykaidqgh8n4.png)

To see all the commits which are recorded as history use `git log`

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/u3j949e9lupp3by7wxmk.png)

so far you are doing great !!!

To add our local folder or a local repository to Github, there are two steps

1. Create a Repository
   2.Add local repo to github

To create a new repository on github, repository(repo) is simply a storage area of all our file along with the commits respectively.

For creating a repo you should have account in github, so signUp and then follow along with me, if you already have an account login to your account , go to repository click new.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/la0eonei3hlxl6sr6j6v.png)
Give a name for your repo and click Create repository

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/s7ym699kg17dbhxqhv9m.png)
and now your screen will appear like this, github show you the steps here we need last two steps , because already we did up to commit,

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/iqvr3wvj8gr2tb4uj1mo.png)

Need to copy HTTPS or SSH link and work on it, word remote denotes you are working with URL, origin is basically your github account.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/c3ih0e2dkurqs12lmvyo.png)

To push the changes that we made in our local repo to github main repo

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/opsiqrzw2irf5o6p0knl.png)

Now go to github tab and refresh the browser and the magic happens, you are able to see the changes that we made in our local repo in main repo

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/dlxvnufv0a3mcwjtmqby.png)

Change something in file1 or file2 and stage the change , now if we want to restore changes we made stage it and check status

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6rv8tposncrkl86fgiwp.png)
and now use `git restore --staged fileName` , leave `--staged` flag to restore local changes too and check status

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y39madjupc0ukhoysjrb.png)

To remove the changes completely use `git rm --cached fileName`and check status

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xonyx5j1am5lh8wcfcef.png)

stage the file, commit it and check status, it shows your branch is ahead of origin/master by 1 commit and inform us to push the local commits, I know that's a lot, move forward you will feel awesome about git

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ay14gd9a7lsde4jnjun4.png)

As the status shows we need to push the changes and check status

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9igoia3ajy8vbuvo0k3s.png)

Go to your browser and refresh, you will be amazed, give an applause to yourself. Note the commit **_back to normal_** that is pushed from our local branch.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/g07s26xjoi2phl1xdv1c.png)

create another file make some changes, stage that and commit
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m0vbini09uyo906zjgr8.png)

See all the commit messages using `git log`.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rd7zd4ghvnkzjd0ep343.png)

**Structure of Commit messages**:
Commit messages are align on _top of one another_, To delete commit messages you need to pick the commitID and paste in `git reset commitID`, this will delete all the commits above the one which you pick.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zguix8tijdwz7xn87c4z.png)

I want this to be clean and understandable , for that delete file3.txt in my case , you may leave this

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hnyrpjmb5gw5ltmbo3wy.png)

To push our changes to github main repo `git push origin master`

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yhtolcx1q487e08j76ju.png)

It's time to know **HEAD**, this is simply a pointer which points to the active branch , you will understand more in a bit.

Now we are going to work on branches, to create a branch use `git branch branchName` and checkout this branch by `git checkout branchName`, after checking out the HEAD is now point to the new branchName, here after the commits we will made is from branchName

Create new branch , checkout then create a file and change something ,stage it and commit

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7tlvyxsnetaqkst153y1.png)
Make some more commits may be two is good to go and `git log` now

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m8lckpdue17g4ibmsuvh.png)

we need to push our change in local branch to github

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ot5epsup1379z6mv6jfr.png)

Now your github screen automatically shows you **Compare & pull request** , click on that

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1rod8nhxxx67t0zjnzel.png)

Now click on **create pull request**it will show you
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yf66ijib4stkpx5nj8ah.png)

Here if there is no conflict on your change can simply click on **Merge pull request**, _conflict_ is popularly known as _merge conflict_ , assume that two persons working on same change and commit it, github doesn't know which change to take in this case we manually make the change on github and then we are allowed
merge pull request
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2wy4pk8sjb43haxpndpc.png)

I know we done a lot but it's worth, now click confirm merge, there you can delete the branch if it is no longer needed
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/t6o1d31fmhi3mxcvd9l3.png)
Go to your code now and refresh the page you can see there will second branch and the file along with it's commit

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5ojaya19syy4onmmn7pm.png)
hope you feel the confidence on yourself, there is little more to do , for that need some changes in master branch may three commits are good to go , now `git log`, In sometimes we need to reduce number of commits as one commit, assume that you are working in login form of your project you will commit each changes and push it, those commits are points to single work so we squash all three to one commit, here we use `git rebase`, before that we need to pick the commit id , this has same hierarchy as `git reset`
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/opnxjao84ngvpl9e8ix6.png)

use this command `git rebase -i CommitID`, _i_ is interactive most of the time we need -i flag, give enter this will show you like this

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kegqv25fdrfrwy19cnpp.png)

you can see that _Pick_ and _s_ ,we don't need to change the first pick it remains same, now if we want to squash the commit we change it to _s_, at least the commits should have one pick ,the _s_ commits combine with the nearest _pick_ commit , it doesn't matter how many commits to be squashed , you should have one _pick_ which will be above _s_ commit . To know more you can refer [](https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase), to type in this click _i_.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/e4llsj1326fa2v5hc45t.png)
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/p10j3gwailyzkj1veqid.png)
to escape from vim editor click `ESC`, colon `:` and `x` after that you have screen like this
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/t6uvo205g0ivum8q2w72.png)

remove the _#_ which is used to comment the line then type you commit message, after that click _ESC_ , _:_ and _x_ to exit edit mode

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/h5ltmx1tyo6sfn5t46oi.png)

we finished rebasing now time to push it to github

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mpkkrpsv89dq6ko0ii9a.png)
here is the Squashed commit
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x3euda70li8m1wzq9an2.png)

and go to github now you can see the change in commit message

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/s40qxl3mqyt0d642d593.png)

- `git push` command is used to push the changes along with commit messages,
- `git fetch` command is used to fetch the recent commit messages, - `git pull` command is used to pull the code with commit messages, it internally operate _git pull_ .

---

Learning never fulfilled untill you practice on your own and share it with other people.

alright now you can add **git** skill in profile and be happy for what you have done by reading this post.
