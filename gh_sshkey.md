### gitbash 基本操作  ###
1. **创建sshkey**   
`ssh-keygen -t rsa -C 'your account' -f ~/.ssh/filename`

2. **配置config**(*~/.ssh/config*)   
`Host hostname`     
`User git`      
`Hostname github.com`    
`PreferredAuthentications publickey`   
`IdentityFile ~/.ssh/filename`

3. **登陆github**   
`ssh -T hostname`
