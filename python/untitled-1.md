# Resizing an image to smaller size

Resizing images to smaller dimension to satisfy the file size or height/width requirements is something we have faced multiple times. Most of the online tools which I previously used were full of advertisments, and even required to login which is something I hated a lot. Today I learned to do this tedious job with python and it's pretty easy also.

Library used: Pillow

```
import os, sys
from PIL import Image

size = (720, 720)

for infile in sys.argv[1:]:
    outfile = os.path.splitext(infile)[0] + f"{size[0]}.jpg"
    if infile != outfile:
        try:
            with Image.open(infile) as im:
                im.thumbnail(size)
                im.save(outfile, "JPEG")
        except OSError:
            print("cannot create thumbnail for", infile)
```

Save file as `resize.py` and run the script with:

> python3 resize.py image.jpg

Thanks to [Jishnu](https://twitter.com/jishnu7) and [Rajeesh](https://twitter.com/rajeeshknambiar), I learned there is another tool called ImageMagick. It can also resize images, along with a ton more other cool stuff.

Try image magic, I think it is built into most distros (if not, easy to install via system package manager) and supports more than 200 formats. Easy to use as well.— Jishnu (@jishnu7) [July 20, 2021](https://twitter.com/jishnu7/status/1417363498120605696?ref\_src=twsrc%5Etfw)

**To Install ImageMagick in your debian based distro:**

```
sudo apt install imagemagick
```

To resize images with height, width use the option:

```
convert -resize 300x720 image.jpg resized_image.jpg
```

You can resize also based on the quality as follows:

```
convert -quality 50 image.jpg resized_image.jpg
```
