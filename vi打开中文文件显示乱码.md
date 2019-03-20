# 问题：

    在vi编辑文件时，写中文会显示乱码。

# 解决方法：

    在~/.vim/vimrc文件中添加如下信息，如果没有~/.vim/vimrc文件则需要先创建文件再添加如下信息。
    set fileencodings=utf-8,ucs-bom,gb18030,gbk,gb2312,cp936
    set termencoding=utf-8
    set encoding=utf-8
