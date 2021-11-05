git submodule update --init --recursive

git submodule update --recursive --remote

 hugo server -D -v --debug --disableFastRender -w

# Convert images

avif (not supported by edge)
avifenc background_principal.jpg background_principal.avif --min 0 --max 63 -a end-usage=q -a cq-level=32 -a tune=ssim -a deltaq-mode=3 -a sharpness=3 -y 420

webp
cwebp background_principal.jpg -o background_principal.webp
for file in $(ls); do cwebp "$file" -o "${file%.*}".webp;done
