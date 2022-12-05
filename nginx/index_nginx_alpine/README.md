# 创建一个索引目录的nginx镜像
docker build -t index_nginx:v1 .
docker run -d -p 80:80 --name nginx -v ${PWD}/data:/data index_nginx:v1
