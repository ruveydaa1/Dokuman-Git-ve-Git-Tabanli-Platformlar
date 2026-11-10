# Branch Mantığı

Branch (dal), Git'te proje geçmişinden bağımsız olarak yeni bir geliştirme süreci oluşturmayı sağlayan yapıdır. Her branch, belirli bir commit'ten başlayarak kendi değişiklik geçmişini oluşturur. Bu sayede geliştiriciler, ana projeyi etkilemeden yeni özellikler geliştirebilir, hataları düzeltebilir veya farklı çözümler üzerinde çalışabilir.

Varsayılan olarak oluşturulan ana branch genellikle **main** veya **master** adını taşır. Yeni oluşturulan branch'ler başlangıçta ana branch ile aynı içeriğe sahiptir. Ancak üzerinde değişiklik yapılmaya başlandığında, her branch kendi geliştirme geçmişini oluşturmaya devam eder.

### Branch Kullanımının Amacı

Branch kullanımının temel amacı, farklı geliştirme çalışmalarını birbirinden bağımsız olarak yürütmektir. Böylece devam eden çalışmalar ana kod tabanını etkilemez ve geliştirilen özellikler tamamlanıncaya kadar ayrı bir ortamda test edilebilir.

Branch kullanımı aşağıdaki durumlarda yaygın olarak tercih edilir:

* Yeni özellik geliştirme
* Yazılım hatalarının giderilmesi
* Deneysel çalışmalar yapılması
* Sürüm hazırlıkları
* Bakım ve güncelleme işlemleri

### Branch Çalışma Mantığı

Bir branch oluşturulduğunda mevcut proje durumu yeni branch'e kopyalanır. Bundan sonra yapılan tüm değişiklikler yalnızca ilgili branch üzerinde uygulanır. Ana branch veya diğer branch'ler bu değişikliklerden etkilenmez.

Geliştirme tamamlandıktan sonra branch, gerekli kontroller yapıldıktan sonra ana branch ile birleştirilir (merge). Böylece yapılan çalışmalar projenin ana geliştirme sürecine dahil edilmiş olur.

Aşağıdaki şema, branch yapısının temel çalışma mantığını göstermektedir.

```
main
 │
 ├───────────────►
 │
 └────► feature-login
         │
         ├────────►
         │
         └────► Merge
                 │
                 ▼
               main
```

### Branch Kullanmanın Avantajları

Branch yapısı yazılım geliştirme sürecine birçok avantaj sağlar.

* Ana kod tabanı korunur.
* Birden fazla geliştirici aynı anda çalışabilir.
* Yeni özellikler bağımsız olarak geliştirilebilir.
* Hatalı değişikliklerin projeyi etkileme riski azalır.
* Kod inceleme ve test süreçleri daha düzenli yürütülebilir.
* Geliştirme süreci daha planlı ve yönetilebilir hâle gelir.

### Dikkat Edilmesi Gerekenler

Branch'ler anlamlı isimlerle oluşturulmalıdır. Aynı branch üzerinde uzun süre çalışılması, ilerleyen süreçte birleştirme işlemlerini zorlaştırabilir. Bu nedenle tamamlanan çalışmalar mümkün olduğunca kısa sürede ana branch ile birleştirilmeli ve kullanılmayan branch'ler temizlenmelidir.

Branch mantığının doğru anlaşılması, Git'in etkin kullanılabilmesi açısından büyük önem taşır. Özellikle ekip çalışmalarında düzenli branch yönetimi, kod kalitesinin korunmasına ve geliştirme süreçlerinin daha verimli ilerlemesine katkı sağlar.
