---
layout: post
title: "Ne için, nerede, ne kullanıyorum?"
---

<p class="message">
    <em>Bu yazı eski blogdan arşiv amaçlı alınmış olduğu için içerikte tutarsızlıklar olabilir.</em>
</p>

Bazen arkadaş arasında `Bunun için ne kullanıyorsun?` diye sorular sorulabiliyor veya yeni birşey bulduğumuzda heyecanla bahsediyoruz. Güncel olarak ne için, nerede, ne kullandığımı derleyip toplamanın hem benim için hem de merak edenler (varsa) için iyi olacağını düşündüm.
<!--more-->
### Sunucu Yazılımları

İşletim sistemi olarak tabiki Linux ([RedHat Enterprise](http://www.redhat.com){:target="_blank"}, yoksa [Debian](http://www.debian.org){:target="_blank"}). Web sunucu olarak da [nginx](http://www.nginx.org){:target="_blank"} ve yerine göre [Apache HTTP Server](http://httpd.apache.org){:target="_blank"}. Daha önce [LigHTTPD](http://www.lighttpd.net){:target="_blank"} kullanma fırsatım oldu, statik dosyalar ve streaming medya için kullanmıştım, geliştirme süreci biraz yavaşladı diye hatırlıyorum. SQL sunucusu olarak [MySQL](http://www.mysql.com){:target="_blank"} ve gerekirse [PostgreSQL](http://www.postgresql.org){:target="_blank"} kullanmayı tercih ederim. 2000 yılından itibaren PostgreSQL kullanan bir proje hazırlamadım fakat arada bir takip ediyorum. Günümüzde bolca ismi duyulan ve moda olan `NoSQL` kavramı ile [MongoDB](http://www.mongodb.org){:target="_blank"} ve key-value (anahtar-değer) veritabanlarından [Redis](http://redis.io){:target="_blank"}, disk üzerinde tutulacak bir veri gereksinimi olmadığında ise [Memcached](http://memcached.org){:target="_blank"} (özellikle oturum yönetimi veya önbellekleme/cache için). Memcached'in verileri disk üzerine de yazan ve `sharding` kavramı getiren ve yönetim paneli gibi özellikleri olan <del>Membase</del> [CouchBase Server](http://www.couchbase.com){:target="_blank"} projesini de takip ediyorum (Redis’e rakip diyebiliriz). Tam metin arama da ise şimdiye kadar [Sphinx](http://sphinxsearch.com){:target="_blank"} ve [Apache Lucene](http://lucene.apache.org){:target="_blank"} deneme fırsatım oldu, fakat Sphinx'in kullanımı daha hoşuma gitti, eğer Lucene'ı Zend Framework ile kullanacaksanız dikkatli olun. Zend Framework içinde gelen Lucene kütüphanesi kaynak kullanı konusunda biraz problemli.

### İnternet Programlama

Yıllar önce Perl ile başlamıştım fakat şu anda tabiki [PHP](http://www.php.net){:target="_blank"} tercih ediyorum. [Python](http://www.python.org){:target="_blank"} ve [Ruby](http://www.ruby-lang.org){:target="_blank"} dillerini uzun süredir inceliyorum fakat 
bir proje çıkartma fırsatım olmadı. (Sadece Python ile Linux üzerinde basit bir socket sunucu hazırlamıştım). Bunlar hariçinde JavaScript ile [node.js](http://nodejs.org){:target="_blank"} platformu üzerinde birşeyler yapma planlarım var, <del>bu yıl</del> geçtiğimiz yıl içerisinde adından çokca bahsettirdi. İlerde kurcaladığımda bununla ilgili bir yazı yayınlamayı da düşünüyorum.

### Mobil Programlama

Şimdiye kadar sadece iOS uygulamaları üzerine uğraşma fırsatım oldu. Çoklu platform desteği ile [Appcelerator Titanium](http://www.appcelerator.com){:target="_blank"} platformunu kullandım ve şimdiye kadar hazırladığım 10'a yakın uygulama yayınlandı <del>(sadece iOS için)</del>. JavaScript bilenler için oldukça basit ve hızlı şekilde iOS, <del>ve</del> Android, BlackBerry, Tizen ve Windows platformları üzerinde uygulama geliştirme için bir platform. Belge olarak biraz eksik ama örneklerden ve API belgelerinden hızlıca öğrenebilirsiniz. Daha sonra biraz Xcode ile Objective-C denemelerim oldu fakat zaman darlığından devam edemedim. Objective-C’nin dil yazımı biraz garip gelebilir fakat çok zor değil, programlama bilgisi olanlar hızlıca çözebilir. Esas zorlayan kısım Xcode ve Cocoa Framework’e alışmanız. İlerde Appcelerator Titanium ve mobil programlama (muhtemelen Objective-C) ile ilgli birkaç yazı yazma planlarım var.

### PHP Çatıları (Framework)

Çok fazla işim düşmese de uzun zamandır [CakePHP](http://www.cakephp.org){:target="_blank"} projesini takip ediyorum ve deneme 
fırsatım oldu. Performans takıntınız yoksa ve hızlıca birşeyler üretmek istiyorsanız PHP çatıları arasında en 
basiti diyebiliriz. CakePHP projesinden ayrılıp daha sert kuralları olan, PHP 5.3 ve üst sürümleri 
destekleyen ve performans olarak daha iyi olan [Lithium Framework](http://li3.me){:target="_blank"} güzel bir proje. Oldukça 
esnek olan Lithium Framework’ün halen kararlı sürümü yok fakat şu anda bazı startup projelerinde kullanılıyor. 
Yazımı ve kullanımı keyifli ve oldukça tertipli düzenli bir çatı. İlerde CakePHP ve Lithium Framework 
konusunda yazılar görebilirsiniz. [Zend Framework](http://framework.zend.com){:target="_blank"}'ü ise her zaman uzaktan takip 
ediyorum. Symfony, <del>Yii,</del> CodeIgniter, Kohana, FuelPHP gibi çatıları tarzları ve yaklaşımları yüzünden hiç 
beğenemedim. (Aman dikkat, bu bundan hızlıdır, bu çatı bunu döver gibi bir söylemim yok, sadece tercih ve 
zevk meselesi.)

### Kod Editörü

<del>Linux üzerinde genellikle GNU nano veya Pico kullanıyorum. Microsoft Windows üzerinde ise Sublime Text 2, yoksa Notepad (plus plus değil, bildiğimiz düz Notepad). Mac üzerinde ise her zaman TextMate, fakat terminal üzerinde yine GNU nano kullanıyorum, genellikle elim terminale aşırı ve abartılı şekilde aşina olduğu için GNU nano kullanımım daha yüksek oranda.</del>
Kodlama için kullandığım araçlar neredeyse tamamen değişti, Linux ve OSX üzerinde [GNU nano](http://www.nano-editor.org){:target="_blank"}, OSX üzerinde [Sublime Text](http://www.sublimetext.com){:target="_blank"} ve [Atom](https://atom.io){:target="_blank"}, IDE olarak ta [PHPStorm](https://www.jetbrains.com/phpstorm/){:target="_blank"} kullanıyorum. 
Microsoft Windows artık kullanmadığım için genel olarak bir araç tercihim yok, ama kullanmam gerekirse muhtemelen editör olarak Sublime Text veya Atom ve IDE olarak PHPStorm kullanırdım.

### Kaynak Kod / Sürüm Yönetimi

Tüm sistemler üzerinde [Git](http://git-scm.com){:target="_blank"} veya [Subversion](http://subversion.tigris.org){:target="_blank"} (SVN), fakat Git daha çok hoşuma gidiyor.

### Tarayıcı

<del>Mac</del>OSX üzerinde [Safari](http://www.apple.com/safari){:target="_blank"} (<del>neden Google Chrome kullanmadığımı bilmiyorum</del> Google Chrome halen 64bit uyumlu sürümünü çıkartmadı ve benim gözlemlerimde Safari'ye göre daha yavaş), Microsoft Windows üzerinde [Google Chrome](http://ww.google.com/chrome){:target="_blank"}, fakat bir siteyi denemem gerekirse (ki uzun zamandır böyle bir gereksinimim olmadı) [Mozilla Firefox](http://www.mozilla.org/firefox){:target="_blank"} ve [IETester](http://www.my-debugbar.com/wiki/IETester/HomePage){:target="_blank"}, Linux üzerinde ise [Lynx](http://lynx.isc.org){:target="_blank"} metin tarayıcısını kullanıyorum.

### Teknoloji / Sektör Takip

Twitter üzerinden arkadaşlar sağolsun birşeyleri `retweet` ediyorlar devamlı, günde sayını bilmediğim kere 
[TechCrunch](http://techcrunch.com){:target="_blank"}, [Read Write Web](http://www.readwriteweb.com){:target="_blank"}, [Smashing Magazine](http://www.smashingmagazine.com){:target="_blank"}, [Webrazzi](http://www.webrazzi.com){:target="_blank"} ve [GitHub](https://github.com){:target="_blank"} üzerinden projelerdeki yenilikleri takip ediyorum. 
Genelde günde bir defa [MacRumors](http://macrumors.com){:target="_blank"}, [9To5Mac](http://9to5mac.com){:target="_blank"} ve [Culf of Mac](http://www.cultofmac.com){:target="_blank"} bloglarını takip ediyorum. 
Hafta bir ve aklıma geldikçe de [myNoSQL](http://nosql.mypopescu.com){:target="_blank"} bloğunu takip ediyorum. 
Genelde RSS okuyucu kullanma alışkanlığım olmadığı için sitelere girip takip ediyorum.
