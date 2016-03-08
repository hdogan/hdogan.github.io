---
layout: post
title: "Yazdan bu yana özet gelişmeler… (Güncellendi)"
---

<p class="message">
    <em>Bu yazı eski blogdan arşiv amaçlı alınmış olduğu için içerikte tutarsızlıklar olabilir.</em>
</p>

Uzun süredir bir şeyler yazamamıştım, en son Linux Yaz Kampı (Temmuz 2012) sonrası neler yaptım neler buldum kısaca bir özet geçeyim. Hem kendim için de bir hatırlama listesi olur.

Etkinlik olarak 7-9 Kasım 2012, Eskişehir Anadolu Üniversitesi'nde gerçekleşen [XVII. Türkiye'de İnternet Konferansı](http://inet-tr.org.tr){:target="_blank"}'na (INET-TR'12) katıldık. Orada [Phalcon - Eklenti olarak sunulan PHP çatısı](https://speakerdeck.com/hdogan/phalcon-eklenti-olarak-sunulan-php-catisi){:target="_blank"} ve [PHP Güvenlik Notları](https://speakerdeck.com/hdogan/php-guvenlik-notlari){:target="_blank"} isimli iki tane sunum yaptım. Daha önce PDF olarak hazırladığım güvenlik kartlarını ve Phalcon, PHP etiketleri bastırıp katılımcılara dağıttık. Söylemeden duramayacağım; Anadolu Üniversitesi ve para derdine düşmüş kurumlar etkinlik için pek ilgisizdi.

23-25 Ocak 2013′de Antalya Akdeniz Üniversitesi'nde gerçekleşen [Akademik Bilişim Konferansı](http://ab.org.tr){:target="_blank"}'na (AB2013) katıldık, 19-22 Ocak arası konferans öncesi düzenlenen kurslar kapsamında PHP'ye Giriş eğitimi düzenlendi. Eğitim sırasında öğrenciler ayaklanma başlattılar ve seçim yaparak sınıfı iki seviye olarak bölmek zorunda kaldık. Kurslar 4 gün sürdüğü için biraz hızlı bilgi yüklenmesi oldu fakat bu bilgilerin en azından bir kılavuz olduklarını düşünüyorum.

Etkinlikler sonrası yine “Sizi davet etsek gelir misiniz?” soruları bolca soruldu, her zamanki gibi şimdiye kadar kimse davet etmedi (Bedava seminer, eğitimi kimse istemiyor sanırım, ücret talep etsek kesin davetler gelmeye başlar).
<!--more-->
[Akademik Bilişim Konferansı](http://ab.org.tr){:target="_blank"}'na katılmadan önce **PHP Geliştiricileri Derneği**'ni kurduk. İlk etkinliğimizde Akademik Bilişim Konferansı öncesi düzenlenen kurslar kapsamında **PHP'ye Giriş** eğitimi oldu. Halen belgelerin tamamlanması ile uğraşıyoruz (yetki belgeleri, makbuzlar, kaşe, v.b.). Aklımızda birçok proje var, yeterli kaynakları bulduğumuzda bunları gerçekleştirmeye başlayacağız. <del>Gelişmeleri http://www.pgd.org.tr adresinden takip edebilirsiniz.</del> **Türkiye PHP Grubu** ise yaşamaya devam edecek. PHP camiasını orada tekrar toparlamaya çalışacağız.

<p class="message">
    <em>PHP Geliştiricileri Derneği'ni yoğun <strong>ilgisizlik</strong> üzerine bu sene tasviye ettik. Hayırlı olsun.</em>
</p>

PHP ve yazılım camiasında takip ettiğim projelerde bazı değişimler yaşandı. Daha önce [Lithium Framework](http://li3.me){:target="_blank"}'ten bahsetmiştim. Halen kararlı (stable) sürüme geçemediler, muhtemelen de geçemeyecekler. Projenin sahibi daha önce kararlı sürüme geçememiş bir proje için ileri geri konuşmuştu fakat şu anda başını çektiği projesi eleştirdiği durumda (en son 2012 yılında kararlı sürüme erişeceklerini söylemişti). Takıntılı bir proje yöneticileri var. Bu sebepten projeyi takip etmekten sıkıldım.

[Phalcon](http://phalconphp.com){:target="_blank"} projesini keşfettim. Phalcon, eklenti (extension) olarak, C dili ile hazırlanmış bir PHP çatısı (framework). Doğal olarak diğer çatılardan daha performanslı, fakat eklenti olarak kurulması yaygınlaşmasının önünde bir engel. Şu anda geliştirmesi hızla devam ediyor. Kararlı sürümünü merakla bekliyorum. [Phalcon - Eklenti olarak sunulan PHP çatısı](https://speakerdeck.com/hdogan/phalcon-eklenti-olarak-sunulan-php-catis) sunumumda detaylarına ve kıyaslamalara göz atabilirsiniz.

Yine önceki yazılarda bahsettiğim ve tercih etmediğim [Symfony Framework](http://symfony.com){:target="_blank"} var. Symfony 1 gerçekten hoşlanmadığım tarzda ve yaklaşımda tasarlanmış bir çatıydı. Fakat Symfony 2 ile birlikte bu görüşlerim değişti. Daha modern bir yaklaşımla hazırlanmış. Çoğu projede Symfony 2 bileşenlerie (component) raslıyorum. Özellikle mikro çatı (micro framework) projelerinin çoğunda Symfony 2 ana bileşenleri temel olarak kullanılıyor (HttpFoundation bileşeni gibi). Symfony ekibinin hazırladığı diğer projelerde ([Silex](http://silex.sensiolabs.org), [Twig](http://twig.sensiolabs.org){:target="_blank"}, [SwiftMailer](http://swiftmailer.org){:target="_blank"}, [Pimple](http://pimple.sensiolabs.org){:target="_blank"} gibi) yaygın bir şekilde kullanılmaya başlandı. Vakit bulursam bunları detaylı şekilde kurcalamayı düşünüyorum.

[Zend Framework](http://framework.zend.com){:target="_blank"} sürüm 2 ile birlikte biraz daha dikkatimi çekse de halen kurcalamaya pek niyetim yok, arada bir sitelerini ziyaret edip gelişmeleri takip edip, belgelerini kurcalıyorum.

CodeIgniter isimli kendisini çatı (framework) zanneden fakat kod kütüphanesi (öbeği) olarak nitelendirdiğim projeye alternatif olarak [Laravel](http://laravel.com){:target="_blank"} projesi var. (Evet FuelPHP ve Kohana projeleri de var fakat pek hoşlanmadığım için bahsetmiyorum). CodeIgniter kullanan tanıdıklarıma ve CodeIgniter öğrenmek isteyenlere Laravel'i tavsiye ediyorum. CodeIgniter hayranlarının ve destekleyenlerin büyük çoğunluğu artık Laravel taraftarı oldular. Siz de öyle yapın bence. (Bakın CodeIgniter'e bağlantı bile vermedim.)

Kısa sürede ortaya bir şeyler çıkartmak isteyenlere ve performans kaygısı olmayanlara (yeni sürümlerinde bu kaygıya da pek gerek yok) önerdiğim [CakePHP](http://www.cakephp.org){:target="_blank"} çatısı, yine her zamanki gibi yakın takibimde.  Yeni yayınlanan 2.3 sürümüyle yapıyı düzeltmeye devam ediyorlar (modernleştirme). Şu anda geliştirmesi devam eden CakePHP 3 ile birlikte isim uzayları (namespaces) ve trait kullanımına geçecekler.

Mobil geliştirme tarafında [Appcelerator Titanium](http://www.appcelerator.com){:target="_blank"} kullanmaya devam ediyorum, 3.0.0 sürümü için yaklaşık 4-5 tane ekleme ve düzeltme göndermiştim (iOS için AlertDialog girişleri, SearchBar bookmark butonu, TableViewRow font seçeneği gibi), sağolsunlar bu sefer pek zorluk çıkartmadan kabul ettiler ve son sürüme dahil edildiler. 3.0.0 sürümü ile birlikte [Alloy Framework](http://docs.appcelerator.com/titanium/latest/#!/guide/Alloy_Quick_Start){:target="_blank"} getirildi. Adobe Flex kullananlar bilir, MXML tarzında bir dil kullanarak (temelinde XML), Allow Framework ile arayüz geliştirebiliyorsunuz. (Dikkat: Pek popüler olmayan Allow PHP Framework ile ismi karıştırılabilir).

Günceleme: HTML, CSS, JavaScript (arayüz) tarafındaki gelişmeler ise; [Twitter Bootstrap](http://getbootstrap.com){:target="_blank"} uygun olduğu sürece projelerde kullanıyorum ve kullanılmasını herkese öneriyorum. Arayüz tarafında hızlıca ortaya bir şeyler çıkartabiliyorsunuz. En son 2003'te yayına açtığım ve yıllardır güncellemediğim [İngilizce Almanca Sözlük](http://www.sozluk.web.tr){:target="_blank"} sitesini Bootstrap ile tekrar düzenledim (arka planında mikro çatı olarak [Slim Framework](http://www.slimframework.com){:target="_blank"} var, arama motoru optimizasyonu (SEO) konusunda SEO Uzmanı Savaş Şahin‘den destek aldım). <del>Bootstrap kullananlar için kaynaklar (eklentiler, temalar gibi) sunan Bootstrap Hero sitesini incelemenizi öneririm.</del>

Mobil web tarafında HP tarafından ilk başta webOS'u için hazırlanmış olan fakat sürüm 2 ile birlikte tüm platformlar için tekrar hazırlanan [Enyo JavaScript Application Framework](http://www.enyojs.com){:target="_blank"}'ü keşfettim, gayet başarılı ve performanslı.

Şimdilik gelişmeler bu kadar. Kod yazmaya, belge okumaya devam...
