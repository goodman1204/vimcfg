### requirements

Your PC must connect the Internet.
Installed Git & Vim.

### If ~/.vimrc and ~/.vim/ exist, then backup your original vim config

```bash
mv ~/.vimrc ~/.vimrc.old
mv ~/.vim ~/.vim.old
```

### do following steps

1. download this repo:  

 ```bash  
 git clone https://github.com/chetui/vimcfg.git
 ```

2. put files in your home:  

 ```bash  
 mv vimcfg/vimrc ~/.vimrc  
 mkdir ~/.vim
 mv vimcfg/colors ~/.vim/
 ```

3. download the plugin mamage plugin:

 ```bash
 git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
 ```

4. Install all the plugins:

 ```bash
 vim +BundleInstall +qall 
 # in this setp, it may ask you for username or password, 
 # please type the ENTER instead of type your username or 
 # password.
 ```

5. fix a bug of WinManager:

 ```bash
 vim ~/.vim/bundle/winmanager/plugin/winmanager.vim
 ```

 add **exe 'q'** in following position:  
 
 ```bash
      function! <SID>ToggleWindowsManager()
        if IsWinManagerVisible()
           call s:CloseWindowsManager()
        else
           call s:StartWindowsManager()
           exe 'q'   
        end
     endfunction
 ```

