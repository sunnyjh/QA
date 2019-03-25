## 问题
   
    SyntaxError: Non-ASCII character '\xe8' in file solid_sample_info.py on line 19, but no encoding declared; see http://python.org/dev/peps/pep-0263/ for details

## 解答

原因：注释里面或者代码中出现了中文，而 Python 支持的 ASCII 码无中文。
在头文件中添加如下代码：

    # -*- coding: utf-8 -*-

    # 这样也行
    # coding:utf-8 

*注意：本行要添加在源代码的第一行。*
    
