---
layout: post
title: Akı(l)cı Ölçekleme (Seam Carving veya Liquid Resampling)
---

Akı(l)cı Ölçekleme (seam carving veya liquid resampling), Shai Avidan ve Ariel
Shamir tarafından 2007 yılında geliştirilmiş, resim içeriğini dikkate alarak
ölçekleme yapar. Resim içeriğini dikkate almaksızın ölçekleme çeşitli sorunları
doğurur. Örneğin, aşağıdaki resim olsun,

![](http://19ceng.github.io/assets/posts/afis_800x363.png)

1) resmin (`400x363`) boyutunun crop (sol), resize (orta) ve akı(l)cı (sağ)
ölçekleme sonucu,

![C](http://19ceng.github.io/assets/posts/afis_400x363_crop.png)
![R](http://19ceng.github.io/assets/posts/afis_400x363_resize.png)
![SC](http://19ceng.github.io/assets/posts/afis_400x363.png)

2) resmin (`800x200`) boyutunun crop (sol), resize (orta) ve akı(l)cı (sağ)
   ölçekleme sonucu,

![C](http://19ceng.github.io/assets/posts/afis_800x200_crop.png)
![R](http://19ceng.github.io/assets/posts/afis_800x200_resize.png)
![SC](http://19ceng.github.io/assets/posts/afis_800x200.png)

elde edilir.

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
