#Docker入门
##什么是Docker？
Docker是一个软件**容器**的平台。开发者使用它来解决“代码在自己机器上可以完美运行，在其他环境上出现错误”的问题；运维人员可以使用Docker在一种隔离的状态下并行的运行apps；企业可以使用它来完成更敏捷的软件开发，更快的软件迭代，在Linux和windows上运行的更高的可靠性。

####那什么是容器呢？
 一个容器是一种轻量级的，可以独立运行的，并且包含所有可以执行的工具包，代码，系统环境，配置文件及所需软件的可运行包。其实就是一种包含软件所用运行集合工具的一个环境。容器支持基于linux和windows的app，一旦创建了一个容器，那么它就不再与外部的环境有关系，这就解决了多人开发时相同代码在不同的环境中运行结果不一致的问题。
 
> 个人理解：一个容器就是对一整套环境的一种封装，和VM有点类似，只是容器是对软件资源的划分隔离，而VM是对硬件资源的划分。所以这也就是Docker官方所说的轻量级，更高效的原因。

##Docker的相关术语
| Name| Description|
| ------------- |:-------------:|
| Docker 镜像(Images)      | Docker 镜像是用于创建 Docker 容器的模板，远程仓库中存放的就是镜像。 |
| Docker 容器(Container)      | 容器是独立运行的一个或一组应用，一个镜像可以产生多个容器。|
| Docker 客户端(Client) | Docker 客户端（terminal窗口）通过命令行或者其他工具使用 Docker API (https://docs.docker.com/reference/api/docker_remote_api) 与 Docker 的守护进程通信。 |
| Docker 主机(Host) | 一个物理或者虚拟的机器用于执行 Docker 守护进程和容器，安装docker后会有一个terminal和一个host。|
|Docker 仓库(Registry) |Docker 仓库用来保存镜像，可以理解为代码控制中的代码仓库。Docker Hub(https://hub.docker.com) 提供了庞大的镜像集合供使用。|
|Docker Machine|Docker Machine是一个简化Docker安装的命令行工具，通过一个简单的命令行即可在相应的平台上安装Docker，比如VirtualBox、 Digital Ocean、Microsoft Azure。|

##Docker基本原理？
![](http://www.runoob.com/wp-content/uploads/2016/04/576507-docker1.png)

private registry : 私有的仓库，可以自己搭建。
remote host : 应该是可以把docker安装到远程的服务器上，然后通过ssh或者其他方式进行连接操作（待确认）

##Docker能做什么？
一. 可以帮助开发者跳过配置繁琐环境的步骤。
二. 可以解决同一个app在不同的开发者电脑上运行结果不一致的问题。

目前只能理解这两个用处（肯定不止这两个，待学习） 

##Docker有什么好处？
1、简化流程：
一个容器相当于提供了一个标准的配置环境，一旦配置好，可以重复使用，简化配置的流程。
2、运行一些软件更方便：
需要很多配置才能使用的软件，有了docker后只需要运行配置好的容器就可以完美的运行。