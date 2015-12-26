---
layout: post
title: Akı(l)cı Ölçekleme (Seam Carving veya Liquid Resampling)
---

Akı(l)cı Ölçekleme (seam carving veya liquid resampling), Shai Avidan ve Ariel Shamir tarafından 2007 yılında geliştirilmiş, resim içeriğini dikkate alarak ölçekleme yapar. Resim içeriğini dikkate almaksızın ölçekleme çeşitli sorunları doğurur. Örneğin,

![](http://19ceng.github.io/assets/posts/afis_800x363.png)

resmini (`800x363`) klasik yolla (sol) ve akı(l)cı (sağ) ölçekleyecek olsak (`400x363`),

![C](http://19ceng.github.io/assets/posts/afis_400x363_classic.png)
![SC](http://19ceng.github.io/assets/posts/afis_400x363.png)

ve yine klasik yolla (sol) ve akı(l)cı (sağ) ölçekleyecek olsak (`800x200`)

![C](http://19ceng.github.io/assets/posts/afis_800x200_classic.png)
![SC](http://19ceng.github.io/assets/posts/afis_800x200.png)

şeklinde bozulmuş görüntüler alırdık.

# Yöntem

ImageMagick v6 ile akı(l)cı ölçekleme,

```bash
$ convert afis_800x363.png  -liquid-rescale 400x363\!  afis_400x363.png
$ convert afis_800x363.png  -liquid-rescale 800x200\!  afis_800x200.png
```

# Kaynaklar

1. http://www.faculty.idc.ac.il/ARIK/site/seam-carve.asp
2. http://www.mathworks.com/matlabcentral/fileexchange/18089-seam-carving-for-content-aware-image-resizing--gui-implementation-demo
2. https://en.wikipedia.org/wiki/Seam_carving
2. http://www.imagemagick.org/Usage/resize/
3. https://www.youtube.com/watch?v=vIFCV2spKtg
