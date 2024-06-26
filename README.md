# Dokku Nginx Max Upload Size

> [!CAUTION]
> This is now [built into Dokku](https://dokku.com/docs/networking/proxies/nginx/#specifying-a-custom-client_max_body_size) and using this plugin breaks the Nginx configuration. To fix the error, refer to [issue #3](https://github.com/Zeilenwerk/dokku-nginx-max-upload-size/issues/3).

Nginx on Dokku throwing the 413 Error (Request Entity Too Large) error?

Install dokku-nginx-max-upload-size and suffer no more!

This is a Dokku plugin for setting the NGINX maximum upload size by setting the nginx `client_max_body_size` directive.

## Installation

```shell
# on 0.4.x+
sudo dokku plugin:install https://github.com/Zeilenwerk/dokku-nginx-max-upload-size.git
```

## Usage

```shell
# To set a max body size, set the MAX_UPLOAD_SIZE env var
# If you unset the variable, a default of 2M will be used
dokku config:set MAX_UPLOAD_SIZE=20M
```
