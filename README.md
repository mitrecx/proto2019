克隆含有子模块的项目:   
```shell script
git clone git@github.com:mitrecx/mitre2019.git

git submodule init

git submodule update --init --recursive
```

或者直接:   
```shell script
git clone --recursive https://github.com/chaconinc/MainProject
```

如果想要在子模块中查看新工作,  
可以进入到目录中运行 <code>git fetch</code> 与 <code>git merge</code>,  
合并上游分支来更新本地代码:  
```shell script
cd src/main/proto
git fetch
git merge origin/master
```
或者, **让 Git 自动进入子模块然后抓取并更新** :
```shell script
git submodule update --remote src/main/proto
```

执行 <code>git pull</code> 拉取代码后, 如果子模块(别人)有提交, 应该更新子模块:
```shell script
git submodule update
```

其它:  
为一个新的仓库添加子模块:  
```shell script
git submodule add <url> <path>

# git submodule add https://github.com/mitrecx/proto2019.git ./src/main/proto 
```
