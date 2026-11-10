# Git Flow

Git Flow, Git tabanlı projelerde branch'lerin nasıl oluşturulacağını, kullanılacağını ve yönetileceğini tanımlayan bir geliştirme modelidir. Bu model, farklı geliştirme süreçlerini belirli branch'lere ayırarak proje yönetimini daha düzenli ve kontrollü hâle getirmeyi amaçlar.

Git Flow özellikle orta ve büyük ölçekli projelerde tercih edilir. Geliştirme, test, sürüm hazırlığı ve acil hata düzeltmeleri birbirinden bağımsız branch'lerde yürütülür. Böylece proje geçmişi daha düzenli olur ve ekip üyeleri aynı proje üzerinde eş zamanlı olarak çalışabilir.

***

### Git Flow'da Kullanılan Branch'ler

Git Flow modeli beş temel branch türünden oluşur.

#### Main Branch

**Main** branch'i, üretim (production) ortamında çalışan kararlı sürümü temsil eder.

Bu branch üzerinde yalnızca yayınlanmaya hazır ve test süreçlerinden geçmiş kodlar bulunur. Yeni geliştirmeler doğrudan main branch'i üzerinde yapılmaz.

***

#### Develop Branch

**Develop** branch'i, aktif geliştirme sürecinin yürütüldüğü ana branch'tir.

Yeni özellikler tamamlandıktan sonra önce develop branch'i ile birleştirilir. Test süreçleri tamamlandıktan sonra ise develop branch'indeki değişiklikler belirli aralıklarla main branch'ine aktarılır.

***

#### Feature Branch

Yeni özellik geliştirmek amacıyla oluşturulan branch'tir.

Her yeni geliştirme için ayrı bir feature branch oluşturulur. Geliştirme tamamlandıktan sonra ilgili branch develop branch'i ile birleştirilir.

Örnek isimler:

* feature-login
* feature-payment
* feature-dashboard

***

#### Release Branch

Yeni bir sürüm yayınlanmadan önce oluşturulan branch'tir.

Bu branch üzerinde son testler yapılır, küçük düzeltmeler gerçekleştirilir ve sürüm yayınlanmaya hazır hâle getirilir.

Yayın tamamlandıktan sonra release branch'i hem main hem de develop branch'i ile birleştirilir.

***

#### Hotfix Branch

Canlı ortamda ortaya çıkan kritik hataları hızlı bir şekilde düzeltmek amacıyla oluşturulan branch'tir.

Hotfix branch'i doğrudan main branch'inden oluşturulur. Düzeltme tamamlandıktan sonra hem main hem de develop branch'i ile birleştirilerek geliştirme sürecinin güncel kalması sağlanır.

***

### Git Flow Çalışma Süreci

Git Flow modelinde genel geliştirme süreci aşağıdaki adımlarla ilerler:

1. Geliştirme çalışmaları develop branch'i üzerinde yürütülür.
2. Her yeni özellik için ayrı bir feature branch oluşturulur.
3. Özellik tamamlandıktan sonra develop branch'i ile birleştirilir.
4. Yayın öncesinde release branch'i oluşturulur.
5. Testler tamamlandıktan sonra release branch'i main branch'i ile birleştirilir.
6. Canlı ortamda kritik bir hata oluşursa hotfix branch'i oluşturulur ve düzeltme tamamlandıktan sonra ilgili branch'lerle birleştirilir.

***

### Git Flow'un Avantajları

Git Flow modeli aşağıdaki avantajları sağlar:

* Düzenli bir branch yapısı oluşturur.
* Büyük ekiplerde iş birliğini kolaylaştırır.
* Geliştirme ve yayın süreçlerini birbirinden ayırır.
* Yeni özelliklerin bağımsız olarak geliştirilmesini sağlar.
* Acil hata düzeltmelerinin güvenli şekilde yönetilmesine yardımcı olur.
* Sürüm yönetimini daha planlı hâle getirir.

***

### Git Flow'un Dezavantajları

Her projede Git Flow kullanılması gerekli değildir. Özellikle küçük ölçekli projelerde veya hızlı geliştirme süreçlerinde fazla karmaşık bir yapı oluşturabilir.

Başlıca dezavantajları şunlardır:

* Branch sayısını artırabilir.
* Süreç yönetimini daha karmaşık hâle getirebilir.
* Küçük projelerde gereksiz iş yükü oluşturabilir.
* Sürekli dağıtım (Continuous Deployment) yaklaşımıyla her zaman uyumlu olmayabilir.

***

### Git Flow Ne Zaman Tercih Edilmelidir?

Git Flow aşağıdaki durumlarda tercih edilebilir:

* Orta ve büyük ölçekli projelerde
* Birden fazla geliştiricinin aynı proje üzerinde çalıştığı ekiplerde
* Düzenli sürüm yayınlanan projelerde
* Test ve yayın süreçlerinin birbirinden ayrılması gereken yazılımlarda

Buna karşılık, küçük ekipler veya hızlı geliştirme süreçleri yürüten projeler için daha basit branch stratejileri tercih edilebilir.

Git Flow, Git ile geliştirilen projelerde en yaygın branch yönetim modellerinden biridir. Doğru uygulandığında geliştirme süreçlerini düzenler, ekip içi koordinasyonu artırır ve sürüm yönetiminin daha güvenli ve planlı bir şekilde yürütülmesine katkı sağlar.
