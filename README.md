![ic_launcher](https://user-images.githubusercontent.com/63213536/83352027-5c091900-a351-11ea-8099-6a884f450279.png)# Colorecognition
Projemiz bir renk tanıma projesi olup android üzerine OpenCV eklentisiyle beraber yapılan ve  uygulanılan bir projedir .
Projemizdeki temel amaç gerçek zamanlı kamera üzerinden alınan bir lokasyona ait Rengin tanımını yapıp bunun Renk kodunu bize vermesidir. Bu sayede renklerin karıştırılmaması sağlamakta  ve odak noktada bulunan rengin net değeri sayı (Renk Kodu )bazında ekranımıza yansımaktadır. 
Projemizin yapım amacı  insanların hayatını kolaylaştırmakla birlikte yapılan ince hesaplamalarda istenilen ton ve renk kodunun yakalanması üzerine yazılmış ve geliştirilmiştir.
Uygulamamız android sürümlü ve kamera donanımlı (cep telefonu , tablet , bilgisayar ) herhangi bir cihazda çalışma kapasitesine sahiptir. Sistemimiz Özellikle kullanılan cep telefonları için tasarlanmış olup günlük hayatta kolayca kullanılabilir duruma getirilmiştir. Uygulamamız kullanıcı tarafından ele alındığında kameradan açılan ve istenilen lokasyonu yakınlaştırıp işaretlenmesi üzerine işaretlenen lokasyon bilgileri ile birlikte sorgu yapılıp geri dönüşü Renk kodunu da dahil ederek ekranımıza yansımaktadır  .
Kullanıcı ilgilenilen lokasyonu manuel olarak seçmelidir 
Tanıma işlemi RGB -HSV renk uzayını sayesinde gerçekleşir 
Anroid içerisinde OPenCV kullanarak renk algılama uygulanır Android studio üzerine OpenCVyi eklenti yapıyoruz Web  Kamera Cihazımız üzerinden kullanarak andorid kamerayı aktarıyor ve OpenCV kütüphanesi sayesinde Kamera geri dönüşünü sağlıyoruz OpenCV gerçek zamanlı görüntüleme yapmamıza olanak sağlıyor ve ekrandaki işaretediğimiz noktayı lokasyon bilgileri ve renk koduyla birlikte ekrana yansıtma olayını gerçekleştiriyoruz.
OpenCV kamera blok .

![Adsız](https://user-images.githubusercontent.com/63213536/83352126-19940c00-a352-11ea-987c-63d982ccc0e3.png)

Sistemimiz renk açısından oldukça verimli bir içeriğe sahip olıp bunu mobil kamera ile hızlı tanıma olanağı sağlamaktadır.
Uygulamamızın en güzel ve verimli hali renk tonlarını değiştiren unsurları dikkate alarak örneğin bir rengin ışık vurması ile kameraya yansıyan halini daha açık yada net veyahut koyu tonlarını tanıyarak tam anlamıyla o renk kodunun yaklaşık değerini bize sunar.
Buda çok az bir yanılma payı olduğundan dolayı kullanım amacını daha iyi yerine getirmemizi sağlar . 
Uygulamamız herhangi bir Ön işleme gerekmediğinden dolayı Renk tabanlı algılama algoritmamız oldukça hızlı bir şekilde çalışmaktadır.
Çoğu piksel ortalama  hesaplama maliyetini azaltan durumun ilk aşamaları tarafından dışlanır Diğer işleme aşamaları kalan yanlış hesaplamaları filtreler  ve işaretleyiciye yaklaşık mesafeyi hesaplar.
Sistemimiz yüksek hesaplama verimliliği elde ederken verimli ve doğru olan bir işaretleyici algoritma imkanı sunuyoruz . Sistemimizdeki lokasyon bilgileri dahilinde olan bilgiler sayesinde konum doğruluğu sağlayarak sistemimizin verimli çalışmasını sağlıyor ve oradaki renk kodlarının daha net olmasına imkan sağlıyoruz. Aşağıdaki resimde kullandığımız (Samsung galaxy s7 prime ) cep telefonumuzda uygulamamızın çalıştırılmış halini görmekte ve ekranda görüldüğü üzere (x,y) değerleri lokasyon (color) ise renk tanıtımı için gereken bölümümüzdür.

![1](https://user-images.githubusercontent.com/63213536/83352159-5bbd4d80-a352-11ea-97ea-a893df726948.png)

Artırılmış gerçeklik ve robotik lokalizasyon gibi uygulamalar için oldukça hızlı ve sağlam algılama sağlayan bir dizi işaretleyici önerilmiştir. Uygulamamız ortamda bulunan koşullar üzerine benzersiz olarak tanımlanabilir renkleri seçme olanağına sahiptir .Dikkatli renk seçimi ve uygun işaretleme olmadan renk işaretleyicisinin algılanması ,birçok dikkat dağıtıcı ortamdaki körlük veyahut aydınlatmada  büyük değişiklerle gerçekci koşullarda başarılı olacaktır . Bu sunumda alınan konu renk işaretleyicileri , ayırt edilebilirliği artırmak için birden fazla renk(algılanabilir ve kameranın çalıştığı ortamdaki tüm renkler) kullanılır ve aydınlatma değişkenliğini açıkca dikkate alan renktabanlı bir algortima tarafından sağlanır .

![2](https://user-images.githubusercontent.com/63213536/83352174-7a234900-a352-11ea-8173-ef78fdd14b99.png) 

Yukarıdaki çalışmamızda ve aşağıda görüldüğü üzere içerisinde birden fazla renk tonu bulan fosforlu kalemlerimizi kamera karşısına koyarak bir örnek oluşturduk Renkler maximum ayırt edicilik olması için farklı tonlar ,yansıyan beyaz arka plan ve ışıklı bir ortam kullanıldı .Burada ışığın yansıyan bir ortamda olması seçicilik özelliğini tamamen etkilemesiyle birlikte örenekte görüldüğü üzere uygulamamızın netliği gayet iyidir. 

![3](https://user-images.githubusercontent.com/63213536/83352210-accd4180-a352-11ea-8c4f-1802f8d585fb.png)

Sistem tüm yüzeylerin RGB değerlerini Tanıyacak şekilde tasarlanmış olup HSV sayesinde elde edilir. Aydınlatıcı değişmediği sürece odaklanılan noktanın renk kodu ve doğruluk oranı oldukça yüksektir aslında renk kümelerinin içindeki renk yayılımı yansıma yani aynasak bileşene bağlıdır çünkü yüzey rengiyle birlikte aldığımız lokasyonun aydınlatıcı rengide kaydedilir . Algılama algoritmamız değişen bakış açısı ve değişen aydınlatıcı altında işaretleyicideki dört sektörün algılanan renk modeline dayanmaktadır. İşaretçinin düz bir yüzeyde olduğunu ve aydınlatmanın işaretleyici üzerinde sabit olarak kabul edilebileceğini varsayıyoruz (yani, onu geçen gölge çizgiler yoktur). Farklı aydınlatıcıların etki ettiği görüntüde yüzeyin renk tahminin değiştiğini görmekte ve renk kodlarının farklı olduğunu gözlemlemekteyiz .Uygulamada  Renk temelli sınıflandırıcının tasarımı için RGB  değişiklikleri dikkate alınmalı bununla birlikte kameradaki renk filtreleri ,kameranın duyarlılığı ve bakış açısıda değerlendirilir. Uygulamanın daha net sonuç verebilmesi amaçlı medyan filtreleme tekniği kullanılabilir .

![20120307004345](https://user-images.githubusercontent.com/63213536/83352227-c79fb600-a352-11ea-87c5-2a637fff3b82.png)

İdeal olarak kamera tarafından üretilen renk değerleri (RGB) ve  ortalama hesaplarına dayanan bir kombinasyona sahiptir Uygulamada bu kombinasyon çeşitli faktörler nedeniyle dahada karmaşıktır renk değerleri bir renk mozaiği sayesinde elde edilir ve buna gürültü ışık vb ölçümler eklenir doğrusal olmayan düzeltme  ölçülen değerleri sıkıştırır ve nokta düzeltmesi renk lokasyonunun bağımsız yeniden ölçeklendirilmesini uygular . Sorunsal olmayan uygulama ve nokta düzeltme işleminden önce modellenmesi ve telafisi gerekir fakat bizim uygulamamız android uygulama oldupundan ve bir çok kameralı cihaz üzerinde kullanılabildiğinden kameraların beyaz nokta kalibrasyonunu sabit bir değere ayarlanmasına izin vermektedir doğrusal olmayan düzeltme ise kalite düzeyi artırılmış kameralarda görmezden gelinecek kadar az bir etki yaratmaktadır (bu ucuz kamera veya cep telefonlarında ihmal edilemeyecek büyüklüktedir)
Uygulamamız, çok çeşitli izleme koşulları ve arka plan altında çok düşük hata ve yanlış alarm oranı ile sağlam algılama gerektirir. Aynı zamanda, bir cep telefonuna uygulandığında, saniyede birkaç karenin makul bir yüksek çözünürlükte analiz edilmesini sağlamak için algoritmanın çok hafif olması gerekir. 
Uygulamayı kullanırken kameradan öncelikle seçeceğimiz alanın daha net ve doğru bilgi vermesi için o alanın renk  doygunluğuna dikkat ediyoruz renklerin oldukça doygun ve çevresel faktörlerden etkilenmemiş hali bize daha doğru ve net sonuç verecektir Renkler ne kadar doygun olursa olsun uygun ortam ve çevresel faktörler aydınlatma yansıtma gibi faktörler olmadığı sürece uygulamadan verim alamayız çünkü kamera neyi görürse onu bize yansıtacaktır Yaptığımız deneylerde aynı cisimdeki rengin farklı ışık ve ortamlarda farklı sonuçlar verebileceğini göz önünde bulundurmamız gerekiyor yanısıra kameradaki hassasiyet ve gürültününde burda büyük etkisi vardır .
Uygulamamız farklı renk tonlarında farklı ortamlarda test edilmiş ve başarı sağlandığı gözlenmiştir .








