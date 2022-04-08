# Docker <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">
All Abound Docker

#### LIST
- [Help 👻](#introduction-)
- [Mysql 👻](#mysql-)
- [Log 👻](#log-)
- [Alias 👻](#alias-)
- [Delete 👻](#delete-)
- [Show 👻](#show-)
- [Referance 👻](#referance-)

#### INTRODUCTION 👻

    docker images   // check images installed
    docker ps   // check run container
    docker ps -a    //check hostory run container stoped
    
    docker stop [container image/ container name]   // stop run container
    
    docker container prune  // remove old container
    docker system prune // remove all stoped container
    
    -d  // run in background

#### MYSQL 👻

    sudo docker run --name=[name container] -p [local port]:[docker port] [option] [image]
    sudo docker run --name=MySql -p 33061:3306 -e MYSQL_ROOT_PASSWORD=1  mysql
    
    sudo docker exec -it MySql2 mysql -uroot -p // enter in mysql

And you mush commit first:
    
    // you cant use -m or -am, but if file updated code you should used -am
    // recomended use -am
    git commit -am "commit first" 

And than you remote git URL:

    git remote add origin <URL>

Case beacause you already remote branch:
    
    fatal: remote origin already exists.
    
You should set remote, follow this tag:

    git remote set-url origin <URL>

If you want make branch auto checkout:

    git branch -M <BRANCH NAME>

Check repository branch active:
    
    git branch

Push in GIT:

    git push -u origin <BRANCH NAME>

#### MERGE 👻
### OPTION 1 MERGE
If you want merege 2 branch and allowed incoming files in DEV into TRIAL <br>
<br>
Checkout Branch MASTER OR TRIAL OR STAGGING OR CENTER:

    checkout <BRANCH MASTER NAME EXAMPLE: trial>

And MERGE branch destination:

    git merge -X theris <BRANCH ANOTHER NAME EXAMPLE: dev>

If this case 
    
    merge: dev - not something we can merge

solve: you don't have branch dev.
if you want all branch or you want spesific branch:

    git fetch origin <BRANCH NAME EXAMPLE: dev>

The error is resolved by toggling the "allow-unrelated-histories" switch. After a git pull or git merge command, add the following tag:

    fatal: refusing to merge unrelated histories

Use anything with --allow-unrelated-histories:

    git pull origin <BRANCH NAME> --allow-unrelated-histories
    OR
    git push -u origin <BRANCH NAME> --allow-unrelated-histories
    OR
    git merge -X theirs <BRANCH ANOTHER NAME EXAMPLE: dev> --allow-unrelated-histories
    
Remember USED THIS:

    < --allow-unrelated-histories >
    
Check branch MERGED:
    
    git branch --merged

![image](https://user-images.githubusercontent.com/77251566/139561661-2b62076c-b9cd-4f84-a977-b64c5cfba81a.png)

### OPTION 2 MERGE
This clone all branch:
    
    git clone <URL>

Check all branch:
    
    git branch -a or git branch -r

Checkout branch first what you need, for update branch:
    
    git checkout <branch name>

Merge:
    
    <example position remote in branch master>
    git merge <target branch name>

And if the conflict and you see it's not too much trouble with the conflict you can reset it first and merge the dominant auto update in the incoming branch/them.
This sample conflict and not too much trouble:
![image](https://user-images.githubusercontent.com/77251566/147038638-7de51fa3-b4b1-4f04-8141-73d24a62dd21.png)

Reset MERGE:
    
    git reset --merge
    
Merge strategy theirs:
    
    git merge --strategy-option theirs

#### LOG 👻
How to check log commit:

    git log
    OR
    git log --all --decorate --oneline --graph

#### ALIAS 👻
Making alias:
    
    alias graph ="git log --all --decorate --online --graph"

#### DELETE 👻
Delete local branch:
    
    git branch -d <BRANCH NAME>
    OR
    git branch -D <BRANCH NAME>
    
#### SHOW 👻
Show existing remote url:
    
    git remote show origin
    OR
    git remote -v

#### REFERANCE 👻
[Documentation](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories) <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">
