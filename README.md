# docker-lssea


进入目录以后

git clone https://git.coding.net/YLY_TTTT/lssea.git 把代码拉下来

执行docker-compose up构建环境

等环境构建成功

docker ps 找到mysql那一行 第一列是CONTAINER ID

docker exec -i ${CONTAINER ID} mysql -uroot --password=cancel lssea < mysql_lssea_database.sql 

导入mysql数据库

访问http://localhost  打不开的话试试docker-machine ip 返回的ip

正常会提示mysql连接错误 

> 需要修改代码里面的db_hostname为mysql

> 另外将代码中的http://www.lssea.com 修改为localhost或者docker-machine ip 

> 准备代码中添加测试模型配置 避免修改

已添加测试模型 修改config.php admin/config.php system/config/default.php 里test字段即可
