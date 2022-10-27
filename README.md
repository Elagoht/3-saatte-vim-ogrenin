> Bu içerik Furkan Baytekin tarafından [Herkes İçin Linux YouTube
> kanalı](https://www.youtube.com/channel/UCIWYzLPBy2Av4sgUsRClP0g) için
> hazırlanmıştır. Bu içeriği kullanabilirsiniz ancak paylaşırken referansta
> bulunmayı unutmayın.

> Vim Kullanımı

# Giriş

Vim, bildiğiniz gibi terminal üzerinde çalışan gelişmiş bir metin
düzenleyicisidir. Özellikle uzak makinelerle çalışırken konsol üzerinden
kullanımı oldukça kolaylık sağlamaktadır. Bu kolaylık, modları ve kısayolları
bilirseniz mümkün olacaktır. Modların tamamını bilmelisiniz. Ayrıca ne kadar
kısayol bilirseniz uygulama üzerinde o kadar etkin olursunuz. Her modun kendine
has kısayolları vardır. Uygulamaya hakim olmanızı sağlayacak bu kısayollara göz
atalım.

# Vim Modları

Vim üzerinde 14 adet mod vardır. Bunlar:

* Normal ( )
* Komut ( : )
* Ekleme ( -- Insert -- )
    * Normal Ekleme ( -- (insert) --)
    * Ctrl+X ( ^X Mode ) 
* Değiştirme ( -- Replace -- )
    * Normal Değiştirme ( -- (replace) -- )
* Görsel ( -- Visual -- )
    * Görsel Blok ( -- Visual Block -- )
    * Görsel Satır ( -- Visual Line -- )
* Terminal ( [user@pc:~] )
    * Terminalde gezinme ( [Terminal] )
* Arama Modu ( / )
    * Geriye Doğru Arama Modu ( ? )
 
 olarak sayılabilir.

Vim üzerinde basılan tuşlar, karakter olarak alınır ve bunlarda dil ayrımı
yapılmaz. Türkçe ve İngilizce klavyelerde aynı kısayollar geçerlidir.
Karakterleri yazmak farklılık gösterebilir. Örneğin sola eğik çizgi için Türkçe
Q klavyede Alt GR + * tuşlarına basmalısınız.

Şimdi bu modlara bir göz atalım.

**Normal Mod:** Metin üzerinde gezinebileceğiniz ve tuşlara tek başına ya da
sırayla basarak işlemler yapabileceğiniz ayrıca en çok kısayola sahip moddur.

**Komut Modu:** Normal moddaki gibi birkaç karakterle yapılamayan daha uzun ve
belki de parametre alması gereken işlemleri yaptırmak için vardır. Normal modda
iken iki nokta yazarak bu moda geçebilirsiniz.

**Ekleme Modu:** Metne karakter eklemek, yani yazı yazmak için kullanılır.
Birçok farklı şekilde ekleme moduna geçilebilir.

**Normal Ekleme Modu:** İsmi tam olarak bu olmasa da bu mod, ekleme modunda
iken geçilen ve tek seferlik normal mod işlemi gerçekleştirip geri ekleme
moduna geçmenizi sağlayan bir moddur.

**Değiştirme Modu:** Var olan karakterlerin üzerine yazan moddur.

**Normal Değiştirme Modu:** Tek seferlik normal mod işlemi gerçekleştirmesini
sağlayan moddur.

**Görsel Mod:** Metin seçmenizi sağlayan moddur. Bu modun, normal moda benzer,
tuş ve tuş kombinasyonu ile sağlanan işlevleri vardır. Küçük `v` yazarak seçimi
başlatabilir ve aynı karakterle görsel moddan çıkabilirsiniz.

**Görsel Blok Modu:** `Ctrl + v` ile geçilen bu mod, bir dikdörtgen şeklinde
seçim yapmanızı sağlar. Ekrandaki görüntü her şeyi açıklamaktadır. Seçim
yapıldıktan sonra görsel modu ile aynı kısayollara sahiptir.

**Görsel Satır Modu:** `Shift + v` ile geçilen bu mod, seçilen satırın tamamını
kapsayan seçim modudur. Seçim yapıldıktan sonra görsel modu ile aynı
kısayollara sahiptir.

**Terminal Modu:** Vim içerisinde bir terminal emülatörü başlatabilirsiniz. Bu
emülatörü yönetmek için terminalin açık olduğu bir pencerede çalışmanız ve bu
ekranda ekleme ya da değiştirme moduna girmeye çalışmanız yeterlidir. Ardından
vim komutları geçersiz sayılacaktır. Vim'e geri dönmek için `Ctrl + Alt Gr + *
, Ctrl + Alt + n` kısayolunu kullanmalısınız. Bu kısayol aslında `Ctrl + \ ,
Ctrl + n` şeklindedir. Ctrl tuşuna basarak satır sonu kaçış karakteri yazmaktan
ibarettir. Ancak Türkçe Q klavyelerde bu şekilde basılmaktadır.

**Terminalde Gezinme Modu:** Değindiğimiz kısayol basıldığında bu moda geçilir.
Terminal emülatörünü sadece okuma moduna açılmış bir dosya olarak ele alır ve
üzerinde metin seçimi, kopyalama gibi işlemler yapabilmenizi sağlar.

**Arama Modu:** Sağa eğik çizgi karakteri ( / ) ile geçebileceğiniz bu modda
arama işlemlerini gerçekleştirebilirsiniz. Aramaya başlamak için Enter tuşuna
basmalısınız. Böylece normal moda geçiş sağlarsınız. Düzenli ifadeler desteği
sunan bu arama, farklı bir ekran açmayacak, eşleşmeleri belirginleştirecektir.
Normal mod kısayolları ile bu eşleşmeler arasında dolaşabilirsiniz.

# Vim Kısayolları

Şimdi bu modların kısayollarına bakalım.

## Normal Mod

En çok kısayol normal mod üzerindedir. Tamamına bu mod üzerinde değinmeyeceğiz.
Başka modları inceledikçe o modlarla ilgili normal mod kısayollarını da
işleyeceğiz. 

İşlemlere geçmeden önce işlem yapacağınız kısmı seçmek için metin üzerinde
gezme tuşlarına bakalım.

### Metinde Gezinme Tuşları

Alışkan olduğunuz ok yönü tuşları ile gezinebileceğiniz gibi `h, j, k, l`
tuşları ile de gezinebilirsiniz.  `<, v, ^, >`

Üzerinde
gezinilecek
güzel bir
metin parçası

---

`e` ile kelime sonuna (end), `E` ile boşluklarla ayrılan ifadelerin sonuna
(End) gidebilirsiniz.

```rust
fn main() { println!("merhaba dünya"); }
```

---

`w` ile kelime (word) başı, `W` ile boşluklarla ayrılan ifadelerin başına
gidebilirsiniz. İfadenin başındaysanız bir sonraki kelimenin başına gider.

```python
def main(): print("merhaba dünya")
```

---

`b` ile kelime başı, `B` ile boşluklarla ayrılan ifadelerin başına
gidebilirsiniz. İfadenin başındaysanız bir önceki (backward) kelimenin başına
gider.

```c
#include<sdt.io>
int main() { printf("merhaba dünya\n"); }
```

---

`0` ya da `Home` satırın başına, `$` ya da `End` satırın sonuna gider.

```awk
BEGIN { print "merhaba dünya" }
{
    print "çalışılıyor"
}
END { print "güle güle dünya" } 
```

---

`^` karakteri satırdaki ilk, `g_` son yazdırılabilir karaktere gider. 

```python
def main():
    print("merhaba dünya")
    # bu satırın sonunda çok fazla boşluk var                                  
```

---

* `G` ya da `Ctrl+End` dosyanın sonuna, `gg` ya da `Ctrl+Home` dosyanın başına
  gider.
* `(` bir cümle önceye, `)` bir cümle sonraya gider.
* `{` bir önceki paragrafa, `}` bir sonraki paragrafa gider.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum.

### Düzenleme İşlemleri

`Ctrl+a` imleç bir sayının üzerinde değilse sonraki sayıya gider. Bulunulan
sayıyı bir artırır.  `Ctrl+x` imleç bir sayının üzerinde değilse sonraki sayıya
gider. Bulunulan sayıyı bir azaltır.

Burada toplam 2 paragraf var.

---

`~` karakterin büyüklük/küçüklük durumunu değiştirir.

bU Cümleyi Normal cümlE forMatınA getiR!

---

`r` karakterinden sonra yazılacak karakter, o an bulunulan karakter ile
değiştirilir.

Yazım yalnışını düzelt!

### Kesme, Kopyalama ve Yapıştırma İşlemleri

Bu işlemlere, henüz görsel moddan bahsetmeden değineceğiz. Görsel mod
yardımıyla kopyaladığınız metinleri buradaki komutlarla yapıştırabilirsiniz.

* `Y` ya da `yy` ile bulunulan satırı kopyalayabilirsiniz (yank).
* "P" ile bulunulan karakterin öncesine yapıştırma işlemi yapılır (Put).
* "p" ile bulunulan karakterin sonrasına yapıştırma işlemi yapılır (put).

**Kopyalanacak satır**

Bu satırın üstüne yapıştır.
Bu satırın altına yapıştır.

---

`dd` bulunulan satırı keser. 

Satırları sırala.

İkinci satır.
Üçüncü satır.
Birinci satır.

---

`D` bulunulan karakterden satırın sonunda kadar keser.

Aşağıdaki satırın sonunu sonraki satıra taşıyın.

Cevabım kesinlikle hayır!
Kadına şiddete

---

Bu örnekler metinde gezinme komutlarıyla birleştirilebilir.

Alttaki satırın başını kopyalayıp sonraki satırın başına ekleyin. 

Sabahları spor yaparım.
kahvaltı etmeden evden çıkmam.

Bu örnekler y^, dg_, yG, dgg, y$, d0, y(, d} şeklinde çoğaltılabilir.

---

`Delete` ya da `x` bulunulan karakteri keser.

Bu satırı yok edin!

### Kayıtlar

`"` (çift tırnak) karakteri kayıtlara erişimi sağlar. kendisinden sonra yazılan
karakter için bir kayıt oluşturur veya var olana erişir. Eriştikten sonra
kopyalama, yapıştırma gibi işlemleri gerçekleştirebilirsiniz.

---

a ve b kayıtlarına iki farklı satır kopyalayalım.

`a` kaydına bunu kopyaladım.
Bunu ise `b` kaydına kopyaladım.

"a" kaydını buraya yapıştırın vvv:
"b" kaydını buraya yapıştırın vvv:

### İşlemi Geri / İleri Alma

* `u` (undo) yapılan işlemi geri alır.
* `Ctrl+R` (redo) yapılan işlemi yeniden yapar.

Deneme tahtası.

### Girinti Ayarlama

`>>` metni bir tab ileri alır.
`<<` metni bir tab geri alır.

Deneme tahtası.

### Yer İmleçleri

`m` karakterinden sonra yazacağınız karakter için bir işaret (mark)
oluşturulur.  `'` (tek tırnak) karakterinden sonra yazacağınız karakter için
bir işaret varsa oraya gider.

`a` karakteri için işaret noktası.

`b` karakteri için işaret noktası.

### Kılavuz Sayfaları

`K` varsa üzerinde bulunana kelimenin `man` sayfasını açar.

man echo grep glue

### Görünüm Kaydırma

* `Ctrl+u` yarım sayfa yukarı kaydırır.
* `Ctrl+d` yarım sayfa aşağı kaydırır.
* `Ctrl+b` tam sayfa yukarı kaydırır.
* `Ctrl+f` tam sayfa aşağı kaydırır.
* `Ctrl+y` bir satır yukarı kaydırır.
* `Ctrl+e` bir satır aşağı kaydırır.

### Satır İçi Arama

* `F` kendisinden sonra basılacak karakteri satırda geriye doğru arar.
* `f` kendisinden sonra basılacak karakteri satırda ileriye doğru arar.
* `;` aranmaya başlanan karakteri sonraki aramaya devam eder.
* `,` aranmaya başlanan karakteri önceki doğru aramaya devam eder.

### Satır Birleştirme İşlemleri

* `J` alttaki satırı bulunulan satıra ekler ve araya boşluk koyar.
* `gJ` alttaki satırı bulunulan satıra ekler ve araya boşluk koymaz.

Aşağıdaki ikili satırları her iki yöntemle birleştirin.

Birinci satır
ve ikinci satır.

Birinci satır
ve ikinci satır.

### Makrolar

* `q` kendisinden sonra yazılan karaktere bir makro atama işlemini başlatır.
  İşlem başlamışsa sonlandırır.
* `@` kendisinden sonra yazılan karaktere ilişkin bir makro varsa onu
  çalıştırır.
* `@@` çalıştırılan son makroyu tekrarlar.

Bulunulan satırın ilk karakterinin büyüklük/küçüklüğünü değiştiren, satırı
kesen ve iki alt satıra yapıştıran bir makro atayıp kullanın.

satır 1
satır 2
satır 3
satır 4
satır 5

### Pencereler

* `Ctrl+w, s` ekranı yatay bölerek bir pencere ekler.
* `Ctrl+w, v` ekranı dikey bölerek bir pencere ekler.
* `Ctrl+w, w` pencereler arası geçiş sağlar.
* `Ctrl+w, h` soldaki pencereye odaklanır.
* `Ctrl+w, j` alttaki pencereye odaklanır.
* `Ctrl+w, k` üstteki pencereye odaklanır.
* `Ctrl+w, l` sağdaki pencereye odaklanır.
* `h, j, k, l` yerine ok yönleri de kullanılabilir.
* `Ctrl+w, x` iki pencerenin yerini değiştirir.
* `Ctrl+w, q` aktif pencereyi kapatır.
* `Ctrl+w, =` pencere boyutlarını eşitler.
* `Ctrl+w, <` pencereyi daraltır.
* `Ctrl+w, >` pencereyi genişletir.
* `Ctrl+w, -` pencereyi kısaltır.
* `Ctrl+w, +` pencereyi uzatır.
* `Ctrl+w, H` pencereyi sola taşır.
* `Ctrl+w, J` pencereyi alta taşır.
* `Ctrl+w, K` pencereyi üste taşır.
* `Ctrl+w, L` pencereyi sağa taşır.

## Ekleme Modu

Ekleme modu, metinde düzenleme yapmanızı sağlar. Ekleme modu denmesinin nedeni,
bulunan metni silmeden araya karakter eklemesinden kaynaklanır. Var olan metni
silerek yazmaya yarayan mod, değiştirme modudur. Ekleme modunda özgürce yazı
yazabilirsiniz.

### Ekleme Moduna Geçmek

Ekleme moduna geçmenin birçok farklı yolu vardır. Normal modda iken ekleme
moduna nasıl geçilebileceğine bakalım.

* `i` ya da `Insert` ile bulunulan karakterde ekleme moduna geçilir.
* `a` (append) ile bir sonraki karakterden başlayarak ekleme moduna geçilir.
* `o` altta yeni bir satır oluşturarak orada ekleme moduna geçer.
* `O` üstte yeni bir satır oluşturarak orada ekleme moduna geçer.
* `I` bulunulan satırın başına gelerek ekleme moduna geçer.
* `A` bulunulan satırın sonuna gelerek ekleme moduna geçer.
* `s` bulunulan karakteri keserek ekleme moduna geçer.
* `S` ya da `cc` bulunulan satırı keserek ekleme moduna geçer.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum.

### Ekleme Modundan Normal Moda Dönme

Basitçe `ESC` tuşuna basarak normal moda dönebilirsiniz.

### Girinti Ayarları

* `Ctrl+t` satırı bir tab boşluğu ileri alır.
* `Ctrl+d` satırı bir tab boşluğu geri alır.

Metinleri
    aynı hizaya
        getirin.

### Kesme ve Yapıştırma İşlemleri

* `Ctrl+w` imleçten önceki kelimeyi siler.
* `Ctrl+h` Backspace tuşu ile aynı göreve sahiptir.

Lorem ipsum dolor sit amet.

---

* `Ctrl+e` imlecin tam altındaki karakteri yazar.
* `Ctrl+y` imlecin tam üstündeki karakteri yazar.

: 
: Bu satırın aynısını üst satıra yazın.
: Bu satırın aynısını alt satıra yazın.
:

---

`Ctrl+r` geçici bir çift tırnak yazar ve ardından basılan karaktere ilişkin
kayıttaki metni çift tırnak yerine yapıştırır.

"a" kaydındaki metni yapıştırın: 

---

### Metin Tamamlama Seçenekleri

Evet, vim bir metin tamamlama motoruna sahip.

* `Ctrl+n` sonraki (next) seçeneği gösterir.
* `Ctrl+p` önceki (previous) seçeneği gösterir.

Metni örnekte olduğu gibi tamamlayınız.
Lorem ipsum dolor sit amet.
Lo ip do si am.

## Normal Ekleme Modu

Normal ekleme modu, ekleme modunda iken tek seferlik normal mod komutu
çalıştırmanızı sağlar. Ardından yeniden ekleme moduna geçilir.

Ekleme modunda iken `Ctrl+o` ile geçiş yapılır.

Aşağıdaki cümlenin ilk harfini büyük harfe çevirmek için normal ekleme modunu
kullanın.

deneme tahtası.

## Değiştirme Modu

Ekleme modu ile neredeyse aynı olan bu mod, var olan metnin üzerine yazar.
Kısayolları ekleme modu ile aynıdır.

### Değiştirme Moduna Geçiş

* `R` normal moddayken geçiş sağlar.
* `Insert` ile ekleme modundayken geçiş sağlanır.

### Mod Değişikliği

* `ESC` ile normal moda geçilir.
* `Insert` ile ekleme moduna geçilir.

## Normal Değiştirme Modu

Normal ekleme modunun değiştirme modu için geçerli halidir. Yapılan işlemden
sonra değiştirme moduna geçilir.

`Ctrl+o` ile değiştirme modundayken geçiş sağlanır.

deneme tahtası.

## Görsel Modu

Görsel modunun amacı metin seçimi yapmaktır. Seçtiğiniz metinler üzerinde
birçok işlem gerçekleştirebilirsiniz. Standart görsel modunda karakter bazında
seçim yapabilirsiniz.

Seçimi başlatacağınız karaktere gelerek `v` yazarak seçimi başlatabilirsiniz.
Seçimi genişletmek için normal modda bahsedilen "metinde gezinme kısayolları"nı
kullanabilirsiniz.

Seçimi sonuçlandırmanıza gerek yoktur. Seçimde hareket etme kısayolları farklı
işlem kısayolları farklıdır. Bir işlem gerçekleştirildikten sonra otomatik
olarak normal moda geçiş yapılacaktır.

### Kesme, Kopyalama ve Yapıştırma İşlemleri

 Metin seçildikten sonra:

* `y` ile kopyalama yapabilirsiniz (yank).
* `d` ya da `Delete` ile kesme yapabilirsiniz (delete).
* `c` ile kesip ekleme moduna geçebilirsiniz (change).
* `p` ya da `P` ile üzerine yapıştırma yapabilirsiniz (put).

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 

### Son Seçimi Tekrarlamak

Son seçimi tekrarlamak için seçimin başından sonuna yeniden gitmek yerine
kısaca `gv` yazabilirsiniz.

### Büyük / Küçük Karakter Düzenlemeleri

* `~` seçili karakterler büyükse küçük, küçükse büyük yapar.
* `u` seçilen karakterleri küçük harf yapar.
* `U` seçilen karakterleri büyük harf yapar.

bu satırı tamamen büyük harf yapın.
BU SATIRI TAMAMEN KÜÇÜK HARF YAPIN.
bU sATIRI bAŞLIK fORMATINA gETİRİN.
BAĞIRMA BANA!

### Toplu Sayı Artırma / Eksiltme

* Seçim içerisine dahil tüm sayıları artırmak için `Ctrl+a`
  kullanılabilir.
* Seçim içerisine dahil tüm sayıları azaltmak için `Ctrl+x`
  kullanılabilir.

Aşağıdaki sayıları 1'den 4'e kadar olacak şekilde artırın.

```html
<div class="page-button">-24</div>
<div class="page-button">-23</div>
<div class="page-button">-22</div>
<div class="page-button">-21</div>
```

### Girintiler

Normal modda olduğu gibi görsel modunda da girintiler ayarlanabilir. Ancak tek
karakterle işlem gerçekleştirilir. Bir satır içerisinde seçili herhangi bir
karakter varsa, işleme o satır da dahil edilecektir. Satırın tamamen seçili
olmasına gerek yoktur.

* `>` bir tab boşluğu içeri alır.
* `<` bir tab boşluğu dışarı alır.

### Paragraf Araçları

* Uzun satırları ve özellikle paragrafları birden fazla kısa satıra ayırmak
(wrap) için `gw` kullanılır.

* Satırlara ayrılmış paragrafları seçerek `J` tuşuna basarsanız satırları
  birleştirebilirsiniz.

Aşağıdaki paragrafı satırlara bölün.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

### Kayıtlar

Normal modda bahsedilen kayıt özelliklerini burada da kullanabilirsiniz. 

deneme tahtası 1
deneme  2

## Görsel Satır

Görsel modunda karakter bazlı bir seçim yaparken görsel satır modunda satır
bazlı seçim yapılır. Bir satırın yarısını alamazsınız. Bir karakter bile
seçseniz satırın tamamı seçime dahil edilir. Paragraf ve kod bloğu taşıma
işlerinde faydalı olabilir. Bunun dışında kısayollar aynıdır.

Bu moda geçmek için `V` kullanılır.

Aşağıdaki kod bloklarının yerini değiştirin.

```bash
{ 
    say_hello Furkan
}
function say_hello {
    echo hello $@
}
```

## Görsel Blok

Standart görsel modu karakter bazlı, görsel satır modu satır bazlı seçim
yaparken görsel blok modu koordinat düzleminde bir dörtgen oluşturacak şekilde
seçim yapar. Bunu anlamak için `Ctrl + v` ile görsel blok moduna geçerek
aşağıdaki dikdörtgeni seçmeyi deneyin.

###############
#=============#
#=============#
#=============#
#=============#
###############

---

Her zaman satırlar aynı uzunlukta olmayabilir. Aşağıdaki kesik dörtgeni seçmeyi
deneyin ve çalışma mantığını daha iyi anlayın.

###############
#=============#
#==========
#========
        ======#
###############

---

Şimdi daha anlamlı bir yerde kullanalım. Aşağıdaki metinde büyük harflerle
yazılmaması gereken harfleri görsel blok modunu kullanarak düzeltin.

Lorem ipsum dolor sit amet,
CoNSECTETUR adipiscing elit,
SeD DO EIUSmod tempor!
InCIDIDUNT ut labore,
Et dolore magna aliqua.

## Arama Modu

Yukarıdan aşağı, arama yapmak için `/` kullanılır. Ardından arama terimini
yazarsınız. Arama terimi düzenli ifadeler (regular expression) içerebilir.
Enter'e basarak aramaya başlayabilirsiniz.

Eşleşmeler renklendirilecektir. Aramaya başladığınızda normal moda dönersiniz.

* Sonraki eşleşmeye gitmek için `n` kullanılır.
* Önceki eşleşmeye gitmek için `N` kullanılır.

### Arama Operatörleri

Aramalarınızı sınırlandırmak veya çeşitlendirmek için bazı operatörler
mevcuttur.

* `\<` kelime başını ifade eder.
* `\>` kelime sonunu ifade eder.
* `\c` büyüklük / küçüklüğü yok sayarak arar.
* `\C` büyüklük / küçüklüğe bakarak arar. (Varsayılan ayardır ancak bu ayar
  değiştirildiğinde bu operatör kullanılabilir.)

Bu doküman içerisinde `lorem` terimini arayın.
Bu doküman içerisinde `lorem\c` terimini arayın.
Bu doküman içerisinde `eş` terimini arayın.
Bu doküman içerisinde `\<eş` terimini arayın.
Bu doküman içerisinde `eş\>` terimini arayın.
Bu doküman içerisinde `^#.*` terimini arayın.

---

`*` normal moddayken basıldığında üzerinde bulunulan ifadeyi ileri doğru
aramaya başlar. 

## Geriye Doğru Arama Modu

Arama modunun geriye doğru yapılan halidir. `n` ve `N` kısayollarının da yönü
değişir.

`#` normal moddayken basıldığında üzerinde bulunulan ifadeyi geriye doğru
aramaya başlar.

Geri kalan tüm özellikler aynıdır.

## Komut Modu

Vim'in en kapsamlı modudur. Kısayollarla yapılabilen her şeyi yapabildiği gibi
kendine has çok sayıda komutu da mevcuttur. Bu komutların bazıları parametre de
alabilmektedir. Komut moduna geçmek için normal moddayken `:` yazmalısınız.
Ardından komutun devamını yazıp `Enter` tuşuna basarak komutu
gerçekleştirirsiniz.

Komut modunda çok sayıda özellik bulunmaktadır. Burada tamamından
bahsetmeyeceğiz. İhtiytaç duydukça araştırabilir ve yeni özellikleri
keşfedebilirsiniz. Burada en önemlilerinden bahsedeceğiz.

Vim'de bazı ayarlar vardır ve bu ayarlar `:set` komutuna parametre göndererek
düzenlenir. Alt başlıklarda buna sıklıkla rastlayacaksınız.

### Arama Kısayolları

Öncelike ekranınızdaki eşleşmelerin renklendirmelerini kaldırmak için şu komutu
deneyin: `:noh` (no highlight)

---

Arama sonuçlarını renklendirme:

* `:set hlsearch!` arama eşleşmelerinin renklendirilmesini açar/kapatır.
* `:set hlsearch` arama eşleşmelerinin renklendirilmesini açar.
* `:set nohlsearch` arama eşleşmelerinin renklendirilmesini kapatır.

---

Aramalarda büyüklük / küçüklük ayarları:

* `:set ic` ya da `:set ignorecase` ile hassasiyeti kaldırırsınız.
* `:set noic` ya da `set noignorecase` ile hassasiyeti sağlarsınız.
  sadece büyükleri aramayı sağlarsınız.

### Dizin İşlemleri

Çalışılan dizin işlemleri:

* `:pwd` çalışılan dizini yazdırır (print working directory).
* `:cd DİZİN` çalışılan dizini değiştir (change directory). Örneğin `:cd
  Documents` ya da `cd ~/Documents`.
* `:cd` parametre verilmemiş hali, çalışılan dizini kullanıcının ana dizini
  olarak ayarlar.
* `:cd -` normal cd komutunda olduğu gibi bir önceki bulunulan dizini çalışılan
  dizin olarak ayarlar.

### Dosya İşlemleri

Dosyayı kaydetme:

Şu ana kadar dosyada yapılan değişiklikleri kaydetmek için `:w` komutu
kullanılır. Eğer üzerinde çalıştığınız metin bir dosyayla ilişkilendirilmemişse
`:w DOSYAADI` yazarak kayıt edebilirsiniz. Dosya aksi belirtilmedikçe çalışılan
dizinde kaydedilecektir. Yani:

* `:w` var olan dosyadaki değişiklikleri yazar.
* `:w!` salt-okunur modda açılan dosyayı yazılabilir hale getirerek yazar.
* `:w dosya.adı` metni, aynı dizinde "dosya.adı" isimli bir dosyaya kaydeder,
  dosya yoksa oluşturup kaydeder. Farklı kaydet amacıyla da kullanılabilir.
* `:w /dosya/yolu/dosya.adı` belirtilen dizinde belirtilen dosyaya kayıt yapar.
* `:wa` açık tüm dosyaları kaydeder.
* `:wr`, `:wri`, `:writ` ve `:write`; `:w` ile aynıdır.

---

Dosya açma:

Açılan dosyalar yeni bir tamponda (buffer) açılır. Önceden açık olan dosya
kapatılmaz. Önceki tamponda beklemeye devam eder.

* `:e DOSYA` belirtilen dosyayı düzenlemek üzere açar. Belirtilen dosya yoksa
  yeni bir metin dosyası açar ancak kaydedilene kadar dosyayı oluşturmaz.
* `:ed`, `:edi` ve `:edit`; `:e` ile aynıdır.

---

Yeni pencerede dosya açma:

* `:new DOSYA` ile yeni bir pencerede dosya açabilirsiniz. İlgili dosya mevcut
  değilse sonraki kaydetme yeni dosya oluşturulur.
* `:vnew` açılacak yeni pencereyi "vertical" olarak oluşturur.

---

Dosyayı kapatma:

Dosyayı kapattığınız zaman ilgili pencere kapanmış olur. Hiçbir pencere
kalmadığı zaman programdan çıkış yapılır.

* `:q` aktif pencereyi kapatır. Normal moddaki `Ctrl+w, q` ile aynıdır.
* `:q!` değişiklikleri yok sayarak aktif pencereyi kapatır.
* `:qu`, `:qui`, `:quit`; `:q` ile aynıdır.
* `:wq` olarak birleştirerek dosyayı kaydedip pencereyi kapatabilirsiniz.

### Tamponlar (Buffer)

`:edit` ile yeni bir tamponda dosya açıldığını söylemiştik.

* `:bn` ya da `:bnext` (buffer next) ile sonraki tampona geçebilirsiniz.
* `:bp` ya da `:bprevious` (buffer previous) ile önceki tampona geçebilirsiniz.
* `:bd` ya da `:bdelete` (buffer delete) aktif tamponu kapatır.
* `:bd!` ya da `:bdelete!` (buffer delete) aktif tampondaki değişiklikleri yok
  sayarak kapatır.
* `:ls` ya da `:buffers` aktif tamponları listeler.
* `:bSAYI` ya da `:buffer SAYI` belirtilen numaralı tampona gider.

### Görünüm

Renk teması ayarlama:

`:colorscheme TEMA` ile renk teması değiştirilir. `Tab` ile seçenekler
listelenebilir.  Örneğin: `:colorscheme habamax`

---

Satır numarası ayarları:

* `:set number` satır numaraları ekler.
* `:set nonumber` satır numaralarını kaldırır.
* `:set number!` satır numaralarını ekler/kaldırır.

---

Belirli satırlara gitmek:

* `:SAYI` ile belirtilen satır numarasına gidebilirsiniz. Eğer satır sayısından
  fazla bir değer girilirse son satıre gider. Örneğin `:42`
* `:SAYI+SAYI` işlemin sonucu olan satır numarasına gider.
* `:%` dokümanın sonuna gider.
* `:-14` 14 satır geri gider.
* `:+14` 14 satır ileri gider.
* `:#` bulunulan satırın numarasını verir. Satır numaraları görünmezken
  kullanışlı olabilir.

---

Satır taşması ayarları:

* `:set wrap` ekrana sığmayan satırları alt satırdan devam ettirmek için
  kullanılır. Varsayılan ayardır.
* `:set nowrap` satırların alt satıra taşmasını engeller. Görüntü yana doğru
  kayar.

Bu cümle, yukarıdaki ayarları deneyebilmeniz açısından sizler için yazılmış ve gereksizce uzatılmış bir cümledir ve ayarların ikisini de bu cümle üzerinde deneyebilirsiniz.

### Girintiler

* `:set autoindent` otomatik girintiyi açar.
* `:set noautoindent` otomatik girintiyi kapatır.
* `:set smartindent` akıllı girintiyi açar.
* `:set nosmartindent` akıllı girintiyi kapatır.
* `:set expandtab` tab boşluğu yerine boşluk kullanmayı sağlar.
* `:set tabstop=SAYI` tab boşluğunun genişliğini ayarlar.
* `:set shiftwidth=SAYI` girinti boşluğunun genişliğini ayarlar. (<< ,>> ,<, >
  Kullanımlarında etkilidir.)
* `:retab` var olan eski tab boşluklarını yeni kurala göre düzenler.

### Yardım Sayfaları

* `:h KOMUT` ya da `:help KOMUT` kendisinden sonra yazılan komut
  ile ilgili varsa yardım sayfasını açar.
* `:h` ya da `:help` vim'in kendi yardım sayfasını açar.

### Terminal Komutları

`:!KOMUT VE PARAMATRELER` şeklinde bash komutları çalıştırıp
çıktılarını görüntüleyebilirsiniz. Ancak unutmayın komutu
çalıştırdıktan sonra o programa girdi veremezsiniz. Sadece
çıktılarını görüntüleyebilirsiniz. Örneğin:

* `:!ls -la` çalışılan dizindeki dosyaları listeler.
* `:!./%` "%" şu anda çalışılan dosya anlamına geldiği için bu
  dizindeki bu dosyayı çalıştır anlamına gelir. Dosyaya çalıştırma
  yetkisi vermeniz gerekiyorsa onu da bu yöntemle verebilirsiniz.
* `:!chmod +x %` çalışılan dosyaya çalıştırma yetkisi verir.

### Diğer Modların Komutlarını Çalıştırmak

* `:normal!KISAYOL` normal mod kısayollarını normal modda yazmak yerine bu
  şekilde de kullanabilirsiniz.
* `:normal!i` yazarak insert mod komutu kullanabilirsiniz. *Aslında burada
  farkına varmanız gereken şey, normal moddan insert moda geçmenin aslında
  insert adlı bir fonksiyonu çalıştırdığıdır.* Demek oluyor ki `:normal!ibu
  metni yazdır.` yazarsam bulunulan yere "bu metni yazdır." yazmış olacağım.
* `:normal!4ikoyun ` yazarsam 4 kere "koyun " metnini yerleştirir. Normal
  moddan ekleme moduna geçmeden önce de, yazacağınız sayı ekleme modunu
  sonlandırdığınızda o yazıyı kaç kere yazacağınızı da etkiler.

### Görsel Mod ile Diğer Modların Komutlarını Birleştirme

Görsel moda geçip bir komut çalıştırırsanız her satır için o komutu
çalıştırabilirsiniz. Bir alıştırma ile pekiştirme yapalım. Normal modda`A`
komutu ile satırın sonuna gidildiğini hatırlarsınız. "println" ile başlayan
satırları, görsel satır modu ile seçip `:normal!A;` yazarak satırların sonuna
";" eklenmesini sağlayabilirsiniz.

```
fn main() {
    println!("Merhaba Dünya")
    println!("Ben her zaman")
    println!("satır sonuna")
    println!("noktalı virgül")
    println!("koymayı unuturum.")
}
```

### Aranan Metni Değiştirme

Sed komutuna benzer şekilde vimde de satırları düzenleyebilirsiniz. Sed
komutundan farklı bayrakları (flag) olsa da anlaması kolaydır.

Aşağıdaki paragrafta geçen "fatih"leri "mehmet" ile değiştirin. Bunun
için o satırda `:s/fatih/mehmet` komutunu çalıştırmayı deneyin.

"Memleketi fatihçiklere borçluyuz, fatihçikler olmasa burada olamazdık."

---

Ancak sadece ilk eşleşmenin değiştiğini gördünüz. Şimdi aynı metni iki
farklı satırda ele alalım. Görsel satır modu ile iki satırı da seçip
aynı komutu tekrarlayın.

"Memleketi fatihçiklere borçluyuz, fatihçikler olmasa burada olamazdık.
 Memleketi fatihçiklere borçluyuz, fatihçikler olmasa burada olamazdık."

---

Bu sefer de her satırdaki ilk değişikliğin gerçekleştiğini gördünüz.  Bu
değişikliğin satırdaki her eşleşme için yapılmasını isterseniz global
bayrağını (flag) eklemelisiniz. `:s/fatih/mehmet/g` komutu ile yeniden deneyin.

"Memleketi fatihçiklere borçluyuz, fatihçikler olmasa burada olamazdık.
 Memleketi fatihçiklere borçluyuz, fatihçikler olmasa burada olamazdık."

---

Birkaç farklı bayrak bulunmaktadır:

* `g` global anlamına gelir ve satırdaki tüm eşleşmeler için işlem yapar.
* `c` confirm anlamına gelir ve her eşleşme için onay ister.
* `i` case insensitive anlamına gelir ve büyük / küçük harf ayrımı yapmaz.

---

Arama yerleştirme işleminde "/" karakterinin kendisini kullanacaksanız kaçış
karakterleri ile uğraşmak yerine farklı ayraçlar kullanabilirsiniz. Aşağıdaki
komutlar bire bir aynı işlemi gerçekleştirir:

* `:s/foo/bar`
* `:s#foo#bar`
* `:s:foo:bar`
* `:s|foo|bar`

---

Tüm dosyada düzenleme yapmak için tüm içeriği seçmek yerine komutun başına "bu
dosya" anlamına gelen "%" işaretini koyabilirsiniz.

* `%s/foo/bar/gc`

### Dosya Ağacı

`:Sexplore` ya da `:Sex` yeni bir pencerede bir dosya ağacı açmak için
kullanılır.

## Terminal Modu

Vim içerisinde bütünleşik bir terminal emülatörü çalıştırabilirsiniz. Bu sayede
kod yazarken başka bir pencerede kodlarınızı denemek de mümkün olacaktır.
İsterseniz bir terminal arayüzlü dosya gezgini, müzik çalar, internet
tarayıcısı için de kullanabilirsiniz.

Güvenliğiniz açısından önce terminal modundan nasıl çıkılacağını yazıyorum:
`Ctrl+\, Ctrl+n` yani Ctrl basılı iken yeni satır karakteri yazmalısınız. Ancak
bunu Türkçe Q klavyede yazmak için ``Ctrl+Alt Gr+*, Ctrl+n`` yazmalısınız. Bu
kısayol terminalde gezinme moduna geçmenizi sağlar.

Terminal açmak için `:terminal` ya da `:term`  komutu kullanılır. Bahsedilen
pencere taşıma kısayolları ile açılan pencerenin yerini değiştirebilirsiniz.

Açılan pencere, `Ctrl+w` ile başlayan kısayollara duyarlıdır. Ayrıca terminalin
kapanması durumunda pencere de kendiliğinden kapanacaktır.

## Terminalde Gezinme Modu

``Ctrl+Alt Gr+*, Ctrl+n`` ile önceden bahsedildiği üzere bu moda geçiş
yapabilirsiniz. Bu modda ekleme moduna geçme kısayolları ile yeniden terminal
moduna geçiş yapabilirsiniz.

Bu modda metin kopyalama işlemleri yapabilir, geçmişte gezinebilirsiniz.
kopyaladığınız metni başka bir pencereye ya da terminalin kendisine
yapıştırabilirsiniz.

# Kapanış

Vim elbette bundan ibaret değildir. Öğrenilecek daha birçok  özelliği,
özellikle komutları vardır. "~/.vimrc" dosyası oluşturarak kendi vim
konfigürasyonunuzu oluşturabilir ve hatta eklentiler kurarak çok daha gelişmiş
bir metin düzenleyicisi elde edebilirsiniz. Vim'i bir IDE haline getirmek de
mümkündür.
