
# labweb-backend

## Introduction
This is an API collection that gets publication data from https://dblp.org/.


<!--- If we have only one group/collection, then no need for the "ungrouped" heading -->
1. [getPublicationByCategoryAndYear](#1-getpublicationbycategoryandyear)
1. [getPublicationByYear](#2-getpublicationbyyear)
1. [getPublicationByCategory](#3-getpublicationbycategory)
1. [getYearPublication](#4-getyearpublication)
1. [getCategoryPublication](#5-getcategorypublication)
1. [getAllPublication](#6-getallpublication)

## Install


```bash
apt install python3-pip
apt-get install net-tools
pip3 install flask
pip3 install flask_cors
```

## Create Service

Create service file

```bash
nano /etc/systemd/system/lab-backend.service
```
Add to file

```bash
[Unit]
Description=Lab Backend
After=network.target

[Service]
User=root
Group=root
WorkingDirectory=/root/labweb-backend
ExecStart=/usr/bin/python3 /root/labweb-backend/restapi-dplp.py
Restart=always

[Install]
WantedBy=multi-user.target

```

Start Service

```bash
systemctl daemon-reload
systemctl start lab-backend.service
systemctl status lab-backend.service
systemctl enable lab-backend.service
```

## Endpoints


--------



### 1. getPublicationByCategoryAndYear



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://192.168.107.133:5000/api/getPublicationByCategoryAndYear
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| author_name | Elena Ferrari |  |
| category_name | Conference and Workshop Papers |  |
| year | 2023 |  |



### 2. getPublicationByYear



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://192.168.107.133:5000/api/getPublicationByYear
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| author_name | Elena Ferrari |  |
| year | 2023 |  |



### 3. getPublicationByCategory



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://192.168.107.133:5000/api/getPublicationByCategory
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| author_name | Elena Ferrari |  |
| category_name | Journal Articles |  |



### 4. getYearPublication



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://192.168.107.133:5000/api/getYearPublication
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| author_name | Elena Ferrari |  |



### 5. getCategoryPublication



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://192.168.107.133:5000/api/getCategoryPublication
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| author_name | Elena Ferrari |  |



### 6. getAllPublication



***Endpoint:***

```bash
Method: GET
Type: 
URL: http://192.168.107.133:5000/api/getAllPublication
```



***Query params:***

| Key | Value | Description |
| --- | ------|-------------|
| author_name | Elena Ferrari |  |



---
[Back to top](#labweb-backend)

>Generated at 2023-08-31 07:58:06 by [docgen](https://github.com/thedevsaddam/docgen)
