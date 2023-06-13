## ls: Dizin İçeriği Listeleme

`ls` komutu, mevcut dizindeki dosyaların ve dizinlerin isimlerini görüntüler. Ayrıntılı olarak görüntülemek için `-la` parametresi ekleyebilirsiniz.

```sh
ls -la
```

## man: Detaylı Dökümantasyon Sunan Komuttur

 `man`, Unix/Linux işletim sistemleri için yazılmış tüm programların detaylı dokümantasyonunu sağlayan bir komuttur.

 ```sh
 man ls
 ```

Bu kod satırı ile `ls` komutunun dökümantasyonuna ulaşabilirsiniz.

## grep: Gelen Sonuçları Verilen Parametreye Göre Filitrelemeyi Sağlar 

`grep`, çıkışta belirtilen karakter dizilerinin bulunduğu satırları veya dosyaları filtrelemekte kullanılır. Örneğin;

```sh
ls -la | grep test1 # test1 adındaki dosya veya klasörlere sahip olan çıkışları filtreleyecektir.
```
veya 
```sh 
ls -la | *test1 dizini* # test1 kelimesini içeren herhangi bir şeyi göstermek için *
```

## rmdir: Boş Dizinleri Silmeyi Sağlayan Komuttur 

Boş bir klasörün silinmesi gerektiğinde `rmdir` komutu kullanılır.

```sh
rmdir test1/
```

## rm -rf: Özyinelemeli Olarak Silmeyi Sağlar 

`rm -rf`, bir dizin ve onun altındaki tüm dosyalar ve klasörler dahil, verilen konumdaki her şeyi siler. Bu işlem geri alınamaz, bu nedenle dikkatli kullanılmalıdır.

## history: Komut Geçmişi

Bu komut satırı ile önceden girilen komutları görebilirsiniz.
```sh
history 
```

## cat: Dosya İçeriğini Ekrana Yazar

Dosyanın içeriği ekrana yazdırılır.
```sh
cat dosyaadi.txt 
```

## tail: Düz Metin Dosyalarının Son Birkaç Satırını Görüntülemek için Kullanılan Bir Unix Komut Satırı Programı
 
Düz metin dosyalarının son birkaç satırını görüntüleyebilirsiniz.

```sh 
tail a.txt # en son 10 satiri goruntuler. Farkli sayida gozuken icin `-n` parametresinden yararlanabilirsiniz; ornegin `tail -n 20 a.txt`.
```
  
 ## cp: Dosya veya Dizin Kopyalamayı Sağlar
 
Bir dosya veya dizinin tamamını ya da belirli bölümlerini başka bir yerdeki adrese taşımanız mümkündür:

 ```sh
 cp kaynak_hedef/dosya_adi.txt yeni_adres/
 ```

## who: Kim Olduğunu Söyler

Bir kullanıcının kim olduğunu gösterir.

```sh
who 
```
 
## whoami: Kullanıcının Kim Olduğunu Gösterir
 
Çalıştırılan oturumun sahibinin adını yazdırır.

```sh
whoami 
```

## tty: TTY, Standart Girişe Bağlanan Dosyanın Stadart Çıkışını Yazan Bir Unix Komutudur 

TTY komutu, standart girişe bağlı olan dosyanın standart çıkış akımını yazdırmak için kullanılır. 

```sh
tty
```

## which: Linux'ta Bir Komutun, Ortam Değişkenlerinde $PATH Değişkeniyle Belirtilen Dizinlerde Arama Yapar ve Yürütülebilir Dosyasını Bulur 

Bu komut ile bir programın tam yolunu öğrenmek mümkündür:

```sh
which ls # /bin/ls gibi.
```

 ## locate: Dosya Arama Aracı 
 
Dosya arama işlemi yapmak için `locate` komutundan yararlanabilirsiniz:

 ```sh
 locate dosya_adi.txt 
 ```
  
 ## pwd: Mevcut Dizini Öğrenme
 
Mevcut dizinin tam adres bilgisini görüntüler.  

 ```sh
 pwd 
 ```
  
  ## date:Tarih Bilgisi
  
Sistem tarihini ve saati göstermek için;

  ```sh   
date  
   ```

## time : Çalışma Sürelerini Verir

Bir komutun ne kadar sürede çalıştığını öğrenmek için;

```sh
time command-name 
```

Umarım bu düzenlemeler notlarınızın daha okunaklı hale gelmesine yardımcı olmuştur.
