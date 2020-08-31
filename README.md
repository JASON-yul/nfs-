# nfs实现多台机器共用一个路径
参考文档地址:https://www.cnblogs.com/scaven-01/p/11461908.html

1.注：公司内部网络可能会存在现象如下;
如果显示mount.nfs: access denied by server while mounting 
可以将服务端的/etc/exports里的ip改为*试试：如/data/  *(rw,sync,root_squash)，或是获取准确的ip网段
2.chowm -R nfsnobody:  /data 
需要将目录下所有文件全部修改，便于客户端能够对所有文件具有执行权限
