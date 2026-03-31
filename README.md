# prometheus-graphana installatiom

#graphana installation
$sudo su
$wget https://dl.grafana.com/enterprise/release/grafana-enterprise-11.1.4.linux-amd64.tar.gz
$ls
$tar -zxvf grafana-enterprise-11.1.4.linux-amd64.tar.gz
$ls
$cd Grafana-11.1.4
$./bin/Grafana-server

#docker setup
$sudo su
$apt-get update -y
$apt install docker.io -y
$service docker start
$docker run -it –name c01 ubuntu
$docker run -it –name c02 ubuntu

#prometheus intallation
$wget https://github.com/prometheus/prometheus/releases/download/v2.53.2/prometheus-2.53.2.linux-amd64.tar.gz
$tar -zxvf prometheus-2.53.2

#in docker
$vi /etc/docker/daemon.json
$service docker restart

#in prometheus
$vi prometheus.yaml
$./prometheus
