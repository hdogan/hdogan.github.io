---
layout: post
title: "Hoşgeldin PHP 5.4: Ne getirdin, ne götürdün?"
---

<p class="message">
    <em>Bu yazı eski blogdan arşiv amaçlı alınmış olduğu için içerikte tutarsızlıklar olabilir.</em>
</p>

Bilindiği üzere umutla beklenen PHP 6 sürümü bir süreliğine iptal edilmişti ve tamamen Unicode desteği askıya alındı, PHP geliştirme ekibi 5.4 sürümü için çalışmaya başlamıştı ve daha kararlı sürümü çıkmadan getireceği yeniliklerden bolca bahsedildi. Bügün yayınlanan PHP 5.4 sürümünün bize bazı güzel getirileri ve olması gereken götürüleri var. Performans olarak daha da iyi duruma getirilen ve yüzlerce hatanın ayıklandığı PHP 5.4 sürümü içinde gelen ve bana göre önemli olan bazı özelliklerden kısaca bahsedeceğim.
<!--more-->
### Yeni Özellikler

* **Trait yapısı** - `Özellik` olarak çağırabileceğimiz bu yenilik sınıflara büyük bir esneklik getiriyor. PHP’de sınıflar birden fazla kalıtım alamadığı için bu özellik bize sınıflarda buna yakın bir özelliği vermemizi sağlıyor. `Trait`leri kendi başlarına bir sınıf gibi düşünebiliriz fakat bu sınıftan yeni nesneler oluşturamıyoruz, tanımladığımız sınıflara `trait`ler ile yeni özellikler, metodlar ekleyebiliyoruz. Bir sınıfta dilediğimiz kadar `trait` kullanabiliyoruz ve bir `trait`i de dilediğimiz kadar sınıfta kullanabiliyoruz. Bu yenilikle bazı PHP çatı/framework projelerinin de ileride değişime uğrayacağını düşünüyorum. Aşağıda basit bir `trait` kullanım örneğini görebilirsiniz. Detaylı bilgiyi de [http://php.net/manual/language.oop5.traits.php](http://php.net/manual/language.oop5.traits.php){:target="_blank"} adresinden bulabilirsiniz.

{% highlight php %}
<?php
trait birinciOzellik {
    public function Merhaba() {
        echo "Merhaba!";
    }
}

trait ikinciOzellik {
    public function Selam() {
        echo "Selam!";
    }
}

class OrnekSinif {
    use birinciOzellik, ikinciOzellik;
}

$ornek = new OrnekSinif;
$ornek->Merhaba();
$ornek->Selam();
?>
{% endhighlight %}

* **Kısa dizi operatörü/kısa dizi tanımlama** - Dizileri Python dilindeki ya da JSON yapısındaki gibi tanımlayabiliyoruz. Aşağıdaki örnekte bunu görebilirsiniz:

{% highlight php %}
<?php
$dizi = array(1, 2, 3);

/* PHP 5.4 ile gelen özellik */
$dizi = [1, 2, 3];
?>
{% endhighlight %}

* **Gömülü web sunucusu** - Özellikle geliştirme ortamında çok fazla gereksinim duyduğumuz ve genellikle hazır paketler (WAMP, MAMP gibi) kurarak çözdüğümüz, web ortamı için hazırladığımız betikleri deneme problemimizi hiçbir ek paket/yazılım kurmadan artık çözebiliyoruz. Komut satırından PHP içindeki gömülü olarak gelen web sunucusunu çalıştırarak hazırladığımız betikleri web ortamında çalıştırabiliyoruz. Sadece yazdığımız betikleri denemek amaçlı kullanmamız önerilsede beta sürümlerinde yaptığım denemelerde performans olarak ta gayet iyi görünüyor (nginx ve php-fpm kurulumuna karşı denedim). Yine de tekrar belirtelim şu anda bu özellik canlı yayında olan bir proje için uygun bir çözüm *kesinlikle değil*.

* **Oturum üzerinde yüklenen dosyaların durumu/takibi** - (Ecnebi dilinde) `Upload Progress` olarak bilinen ve şimdiye kadar üçüncü parti eklentilerle veya `APC` eklentisi ile çözüm bulduğumuz bu özelliği artık öntanımlı olarak kullanabiliyoruz. Web sayfasından yüklediğimiz dosyaların yükleme durumlarına oturum bilgilerinden (`$_SESSION` süper-global değişkeni içinden) erişiliyor. Detayları ve örnekleri [http://php.net/manual/session.upload-progress.php](http://php.net/manual/session.upload-progress.php){:target="_blank"} adresinden görebilirsiniz.

### Kaldırılan Özellikler

* `safe mode` yapısı tamamen kaldırıldı – Birden fazla kişinin paylaştığı sistemlerde (barındırma hizmeti veren yerler gibi) bu özellik yerine `open_basedir` ve `disable_functions` ayarlarıyla belirli bir seviyede güvenlik önlemi alabilirsiniz.
* `register_globals` ve `magic quotes` yapısı kaldırıldı – Zaten kullanmamamız gereken ve birçok güvenlik açığına sebep olan bu iki özelliğin kaldırılması artık daha dikkatli ve bilinçli kod yazmamız gerektiğini bize zorla hatırlatacak gibi. (Zaten bu iki özelliği kullanmıyoruz değil mi?) `magic quotes` ile ilgili fonksiyonlar (`get_magic_quotes_gpc` gibi) artık öntanımlı olarak `false` değerini dönüyor.
* `break $degisken` ve `continue $degisken` kullanımı kaldırıldı.
* `session_register()`, `session_unregister()`, `session_is_registered()` fonksiyonları kaldırıldı.

Bunlar hariçinde gelen yenilikleri, değişiklikleri ve düzeltmelerin listesini [http://php.net/ChangeLog-5.php](http://php.net/ChangeLog-5.php){:target="_blank"} adresinden bulabilirsiniz. PHP 5.3 sürümünden 5.4 sürümüne geçiş için ise [http://php.net/migration54](){:target="_blank"} adresinde dikkat edilmesi gereken hususlar bulunabilir.


