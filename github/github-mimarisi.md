# GitHub Mimarisi

GitHub mimarisi, Git versiyon kontrol sisteminin sunduğu yapılar üzerine kuruludur. GitHub, geliştiricilerin yerel ortamda oluşturdukları repository'leri uzak sunucular üzerinde saklamasına, değişiklikleri takip etmesine ve ekip çalışması süreçlerini yönetmesine olanak sağlar.

GitHub'ın temel çalışma mantığı; **Local Repository**, **Remote Repository**, **Branch**, **Commit**, **Pull Request** ve **Merge** kavramları üzerine kuruludur. Bu bileşenler birlikte çalışarak yazılım geliştirme sürecinin düzenli ve kontrollü şekilde yürütülmesini sağlar.

***

### Local Repository ve Remote Repository

GitHub kullanımında iki temel repository yapısı bulunur:

#### Local Repository

Geliştiricinin kendi bilgisayarında bulunan proje deposudur. Git komutları kullanılarak dosya değişiklikleri takip edilir, commit işlemleri gerçekleştirilir ve branch yönetimi yapılır.

#### Remote Repository

GitHub sunucuları üzerinde bulunan ve ekip üyeleriyle paylaşılan uzak depodur. Local repository'deki değişiklikler push işlemi ile remote repository'ye gönderilir, diğer geliştiricilerin yaptığı değişiklikler ise pull işlemi ile alınır.

Genel çalışma akışı:

```
Local Repository
        |
        | git push
        ▼
Remote Repository (GitHub)

Remote Repository
        |
        | git pull
        ▼
Local Repository
```

***

### Repository Yapısı

GitHub üzerindeki her proje bir repository içerisinde bulunur. Bir repository aşağıdaki bileşenleri içerir:

#### Dosyalar

Kaynak kodlar, dokümantasyon dosyaları ve proje için gerekli diğer dosyalar repository içerisinde saklanır.

#### Commit Geçmişi

Projede yapılan tüm değişiklikler commit olarak kayıt altına alınır. Bu sayede geçmiş sürümler takip edilebilir.

#### Branch'ler

Farklı geliştirme süreçlerini birbirinden ayırmak için kullanılır. Yeni özellikler veya hata düzeltmeleri genellikle ayrı branch'ler üzerinde gerçekleştirilir.

#### Issues

Projede karşılaşılan hataları, geliştirme önerilerini veya görevleri takip etmek için kullanılır.

#### Pull Request'ler

Bir branch'te yapılan değişikliklerin başka bir branch ile birleştirilmeden önce incelenmesini sağlar.

***

### GitHub Branch Yapısı

GitHub projelerinde genellikle aşağıdaki branch yapıları kullanılır:

```
main
 |
 ├── feature-login
 |
 ├── feature-payment
 |
 └── bugfix-error
```

Geliştiriciler kendi branch'lerinde çalışır, değişikliklerini commit eder ve tamamlanan çalışmaları Pull Request aracılığıyla ana branch'e aktarır.

***

### Commit ve Version Kontrolü

GitHub, Git'in commit yapısını kullanarak proje geçmişini saklar.

Her commit:

* Yapılan değişiklikleri,
* Commit mesajını,
* Değişikliği yapan kişiyi,
* Zaman bilgisini

içerir.

Bu yapı sayesinde projede hangi değişikliğin ne zaman ve kim tarafından yapıldığı takip edilebilir.

***

### Pull Request Akışı

GitHub'da ekip çalışması genellikle Pull Request süreci üzerinden ilerler.

Temel akış:

1. Yeni bir branch oluşturulur.
2. Kod geliştirmesi yapılır.
3. Değişiklikler commit edilir.
4. Branch GitHub repository'sine gönderilir.
5. Pull Request oluşturulur.
6. Kod incelemesi yapılır.
7. Onay sonrası merge işlemi gerçekleştirilir.

***

### GitHub Mimarisi Bileşenleri

GitHub'ın temel bileşenleri şu şekilde özetlenebilir:

<table data-search="false"><thead><tr><th>Bileşen</th><th>Açıklama</th></tr></thead><tbody><tr><td>Repository</td><td>Projelerin saklandığı alan</td></tr><tr><td>Branch</td><td>Bağımsız geliştirme alanı</td></tr><tr><td>Commit</td><td>Değişiklik kaydı</td></tr><tr><td>Issue</td><td>Görev ve hata takibi</td></tr><tr><td>Pull Request</td><td>Kod değişikliği inceleme süreci</td></tr><tr><td>Actions</td><td>Otomasyon ve CI/CD işlemleri</td></tr><tr><td>Security</td><td>Kod güvenliği araçları</td></tr></tbody></table>

GitHub mimarisi, Git'in temel versiyon kontrol yapısını web tabanlı geliştirme araçlarıyla birleştirir. Bu yapı sayesinde geliştiriciler hem bireysel projelerini yönetebilir hem de büyük ekiplerle güvenli ve düzenli bir şekilde yazılım geliştirme süreçlerini sürdürebilir.
