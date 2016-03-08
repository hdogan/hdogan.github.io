---
layout: post
title: "En çok sorulan soru: PHP ile MySQL'e nasıl bağlanırım?"
---

<p class="message">
    <em>Bu yazı eski blogdan arşiv amaçlı alınmış olduğu için içerikte tutarsızlıklar olabilir.</em>
</p>

`PHP ile MySQL'e nasıl bağlanırım?` sorusu şimdiye kadar aldığım (yaklaşık 10 yıldır sorulur) sorulardan en sık sorulanı. İşte bu sihirli sorunun gizemli cevabı:
<!--more-->
### 1. Yöntem: MySQL eklentisini kullanarak.

{% highlight php %}
<?php
$mysql_baglantisi = mysql_connect("adresi", "kullanici_adi", "parola");
mysql_select_db("veritabani_adi", $mysql_baglantisi);
?>
{% endhighlight %}

### 2. Yöntem: MySQLi (MySQL Improved) eklentisini kullanarak.

{% highlight php %}
<?php
$mysql_baglantisi = new mysqli("adres", "kullanici_adi", "parola", "veritabani_adi");
?>
{% endhighlight %}

### 3. Yöntem: PDO eklentisini kullanarak.

{% highlight php %}
<?php
$mysql_baglantisi = new PDO("mysql:dbname=veritabani_adi;host=adres", "kullanici_adi", "parola");
?>
{% endhighlight %}

Örneklerde geçen `adres` MySQL sunucusunun çalıştığı internet adresi (IP adresi de olabilir) (örneğin: localhost), `kullanici_adi` olarak belirtilen MySQL sunucunuzun kullanıcı adı (örneğin: root), `parola` olarak belirtilen yine MySQL sunucunuzun <del>şifresi</del> parolası ve son olarak `veritabanı_adi` olarak belirtilen ise MySQL sunucusunda oluşturduğunuz veritabanı adı.

Bu eklentiler ve MySQL'e bağlandıktan sonra neler yapabileceğinizi öğrenmek için aşağıda verdiğim adresleri inceleyebilirsiniz.

* MySQL eklentisi için detaylı bilgi adresi: [http://tr.php.net/manual/en/book.mysql.php](){:target="_blank"}
* MySQLi eklentisi için detaylı bilgi adresi: [http://tr.php.net/manual/en/book.mysqli.php](){:target="_blank"}
* PDO eklentisi için detaylı bilgi adresi: [http://tr.php.net/manual/en/book.pdo.php](){:target="_blank"}

### Son (ve acı) söz

PHP veya başka bir programlama dilini öğrenmeye niyetlendiğimizde öncelikle birşeyi yapmak için öğrenmek yerine öğrenip birşeyi yapmak daha uygundur (doğal süreç). Programlama mantığını öğrenmeden bir programlama dilini öğrenmek ilerde sadece kendinizi progamlamadan anlamayan ama programlama yaptığını sanan bir yazılımcıya dönüştürür (yazılım uzmanı demeye dilim varmadı, esasında yazılımcı demek te yanlış, herneyse). Ek olarak alışkanlık haline getirmemiz gereken bir konu da başvuru kaynakları. Bir soruyu sormadan önce her zaman yaptığım şey: [RTFM](http://en.wikipedia.org/wiki/RTFM). Lütfen kimse alınmasın, kırılmasın, kızmasın, dost acı söyler diyelim.

Sürç-i lisan ettiysek affola.
