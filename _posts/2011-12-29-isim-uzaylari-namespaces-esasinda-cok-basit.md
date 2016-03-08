---
layout: post
title: "İsim uzayları - Namespaces: Esasında çok basit."
---

<p class="message">
    <em>Bu yazı eski blogdan arşiv amaçlı alınmış olduğu için içerikte tutarsızlıklar olabilir.</em>
</p>

PHP 5.3.0 ile birlikte gelen yenilikler ve eksiklikler arasında en çok ismini duyduğumuz şeylerden 
biriside `namespace`, Türkçesi (ve benim hoşuma giden, komik olanı) `isim uzayı`.

Esasında isminden de belli olduğu gibi içinde birşeylerin (isimlerin) döndüğü bir uzay olarak düşünebiliriz. Genelde içinde sabit değerler, fonksiyonlar ve sınıflar barındıran öbekler de diyebiliriz. Çok basit bir iki örnekle esasında bir mühendislik gizemi olmadığı anlaşılacak.
<!--more-->
#### Örnek 1: (tavsan.php)

{% highlight php %}
<?php
namespace Tavsan;

const TUY_RENGI = "beyaz";

function zipla($ileri = true) { }
?>
{% endhighlight %}

#### Örnek 2: (kanguru.php)

{% highlight php %}
<?php
namespace Kanguru;

const TUY_RENGI = "kahverengi";

function zipla($ileri = true) { }
?>
{% endhighlight %}

Yukarıdaki iki farklı isim uzayında bulunan `TUY_RENGI` sabiti ve zipla isimli fonksiyon tanımlanmış. 
Normalde PHP’de bu tür bir kod çalıştırdığımızda bu fonksiyonun daha önce tanımlandığına dair bit hata 
mesajı alırız ve sabitimiz de en son atandığı değeri alır (yani `kahverengi` değerini alır). Fakat burada 
sabitimiz ve fonksiyonumuz iki farklı uzayda bulundugu için birbirinden tamamen bağımsız olarak ele 
alınmakta. Peki bunları nasıl kullanırız? Ya da kullandığımız sabitin hangi uzaya ait olduğunu nasıl 
söyleriz. Buyrun:

{% highlight php %}
<?php
include("tavsan.php");
include("kanguru.php");

/* En son tanımlanmış isim uzayımız Kanguru (kanguru.php'yi en son dahil ettik) */

echo TUY_RENGI; /* Kanguru isim uzayına ait TUY_RENGI sabitini döner */

zipla(false); /* Kanguru'ya ait

/* Tavsan isim uzayına ait değerleri ve fonksiyonları çağırmak için */
echo Tavsan\TUY_RENGI;
Tavsan\zipla(true);
?>
{% endhighlight %}

Ek bir bilgi olarak isim uzaylarında PHP içinde tanımlanmış fonksiyonları ve sınıflar ile aynı isimde 
tanımlamalar yapabilirsiniz. Örneğin kendi isim uzayınızda mysql\_connect isimli bir fonksiyon tanımlayabilir 
ve içini doldurabilirsiniz. Burada karşımıza şöyle bir problem çıkıyor: Peki ben gerçekten PHP içindeki 
mysql_connect fonksiyonunu çağırmak istersem? Cevabı: Global isim uzayı. Global isim uzayından birşeyler 
çağırmak için sadece başına `\` eklememiz yeterli (isimsiz isim uzayı olarak düşünün.)

#### Örnek: Global isim uzayı.

{% highlight php %}
<?php
namespace CokBuyukProgram;

function strlen($metin) {
    return "Boyutunu ölçmek istemiyorum!";
}

$sahte_boyut = strlen("deneme");
$gercek_boyut = \strlen("deneme");

echo $sahte_boyut . "\n";
echo $gercek_boyut . "\n";
?>
{% endhighlight %}

Yukarıda bir isim uzayımız ve bu isim uzayı içinde `strlen` isimli bir fonksiyonumuz var. (PHP içinde de 
strlen isimli bir fonksiyon var bunu biliyoruz değil mi?) PHP’den ayrı olarak bu bize boyut ölçmek 
istemediğini söylüyor :) Aşağıdaki satırda ise dikkat ederseniz `\strlen` olarak bir fonksiyon çağırılmış, 
iste bu da global isim uzayı yani PHP içindeki strlen fonksiyonunu tetikliyor.

Sanırım şimdilik bu bilgiler yeterli olur, umarım kafanız daha da karışmamıştır.

Yazı içindeki kodlar tamamen teorik olarak yazıldı. Herhangi bir deneme yapmadım. Eğer bir hata bulursanız 
yazıya yorum olarak gönderebilirsiniz.


