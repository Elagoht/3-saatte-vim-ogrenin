> Bu içerik Furkan Baytekin tarafından [Herkes İçin Linux YouTube kanalı](https://www.youtube.com/channel/UCIWYzLPBy2Av4sgUsRClP0g) için hazırlanmıştır. Bu içeriği kullanabilirsiniz ancak paylaşırken referansta bulunmayı unutmayın.

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

Vim üzerinde 13 adet mod vardır. Bunlar:

* Normal ( )
* Komut ( : )
* Ekleme ( -- Insert -- )
    * Normal Ekleme ( -- (insert) --)
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

* `Y` ya da `yy` ile bulunulan satırı kopyalayabilirsiniz.
* "P" ile bulunulan karakterin öncesine yapıştırma işlemi yapılır.
* "p" ile bulunulan karakterin sonrasına yapıştırma işlemi yapılır.

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

a kaydını buraya yapıştırın vvv:
b kaydını buraya yapıştırın vvv:

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

## Ekleme Modu

Ekleme modu, metinde düzenleme yapmanızı sağlar. Ekleme modu denmesinin nedeni,
bulunan metni silmeden araya karakter eklemesinden kaynaklanır. Var olan metni
silerek yazmaya yarayan mod, değiştirme modudur. Ekleme modunda özgürce yazı
yazabilirsiniz.

### Ekleme Moduna Geçmek

Ekleme moduna geçmenin birçok farklı yolu vardır. Normal modda iken ekleme moduna nasıl geçilebileceğine bakalım.

* `i` ya da `Insert` ile bulunulan karakterde ekleme moduna geçilir.
* `a` (append) ile bir sonraki karakterden başlayarak ekleme moduna geçilir.
* `o` Altta yeni bir satır oluşturarak orada ekleme moduna geçer.
* `O` Üstte yeni bir satır oluşturarak orada ekleme moduna geçer.
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
* `Ctrl+d` satırı bir tab boşluğu ileri alır.

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

* `R` Normal moddayken ile geçiş sağlar.
* `Insert` ile ekleme modundayken geçiş sağlanır.

### Mod Değişikliği

* `ESC` ile normal moda geçilir.
* `Insert` ile ekleme moduna geçilir.

## Normal Değiştirme Modu

Normal ekleme modunun değiştirme modu için geçerli halidir. Yapılan işlemden
sonra değiştirme moduna geçilir.

`Ctrl+o` ile değiştirme modundayken geçiş sağlanır.

deneme tahtası.


