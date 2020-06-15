# Video 1

Örnek Yok

- -1 +1 arası değer alır
- monoton artan fonksiyon
- global fonksiyon (-sonsuz +sonsuz)

- supervised learning
- unsupervised learning
- reinforcement learning

# Video 2

## Function Approximation

Bu ornekte direkt olarak sonuç axon u buluyor.

n1 = W1 \* p + b

![](2020-06-15-02-55-08.png)

## Performance Index Example

Burada tek node var o yuzden direkt cıkıs eğitme yok
Çıkış fonksiyonu karesel hata

![](2020-06-15-03-01-18.png)

# Video 3

## Gradient İle P Vektörü Projeksiyon Bulma

Cost fonksiyonu verilmiş burada ilerleyip J'yi min yapacak değer aranıyor

Giriş değeri {{0.5},{0}} yön vektörü p {{1},{-1}}

Gradient descent gn Der(F(x)) = {{2x1 + 2x2}, {2x1 + 4x2}} | x = x0
Gradient descent 0 g0 = {{1},{1}}

Burada amac en yuksek p vektorunu bulmak zaten ogreniyoruz ki -g p için en iyisi

![](2020-06-15-03-05-08.png)

## Performance Index Iteration

Gradient descent gn bulunuyor. Daha sonra bu descent vektörü ile
g0 bulunması için gn vektörüne x0 giriş değeri veriliyor.

x1 = x0 - alfa _ g0
x2 = x1 - alfa _ g1
ile iki adım gitmiş alıyor ama burada tek node olduğundan BP olmuyo gibi

Burada soruyu çözmek için Jmin değerini veren xleri bulmak için gn fonksiyonu 0 a eşitleniyor. Ardından en uygun x1,x2... değerleri bulunuyor.

![](2020-06-15-03-11-28.png)

## Taylor Series Expansion

Ne olduğuna bakmadım bile

![](2020-06-15-03-15-45.png)

# Video 4

Örnek olmasa da çok iyi özet dursun burada

![](2020-06-15-03-19-42.png)

## Example Function Approximation

Soru bu sınavda da sorduğu

![](2020-06-15-03-20-21.png)

Soruda 3 adım var çözümler adım adım.

- FeedForward kısmı

  a1 ve a2 çıktı axonlarını buluyor.

  ![](2020-06-15-03-21-07.png)

- BackPropagation kısmı

  burada s1 ve s2 sensitivitiylerini buluyor.

  ![](2020-06-15-03-22-21.png)

- WeightUpdate kısmı

  burada da artık s1 ve s2 sensleri ile weightleri güncelliyor

  ![](2020-06-15-03-23-07.png)

# Video 5

Hebbian öğrenme

Örnek değil ama dursun belki sorar

- Lineer birleştirici

  ![](2020-06-15-03-24-08.png)

- Hebb kuralı

  ![](2020-06-15-03-24-43.png)

- Yığın operasyon

  ![](2020-06-15-03-25-21.png)

## Performance Analysis Example - Hebb Rule

Hebb rule ile örnek sanırım
batch ile /w zero initial weights
3 girişli 1 çıkışlı lineer nöron

![](2020-06-15-03-26-18.png)

- Pseudo inverse 1

  ![](2020-06-15-03-28-45.png)

- Pseudo inverse 2

  ![](2020-06-15-03-29-00.png)

## Relationship to the Hebb Rule Example

Bu sefer psuedo inverse ile çözülüyor.

Wp1 ve Wp2 test işlemleridir.

![](2020-06-15-03-29-41.png)

# Video 6

- Autoassociative memory

  belki çıkar dursun

  ![](2020-06-15-03-31-33.png)

- Variations of hebbian learning

  ![](2020-06-15-03-31-58.png)

## Taylor Series Expansion Example - Hebbian

Taylor serisiyle doğrudan xin kuvvetleri olarak yazıyoruz
x\* = 0 olduğundan artık adı Maclorien or stmlike that serisi
Burada serinin ilk 1,2 ya da 3 terimini aldın mı zaten yaklaşık eşittir oluyor böyle de çözülebiliyormuş

![](2020-06-15-03-33-00.png)

## Directional Derivatives Example - Hebbian

Ön bilgi öyle boş

![](2020-06-15-03-34-55.png)

önce gradient vektör bulunuyor.
gn e x0 yazılıyor.
p vektörü boyunca yönsel türevi alınıyor. sonuç.
istersen hessian matrisini der(gn) ile bulabilirsin.
! Hessian 2x2 matrix unutma

![](2020-06-15-03-35-40.png)

## First - Second Order Condition Example - Özdeğer

gradient bulunur.
çözümü için gradient 0 a eşitlenerek min yapar x ler bulunur -1, 0.5 iterasyona gerek yok.

gn tekrar türevi ile hessian matrisi bulunur 2x2

Burada hessian matrisinden lambda _ birim matris çıkarıp determinantını alıyoruz. sol yukarı _ sağ alt - sol alt \* sağ yukarı
kökler özdeğerleri verir özdeğerler pozitifse uydu ayrıca minimum strong/global

![](2020-06-15-03-38-06.png)

- Quadratic functions

  Quadratic falan çıkarsa bak buraya

  ![](2020-06-15-03-40-45.png)

# Video 7

- Second directional derivative

  belki çıkar

  ![](2020-06-15-03-42-24.png)

- Circular hollow

  ![](2020-06-15-03-42-52.png)

- Elliptical hollow

  ![](2020-06-15-03-43-12.png)

- Elongated saddle

  ![](2020-06-15-03-43-40.png)

- Sationary valley

  ![](2020-06-15-03-44-11.png)

- Quadratic Function Summary - Stationary Point

  ![](2020-06-15-03-44-45.png)

# Video 8

## Steepest Descent - İki Değişkenli Gradient Problemi

Problemi çözün demek türevi sıfıra eşitlemek.
Türev = gn = der Fx
Nonlineer olduğundan 0 a eşitleyince çözülmüyor çözülmeyince iterasyon lazım
Soru vizedeki soru çözüm de aynı niye tekrar işliyoruz bilmem
sonuç -1 0.5

![](2020-06-15-03-45-56.png)

- Stable learning rates (quadratic)

  sonraki örneğin konusu bu
  d özdeğer

  ![](2020-06-15-03-49-00.png)

## Stable learning rates (quadratic) Example

A (hessian) - lambda \* I = 0 ile özdeğerler bulunur
kökler özdeğer

A _ z = lambda _ z -> z özdeğer vektörü

![](2020-06-15-03-49-33.png)

- Minimizing along a line
  quadratic ifadede alfa güncellemesini direkt böyle yapabilirmişiz

## Minimizing Along a Line - Quadratic Alfa Hesabı Example

Fx quadratic verilmiş
gradient bulundu
po = -g0 alıyoruz.
a0 hesaplıcaz
sonra da x1 = x0 - a0 \* g0
her iterasyonda bu şekilde learning rate değiştiriyoruz. Onu bile öğretiyoruz wow

![](2020-06-15-03-54-35.png)

- Newton's method

  Elma

  ![](2020-06-15-03-56-09.png)

## Newton Algoritması Newton's Method Example (Quadratic)

Aynı soruyu newton methodu ile bulma
Gradient bulduk
g0 bulduk
Hessian bulduk
x1 = güncelleme denklemi = newton's method
çıkan x1 sonucunu gn e yazarsak
Niye bilmiyom burada g1 için yazınca sonu 0 geldi 0 gelince de xi hesaplamasında x2 = x1 = x\* oldu optimum x bulundu tek iterasyonla çözmüş he bu methodla hep bi adımda bulunuyormuş çünkü quadraticmiş

![](2020-06-15-03-57-16.png)

## Newton Algoritması Newton's Method Example (Non-Quadratic)

Quadratic olmazsa tekte bulmuyor ama yine hızlı
iterasyon yapa yapa gidiyoz yine bi x1 bulma fonksiyonu farklı

![](2020-06-15-04-00-41.png)

## Conjugate Gradient Algorithm Example - Sorumlu değişmişiz

Ama ne olacağı belli olmaz laz bu

![](2020-06-15-04-02-44.png)

- ADALINE network

  Adaptive lineer
  R girişli S çıkışlı purelin fonksiyon a = n(Wp+b) = Wp+b

  ![](2020-06-15-04-03-16.png)

- Two input adaline network

  iki girişi var bi numarası yok

  ![](2020-06-15-04-04-22.png)

- Error analysis quadratic adaline

  çıkmaz

  ![](2020-06-15-04-05-50.png)

## Steady State Response - Conditions for Stability Example

R bulunuyor korelasyon yapıyoruz
matrisin özdeğerleri bulunuyor
en büyük özdeğerler de alfa bulunuyor

![](2020-06-15-04-07-13.png)

# Dönem Ödevi Açıklama

Yapay sinir ağı ile ülke bayrağı tanıma

Yapay sinir ağı projemizde nöron ağlarına 100 ülke bayrağı tanıttık.
Yapay sinir ağı kendisine verilen bayrakları rastgele şekilde deneyerek öğrendi.
Ardından test için üzerinde farklı şekilde oynanmış bayrakları sinir ağına girdi olarak verdik
ve sinir ağı başarılı şekilde bayrakları tanıdı.
