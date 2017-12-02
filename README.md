## Shared CSS Library

Reverse proxy with nginx can be used for frontend development.
Nginx is very simple to setup for css files substitution.


### How to test

```
    # install nginx
    sudo apt-get update && sudo apt-get upgrade
    sudo apt-get install nginx

    #remove default nginx.conf
    cd /etc/nginx
    sudo rm nginx.conf

    # make symbolik link to our nginx.conf
    /etc/nginx$ sudo ln -s /path/to/cloned/repo/32_stylish_portal/nginx.conf
```

Open nginx.conf and change "/path/to/32_stylish_portal/dist/style.css" on yours. Visit urls from "listen" directives in browser and nginx will redirect requests to urls from "proxy_pass" directives and substitute appropriate regexes to  aliases.


```

    # start nginx
    sudo service nginx start

    # stop nginx
    sudo nginx -s stop

```


### Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
