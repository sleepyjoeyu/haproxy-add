# haproxy-add

# 3 variables

newapp:  [ ap server name or IP ]
appname: [ app backend name ]
appport: [ app service port ]


# demo systems

Load Balancer: haproxy.example.com
App backend server1: app1.example.com
App backend server2:app2.example.com

# Play
1. Install httpd

ansible-playbook install-httpd.yml

2. add haproxy

ansible-playbook haproxy-add.yml -e "newapp=app2.example.com"


# check result

http://haproxy.example.com
http://haproxy.example.com/haproxy_stats




