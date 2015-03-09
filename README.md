# svn-info
svn简明操作指南，reveal.js
具体其他详细说明，[请点击](http://www.sundexin.com
)：http://www.sundexin.com



#####检出主干

````
svn co svn://localhost/demo/trunk ~/ppt/demo
````

#####查看主干信息

````
svn info
````
#####创建分支

````
svn cp svn://localhost/demo/trunk svn://localhost/demo/branches/branch_demo -m "创建分支"
````
#####检出分支

````
svn co svn://localhost/demo/branches/branch_demo ~/ppt/branch
````

#####查看分支信息

````
svn info
````

#####修改主干与分支的文件 造成冲突

````
svn up 
````

````
svn ci -m "message"
````

#####在主干上合并分支

````
svn merge -r 14:16 svn://localhost/demo/branches/branch_demo
````

#####解决冲突

````
svn resolve index.php --accept mine-conflict
````

````
svn resolve index.php --accept theirs-conflict
````


#####标记冲突已解决

````
svn resolved index.php
````

#####提交主干

````
svn ci -m "message"
````
