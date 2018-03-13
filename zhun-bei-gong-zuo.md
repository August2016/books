# 准备工作

## 1. 下载代码

```
git clone https://github.com/apache/rocketmq.git
cd rocketmq

# 查看发布版本（一般情况下公司的每个发布版本都会打一个tag）
git tag
```

结果如下:![](/assets/WX20180313-145441@2x.png)

```
# 切换到稳定版本4.2.0
git branch -b rocketmq-all-4.2.0
```

## 2. 使用IDE查看代码

我使用的是IDEA免费版进行代码开发的，用其它ide也可以，但是要先配置好**JDK**和**MAVEN**环境。

![](/assets/package_structure.png)

## 3. 模块依赖关系

选中rocketmq-test，按下快捷键command+option+u可以看到下图

![](/assets/module_dependencies.png)

图中展示了各个模块的依赖关系，下面的章节中会根据依赖关系，对各个模块进行讲解。







