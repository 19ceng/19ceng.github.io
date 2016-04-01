---
layout: post
title: Görsel Arama
---

Pinterest 2010 yılında kurulmuş, 70 milyondan fazla kullanıcısı olan her türlü görselin paylaşıldığı ve pano sistemiyle çalışan bir sosyal platformdur. Bu yazının konusu ise pinterest ile birlikte endüstriyel ün kazanan görsel arama üzerine olacak. Bu özellik sayesinde "benzer paylaşımlar" ve "benzer görünüşler" için öneri/aram imkanı sunulabilmektedir.

Benzer bir yaklaşımın <http://www.dressbit.com/> sitesinde de yapıldığı görülebilir,

> 8bit olarak Deep Learning teknikleri ile demo amaciyla gelistirdigimiz moda platformu www.dressbit.com . Amacimiz begendiginiz urunlere gorsel olarak benzeyen urunleri kullaniciya sunmak. Urunun amaci biraz out of scope bizler icin ama yinede paylasmak istedim :)﻿
> **Sitenin sloganı**: Click to find similar fashion. Shuffle to discover.

Ayrıca Cloudinary'de bunun benzeri işlere başlamış (ilkel düzeyde de olsa), [How-to automatically identify similar images using pHash](http://cloudinary.com/blog/how_to_automatically_identify_similar_images_using_phash)

# Yöntem

**[jing2015]** vd. yaptıkları çalışmada derinlemesine konvolüsyon ağlarının (CNNs) ara katmanlarından resimlerin yerel öznitelikleri ve "derin öznitelikleri" çıkarmışlardır. Kullandıkları CNNs, AlexNet ve VGG mimarileri temelinde seçmişlerdir. Özniteliklerinin temsil etkinliğini arttırmak için ikilleştirmişler ve Hamming mesafesi kullanarak karşılaştırmıştırlarr. Açık kaynak kod Caffe kullanarak eğitim ve çıkarım sağlamışlardır.

# Örnek

Çanta arama sonuçları,

![](http://i.imgur.com/NnoSJ19.png)

Ya da ayakkabı arama sonuçları,

![](http://i.imgur.com/lRbN1oa.png)

# Kaynakça

1. **[jing2015]** Yushi Jing, David Liu, Dmitry Kislyuk, Andrew Zhai, Jiajing Xu, Jeff Donahue, "Visual Search at Pinterest", ACM,  http://dx.doi.org/10.1145/2783258.2788621, http://arxiv.org/pdf/1505.07647v2.pdf
