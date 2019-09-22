## 契约

> 环境称呼约定：
> 1. `getRiches`仓库均为**线上环境**; 
> 2. Fork至自己仓库的和本地为**开发环境**;
>
> 分支区别：
> 1. `release` 为正式发布的分支
> 2. `master` 为测试发布的分支
>
> 注意: 在开发过程中,请使用不同的分支进行对功能的区分(仅限于Fork仓库)


## 代码仓库
1. 将代码Fork至自己的仓库
2. 拉去自己的代码
    ```shell script
    git clone git@github.com:FzPying/wocms.git
    ```
3. 添加远程仓库
    ```shell script
    git remote add ups git@github.com:getRiches/wocms.git
    # 其中 `ups` 是自定义的
    ```
4. 提交代码
    1. 合并线上正式环境 
        ```shell script
        # 提交任何代码时都需要执行
        git pull ups release 
        ```
    2. 推送代码至开发仓库
        ```shell script
        git push origin
        ```
    3. 在页面中创建合并请求,如果有冲突请在开发环境解决好冲突
5. 代码冲突处理
    1. 切换至`master`分支
        ```shell script
        git checkout master
        ```
    2. 合并线上正式环境 
         ```shell script
         git pull ups release
         ```
    3. 合并线上测试环境
        ```shell script
        git pull ups master
        ```
    4. 合并forks仓库开发分支
        ```shell script
        git pull origin local-dev
        ```
        > 以上3步如有冲突请解决
    5. 提交代码及推送至forks仓库   
       ```shell script
       git commit -m 'refactor(*): 处理冲突'
       git push origin master
       ```   