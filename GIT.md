####Can I specify multiple users for myself in .gitconfig?
- https://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig
####The “fatal: refusing to merge unrelated histories” Git error
- https://www.educative.io/edpresso/the-fatal-refusing-to-merge-unrelated-histories-git-error
####Adding a new SSH key to your GitHub account
- https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account
####Can I specify multiple users for myself in .gitconfig?
- https://stackoverflow.com/questions/4220416/can-i-specify-multiple-users-for-myself-in-gitconfig

- git pull origin master --allow-unrelated-histories
- git remote add origin git@github.com:Personal-Practise-Projects/00-starter.git

####Setup multi github account
#####Local
- `git config user.name "Your Name Here"`
- `git config user.email your@email.com`

#####Global
- `git config --global user.name "Your Name Here"`
- `git config --global user.email your@email.com`

You might want to start checking your currently saved keys
- `ssh-add -l`

If you decide to delete all cached keys before (optional, careful about this)
- `ssh-add -D`
- `cd ~/.ssh`
- `ssh-keygen -t rsa -C "work@company.com"` <-- save it as "id_rsa_work"
- `ssh-keygen -t rsa -C "pers@email.com"` <-- save it as "id_rsa_pers"

After performing this commands you will have the following files created
```
~/.ssh/id_rsa_work      
~/.ssh/id_rsa_work.pub

~/.ssh/id_rsa_pers
~/.ssh/id_rsa_pers.pub
```

Make sure authentication agent is running
- `eval ssh-agent -s`

Add the generated keys as following (from the ~/.ssh folder)
- `ssh-add id_rsa_work`
- `ssh-add id_rsa_pers`
- `ssh-add ~/.ssh/id_rsa_pers`



