### gitbash 基本操作  ###
- **创建sshkey**   
>`ssh-keygen -t rsa -C 'your account' -f ~/.ssh/filename`

-  **配置config**(*~/.ssh/config*)   
>`Host hostname`     
 `User git`      
 `Hostname github.com`    
 `PreferredAuthentications publickey`   
 `IdentityFile ~/.ssh/filename`

- **登陆github**   
>`ssh -T hostname`

- **本地初始化文件hub**   
>`git init`   
 *若需要本地的hub能与github上的hub同步，你需要在github上创建一个repository,然后把本地hub push到github上*

- **在github创建repository**   
>*创建成功之后，你会得到这个repository的[地址协议](# "本人随便起的")如：
 [`https://github.com/silenjs/test.git`](# "HTTP协议")   
 [`git@github.com:silenjs/test.git`](# "SSH协议")

- **本地hub关联远程hub**   
>通过remote把远程hub添加到本地的远程hub,这里可以通过HTTP协议或者SSH协议进行关联，两者的区别暂时木有了解
 `git remote add origin git@github.com:silenjs/test.git`

- **本地hub推送到远程hub进行同步**   
> 推送的前提条件是你的[SSK Key 公钥](# "详见上文关于sshkey一节")在你账户列表中
 前提条件满足了，我们就可以通过push把commit在暂存区的本地hub文件同步到远程hub上去
 [`git push origin master`](# "把本地hub推送到origin指定的远程hub上的master分支")*这里的origin要特别注意，hostName的地方要填写你config里面的hostName，并且确保改host的sshkey在你的用户列表里面*

