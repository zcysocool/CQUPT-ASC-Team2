nux网络配置与GitHub团队仓库克隆，过程中遇到了两个关键问题并逐一解决：一是Linux系统中NetworkManager对ens33网卡存在`strictly unmanaged`的底层托管限制，导致`nmcli`命令操作全部失效，最终切换到传统的`network.service`管理网络，通过修正`ifcfg-ens33`配置文件并重启服务，成功实现了网络连通；二是校园网对GitHub的访问限制，HTTPS的443端口和SSH的22端口均被拦截，出现`Connection refused`报错，后通过修改`~/.ssh/config`文件指定`Port 443`和`HostName ssh.github.com`，改用443端口走SSH协议，绕开了校园网的端口拦截。

在Linux、gcc、Git三类知识点中，**gcc编译相关内容是我最不熟悉的部分**，目前仅了解`gcc -o`的基础编译命令，对编译的预处理、编译、汇编、链接等阶段的原理和参数配置完全没有概念，也不知道如何通过gcc排查程序编译时的报错信息。

目前我最困惑的点是：SSH配置的权限规则逻辑，比如`.ssh/config`文件必须设置600权限、`.ssh`目录需设700权限的底层原因，以及当权限配置错误触发`Bad owner or permissions`报错时，如何快速定位并修复权限问题，避免反复试错。

