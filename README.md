1. 安装PostgreSQL
helm install postgresql ./postgresql -n default
2. 查看 pod状态
kubectl get pod -n default
3. 进入pod
kubectl exec -it podname -n default -- /bin/bash
4. 链接数据库
psql -h IP地址 -U 用户 -d 数据库name
:键入密码 ### 相关用户密码在values.yaml文件中
5. 查看相关表
\d test 
6. 查看数据
SELECT * FROM test;
7. 卸载
helm uninstall postgresql
