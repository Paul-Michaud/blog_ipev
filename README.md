# Blog IPEV

## Init submodule
```bash
git submodule update --init --recursive
git submodule update --recursive --remote
```

## Run development server
```bash
hugo server -D -v --debug --disableFastRender -w
```
## Convert images

### webp
```bash
# only one
cwebp background_principal.jpg -o background_principal.webp
# all in the current directory
for file in $(ls); do cwebp "$file" -o "${file%.*}".webp;done
```

## URL

Automatically deployed using cloudflare pages to https://pole.michaud.bzh/
