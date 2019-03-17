# 
## Question： 用nohup执行python程序时，print无法输出

    nohup python test.py > nohup.out 2>&1 &
    发现nohup.out中显示不出来python程序中print的东西。

## Answer:

    这是因为python的输出有缓冲，导致nohup.out并不能够马上看到输出。

### 方法一：
    
    python 有个-u参数，使得python不启用缓冲。
    nohup python -u test.py > nohup.out 2>&1 &

### 方法二：
    
    export PYTHONUNBUFFERED=1
    nohup python -u test.py > nohup.out 2>&1 &
