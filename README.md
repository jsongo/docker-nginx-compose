##centos7初始化##

curl -sSL http://get.docker.com/ | sh  
docker pull daocloud.io/nginx  
sudo docker run -it --rm -v /data:/data daocloud.io/nginx bash  
然后在里面把/etc/nginx拷到/data里。  
yum install python-pip  
pip install docker-compose  
然后把这个文件下载下来：https://raw.githubusercontent.com/jsongo/docker-nginx-compose/master/docker-compose.yml  
  
sudo docker-compose up -d  
报错的话，就直接运行：  
sudo docker run --net=host --name nginx -v /data:/data -v /etc/nginx:/etc/nginx -v /var/log/nginx:/var/log/nginx -d daocloud.io/nginx  
