文件结构
```
├─ hosts # 主机清单配置
├─ roles # ansible 脚本角色目录
├─ init-base.yml # 安装服务器基础软件包
└─ init-roles.yml # 初始化服务器，调用 roles 资源进行服务器初始化配置
```





```
# ping
ansible all -m ping -i hosts

```


# 初始化系统需要做的事情
1. 初始化系统
1.1 更新系统
1.2 安装基础软件包
1.3 对服务器进行初始化配置，如安装时间同步服务，安装docker等
ansible-playbook -i hosts init.yml -e 'hosts=all'
ansible-playbook -i hosts init-roles.yml -e 'hosts=all'



