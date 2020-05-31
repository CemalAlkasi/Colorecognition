# Colorecognition
Projemiz bir renk tanıma projesi olup android üzerine OpenCV eklentisiyle beraber yapılan ve  uygulanılan bir projedir .
Projemizdeki temel amaç gerçek zamanlı kamera üzerinden alınan bir lokasyona ait Rengin tanımını yapıp bunun Renk kodunu bize vermesidir. Bu sayede renklerin karıştırılmaması sağlamakta  ve odak noktada bulunan rengin net değeri sayı (Renk Kodu )bazında ekranımıza yansımaktadır. 
Projemizin yapım amacı  insanların hayatını kolaylaştırmakla birlikte yapılan ince hesaplamalarda istenilen ton ve renk kodunun yakalanması üzerine yazılmış ve geliştirilmiştir.
Uygulamamız android sürümlü ve kamera donanımlı (cep telefonu , tablet , bilgisayar ) herhangi bir cihazda çalışma kapasitesine sahiptir. Sistemimiz Özellikle kullanılan cep telefonları için tasarlanmış olup günlük hayatta kolayca kullanılabilir duruma getirilmiştir. Uygulamamız kullanıcı tarafından ele alındığında kameradan açılan ve istenilen lokasyonu yakınlaştırıp işaretlenmesi üzerine işaretlenen lokasyon bilgileri ile birlikte sorgu yapılıp geri dönüşü Renk kodunu da dahil ederek ekranımıza yansımaktadır  .
Kullanıcı ilgilenilen lokasyonu manuel olarak seçmelidir 
Tanıma işlemi RGB -HSV renk uzayını sayesinde gerçekleşir 
Anroid içerisinde OPenCV kullanarak renk algılama uygulanır Android studio üzerine OpenCVyi eklenti yapıyoruz Web  Kamera Cihazımız üzerinden kullanarak andorid kamerayı aktarıyor ve OpenCV kütüphanesi sayesinde Kamera geri dönüşünü sağlıyoruz OpenCV gerçek zamanlı görüntüleme yapmamıza olanak sağlıyor ve ekrandaki işaretediğimiz noktayı lokasyon bilgileri ve renk koduyla birlikte ekrana yansıtma olayını gerçekleştiriyoruz.
OpenCV kamera blok .
