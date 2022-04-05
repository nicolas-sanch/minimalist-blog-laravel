# Minimalist blog using Laravel

```bash
git clone https://github.com/nicolas-sanch/minimalist-blog-laravel

cd minimalist-blog-laravel
cp .env.example .env

docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer install
  
sudo chmod 666 /var/run/docker.sock

vendor/bin/sail up -d
vendor/bin/sail artisan key:generate               
vendor/bin/sail artisan migrate  
```
