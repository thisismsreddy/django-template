# {{ Your Project name }}
its works with latest Djagno and python 2.7 or 3.4
## Getting Started

Make sure you are using a virtual environment of some sort (e.g. `virtualenv` or
`pyenv`).

```
pip install -r requirements.txt
./manage.py migrate
./manage.py loaddata sites
./manage.py runserver
```

      sudo nano /etc/nginx/sites-available/myprojectserver 
```
server {
    listen 80;
    server_name 38.76.11.161
    access_log off;

    location /static/ {
        alias /home/ubuntu/work/myproject/static/;
    }

    location / {
            proxy_pass http://127.0.0.1:8000;
    }
}

```

      cd /etc/nginx/sites-enabled
      sudo ln -s ../sites-available/myproject
    sudo rm default
    sudo service nginx restart
