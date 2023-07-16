#!/bin/bash
yum update -y
yum install -y
yum install -y httpd
cd /var/www/html
wget https://github.com/Ekene205/ekywebsite/archive/refs/heads/main.zip
unzip main.zip
cp -r ekywebsite-main/* /var/www/html/
rm -rf ekywebsite-main main.zip
systemctl enable httpd
systemctl start httpd
