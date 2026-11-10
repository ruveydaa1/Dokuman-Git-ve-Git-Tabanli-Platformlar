# Merge

Merge (Birleştirme), Git'te farklı branch'lerde yapılan değişikliklerin tek bir branch altında birleştirilmesini sağlayan işlemdir. Genellikle ayrı bir branch üzerinde geliştirilen yeni özellikler, hata düzeltmeleri veya güncellemeler tamamlandıktan sonra ana branch ile birleştirilir.

Merge işlemi sayesinde farklı geliştiriciler tarafından bağımsız olarak yürütülen çalışmalar, proje bütünlüğü korunarak tek bir geliştirme geçmişinde bir araya getirilebilir.

### Merge İşleminin Çalışma Mantığı

Bir branch üzerinde yapılan geliştirme tamamlandıktan sonra, ilgili branch ana branch ile birleştirilir. Git, iki branch'in commit geçmişini inceleyerek değişiklikleri otomatik olarak bir araya getirmeye çalışır.

Eğer iki branch'te aynı dosyanın aynı bölümü üzerinde çakışan değişiklikler bulunmuyorsa merge işlemi otomatik olarak tamamlanır. Çakışma oluşması durumunda ise geliştiricinin gerekli düzenlemeleri yapması gerekir.

Aşağıdaki şema merge işleminin temel mantığını göstermektedir.

```
main
 │
 ├───────────────●───────────────
 │               ▲
 │               │
 └────► feature-login
         │
         ├──────●──────●
```

Merge işlemi tamamlandığında, **feature-login** branch'inde yapılan değişiklikler **main** branch'ine aktarılmış olur.

### Merge İşleminin Kullanım Alanları

Merge işlemi aşağıdaki durumlarda yaygın olarak kullanılır:

* Yeni bir özelliğin geliştirilmesi tamamlandığında
* Hata düzeltmeleri ana projeye aktarılacağında
* Bakım çalışmaları tamamlandığında
* Test edilen değişiklikler yayınlanmaya hazır olduğunda

### Merge İşleminin Avantajları

Merge işlemi birçok avantaj sağlar:

* Farklı branch'lerde yapılan çalışmalar tek bir proje geçmişinde birleştirilir.
* Ana geliştirme süreci kesintiye uğramaz.
* Ekip üyeleri bağımsız olarak çalışabilir.
* Kod inceleme süreçleri daha düzenli yürütülebilir.
* Proje geçmişi korunarak geliştirme süreci sürdürülebilir.

### Merge Türleri

Git, branch'leri birleştirirken farklı merge yöntemleri kullanabilir. Bunlardan en yaygın olanları şunlardır:

#### Fast-Forward Merge

Fast-Forward Merge, hedef branch üzerinde ek bir değişiklik bulunmadığında gerçekleştirilir. Git yalnızca branch işaretçisini ileri taşıyarak birleştirme işlemini tamamlar ve yeni bir merge commit'i oluşturmaz.

#### Three-Way Merge

Her iki branch üzerinde de yeni commit'ler bulunduğunda Three-Way Merge gerçekleştirilir. Git ortak atayı (common ancestor) kullanarak değişiklikleri birleştirir ve yeni bir merge commit'i oluşturur.

### Dikkat Edilmesi Gerekenler

Merge işleminden önce ilgili branch'in güncel olduğundan emin olunmalıdır. Birleştirme sonrasında oluşabilecek çakışmalar dikkatlice incelenmeli ve yapılan değişiklikler test edilmelidir. Ayrıca merge işleminden önce kod inceleme süreçlerinin tamamlanması, proje kalitesinin korunması açısından önemlidir.

Merge işlemi, Git'in ekip çalışmasını destekleyen en önemli özelliklerinden biridir. Doğru planlanan bir branch yapısı ve düzenli merge süreçleri sayesinde proje geçmişi düzenli tutulabilir, geliştirme süreçleri güvenli bir şekilde yönetilebilir ve ekip üyeleri arasında verimli bir iş birliği sağlanabilir.
