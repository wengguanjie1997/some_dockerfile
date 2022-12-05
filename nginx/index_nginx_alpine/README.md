<h1>创建一个索引目录的nginx镜像</h1>

# 制作镜像
docker build -t index_nginx:v1 .

# 运行容器
docker run -d -p 80:80 --name nginx -v ${PWD}/data:/data index_nginx:v1
