1.git bash中中文文件名乱码解决方案：
    右击git bash 选择options...
    菜单中选择Text->Local,选择zh_CN,utf-8,点击apply,save
    执行命令：git config --global core.quotepath false
    (就不会对0×80以上的字符进行quote，中文显示正常。)

2.git log显示提交的中文log乱码解决方案：
    git config --global gui.encoding utf-8

3.git查看帮助的方法：
    (1) git help opt (opt为某个操作)
    (2) git opt --help (opt为某个操作)
    (3) man git opt (opt为某个操作)