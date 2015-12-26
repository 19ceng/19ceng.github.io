---
layout: post
title: Akı(l)cı Ölçekleme (Seam Carving veya Liquid Resampling)
---

Akı(l)cı Ölçekleme (seam carving veya liquid resampling), Shai Avidan ve Ariel Shamir tarafından 2007 yılında geliştirilmiş, resim içeriğini dikkate alarak ölçekleme yapar. Resim içeriğini dikkate almaksızın ölçekleme çeşitli sorunları doğurur. Örneğin,

![](http://19ceng.github.io/assets/posts/afis_800x363.png)

resmini (`800x363`) klasik yolla ölçekleyecek olsak (`400x363`),

![](http://19ceng.github.io/assets/posts/afis_400x363_classic.png)

veya (`800x200`)

![](http://19ceng.github.io/assets/posts/afis_800x200_classic.png)

şeklinde bozulmuş görüntüler alırdık. Akı(l)cı ölçekleme ile yapılacak olsa ilk resim (`400x363`),

![](http://19ceng.github.io/assets/posts/afis_400x363.png)

ve sonraki (`800x200`)

![](http://19ceng.github.io/assets/posts/afis_800x200.png)

olacak.

# Yöntem

# Kaynaklar
