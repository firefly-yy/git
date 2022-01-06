# git 基本操作
### 场景1:
  - 主分支有修改 
  - 当前分支有修改 

1. 在当前分支上进行 git stash  将修改先隐藏
2. git checkout main  回到主分支
3. git pull  拉取主分支上最新代码
4. git checkout <your branch name>  回到自己的分支
5. git merge main 将主分支的代码merge到自己的分支
6. git stash pop  释放之前修改的内容
7. 手动解决冲突 (删代码....)
8. git add .
9. git commit ...
10. git push
  
  
### 场景2:
 - 主分支没修改
 - 当前分支有修改
 - 需要将当前分支的代码合并至主分支
1. git chekcout main && git pull (以防万一，每次都提前拉一下主分支上的最新代码)
2. git merge <your branch name> 将分支合并至主分支
3. git push 将主分支的代码上传并合并
  
### 场景3
 - git pull git push 超时
1. ping github.com 确认连接超时
2. git config --global http.proxy 127.0.0.1:<your proxy port> 配置代理
3. git config --global -l  查看git的所有配置
