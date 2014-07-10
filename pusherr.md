###push
**config**
>Host github4silenjs
 User git   
 Hostname github.com  
 PreferredAuthentications publickey   
 IdentityFile ~/.ssh/github4silenjs

**remote**
>$ git remote -v   
 origin  git@github.com:silenjs/ghnote.git (fetch)   
 origin  git@github.com:silenjs/ghnote.git (push)   

**push err**  
>$ git push origin master   
 Permission denied (publickey).   
 fatal: Could not read from remote repository.   
 Please make sure you have the correct access rights and the repository exists.

**remote add**   
>$ git remote add github4silenjs git@github4silenjs:silenjs/ghonte.git

**remote**   
>$ git remote -v   
 origin  git@github.com:silenjs/ghnote.git (fetch)   
 origin  git@github.com:silenjs/ghnote.git (push)   
 github4silenjs    git@github4silenjs:silenjs/ghnote.git (fetch)   
 github4silenjs    git@github4silenjs:silenjs/ghnote.git (push)

**push done**  
>$ git push github4silenjs master

