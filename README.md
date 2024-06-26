find . -type l -name "*.gz" -exec readlink -f {} \; | xargs -I{} gzip -d -- {}
find . ! -type l -type f -name "*.gz" -exec gzip -d -- {} +
