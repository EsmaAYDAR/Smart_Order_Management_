# Smart_Order_Management_
Bu proje, bir işletmenin dijital dönüşüm sürecindeki en temel adım olan veri yapılandırması ve karar destek mekanizmalarını Python programlama dili kullanarak modellemektedir. Proje, ham verinin nasıl anlamlı bilgiye dönüştürüldüğünü gösteren bir mimariye sahiptir.

#Akıllı Sipariş Yönetim Sistemi (Smart Order Management)
 1. Koleksiyonların Gerçek Hayattaki Karşılığı
Yazılım dünyasındaki veri yapıları, aslında fiziksel bir deponun veya bir ofis klasörünün dijital ikizleridir:
Listeler: İşletmenin Gelen Sipariş Defteridir. Siparişlerin geliş sırası önemlidir ve her işlem (aynı müşteri olsa bile) ayrı bir satır olarak kaydedilir.
Sözlükler: Her bir siparişin detay formudur. Müşteri adı, ürünler ve ödeme durumu gibi farklı nitelikteki bilgileri bir arada tutan bir kimlik kartı gibidir.
  
  2.Veri Yapıları: List & Set & Tuple
  
List (Liste):Kaç tane ürün satıldığını bilmek istiyoruz. İki kez monitor satıldıysa, ikisini de saymalıyız.
Set (Küme):Kaç farklı müşterimiz var? sorusuna yanıt verir. Tekrarları ayıklayarak temiz bir müşteri portföyü sunar.
Tuple (Demet):Müşteri ismi ile ödediği tutarı birbirine bağlar. Bu bağın sonradan yanlışlıkla değiştirilmesini engeller.

  3.Boolean ve If Kontrollerinin Sistem Mantığındaki Rolü
Bir sistemin akıllı olabilmesi için karar verebilmesi gerekir.
Boolean Mantığı: Bir sipariş ya ödendi (True) ya da ödenmedi (False) durumundadır. Arası yoktur. 
Kontrol Mekanizması: if-else blokları, sistemin kalite kontrol aşamasıdır. Ödemesi yapılmamış bir siparişin onaylanmasını engelleyerek işletmeyi finansal riskten korur.
4. Bu Projede Hangi Veri Yapısı Neden Seçildi?
Neden Sözlük Listesi?
Sipariş verileri heterojendir (metin, sayı, liste, boolean). Bu karmaşık yapıyı en iyi Dictionary temsil eder. Bunların kronolojik takibi için ise bir List içinde saklanmaları en verimli yoldur.

Neden Set Dönüşümü?
Veri analizinde "Gürültü Ayıklama" (Data Cleaning) çok önemlidir. itemListSet kullanarak, stokta hangi farklı ürünlerin bulunduğunu, adetlerinden bağımsız olarak görebiliyoruz.

Neden Tuple Kullanıldı?
Finansal raporlama yaparken (Müşteri - Toplam Tutar eşleşmesi), bu verinin "sabitlenmiş" olması gerekir. Tuple'ların değişmezlik (immutability) özelliği, veri tabanı tutarlılığı için kritik bir güvenlik katmanı sağlar.
