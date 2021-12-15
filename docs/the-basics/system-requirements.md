---
id: system-requirements
title: System Requirements
---

# 💻 System Requirements

:::danger
If you are using services such as a VPS or a dedicated server, or if you are hosting a webserver yourself, you are expected to know how these types of services work. No support will be given with setting these up.
:::

## Requirements

* [ ] Apache 2 or Nginx webserver (Configuration **NOT** included)
* [ ] Reliable webhost (We Recommend [**Hexane Networks**](https://billing.hexanenetworks.com/aff.php?aff=358))
* [ ] PHP >= 7.4 (PHP 8.0 recommended)
* [ ] MySQL >= 5.8 or MariaDB >= 10.2
* [ ] JSON, BCMath, OpenSSL, MBString, Tokenizer, XML PHP, CType & GMP (PHP Extensions)
* [ ] `allow_url_fopen` module _enabled_

## Our Recommended Hosting Provider

![Hexane Networks (Use Code COSMO for 25% off at checkout)](../../static/img/hexane-promo.png)

## Nginx Basic Configuration

_If you are not self-hosting cosmo you can skip this part._

```nginx
server {
        listen 80;
        listen [::]:80;

        server_name <your_domain> www.<your_domain>;
        return 301 https://$server_name$request_uri;
}

server {
        listen 443 ssl http2;
        listen [::]:443 ssl http2;

        include snippets/ssl-example.com.conf;
        include snippets/ssl-params.conf;

        root /var/www/cosmo/public;

        index index.php index.html index.htm index.nginx-debian.html;

        server_name <your_domain> www.<your_domain>;

        location / {
                try_files $uri $uri/ /index.php?$query_string;
        }

        location ~ \.php$ {
                include snippets/fastcgi-php.conf;
                fastcgi_pass unix:/run/php/php7.4-fpm.sock;
        }

        location ~ /\.ht {
                deny all;
        }

        location ~ /.well-known {
                allow all;
        }
}
```

