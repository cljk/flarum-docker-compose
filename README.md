# Flarum Forums made simple.

> Flarum is the next-generation forum software that makes online discussion fun. It's simple, fast, and free.
> http://flarum.org/

To start a fresh flarum setup just checkout the repo and startup 
with 
```
git clone https://github.com/cljk/flarum-docker-compose
cd flarum-docker-compose
docker-compose build
docker-compose up
```
# Persistent storage
In `docker-compose.yml` all data (from database and www/flarum files) are mapped
in the folders under `/data`.

On first startup composer is called to install flarum in 
`/var/www/html` which maps to `/data/www_html`
(compare `/http/docker/hooks/entrypoint-pre.d/02_installFlarum`)

This takes some time... after that you can call installation procedure of flarum.
Enter following data for db link:

* Mysql host: db
* Mysql database: flarum
* Mysql Username: flarum
* Mysql Password: flarum
* Table Prefix: 



# Flarum
HTTP exposed at 8180
  * [http://127.0.0.1:8080](http://127.0.0.1:8080)

# Phpmyadmin 
 running on 8181
  * [http://127.0.0.1:8081](http://127.0.0.1:8081)

# Mailhog at 8025
  * [http://127.0.0.1:8025](http://127.0.0.1:8025)

# Mysql 
at 3306

