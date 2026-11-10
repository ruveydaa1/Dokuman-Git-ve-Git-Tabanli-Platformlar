# Repository Yönetimi

Repository (Depo), bir yazılım projesine ait kaynak kodların, dosyaların, commit geçmişinin ve proje ile ilgili diğer bilgilerin saklandığı alandır. GitHub üzerinde her proje bir repository içerisinde yönetilir.

Repository yönetimi; yeni bir repository oluşturma, mevcut repository'leri düzenleme, erişim izinlerini belirleme ve proje dosyalarını yönetme işlemlerini kapsar. Düzenli bir repository yapısı oluşturmak, proje geliştirme süreçlerinin daha kolay takip edilmesini sağlar.

***

### Repository Oluşturma

GitHub üzerinde yeni bir repository oluşturularak sıfırdan bir proje başlatılabilir veya mevcut bir proje GitHub'a aktarılabilir.

Repository oluşturulurken aşağıdaki bilgiler belirlenir:

* Repository adı
* Açıklama
* Görünürlük ayarı
* README dosyası
* `.gitignore` dosyası
* Lisans seçimi

***

### Repository Görünürlüğü

GitHub repository'leri farklı erişim seviyelerine sahip olabilir.

#### Public Repository

Herkese açık repository türüdür.

Özellikleri:

* Her kullanıcı repository'yi görüntüleyebilir.
* Açık kaynak projeler için uygundur.
* Diğer geliştiriciler projeye katkıda bulunabilir.

***

#### Private Repository

Sadece izin verilen kullanıcıların erişebildiği repository türüdür.

Özellikleri:

* Proje kodları gizli tutulur.
* Ekip içi projelerde tercih edilir.
* Erişim yetkileri geliştirici bazında yönetilebilir.

***

### Repository Klonlama (Clone)

Bir repository'nin yerel bilgisayara kopyalanması işlemidir.

Clone işlemi sayesinde geliştiriciler GitHub üzerindeki projeyi kendi ortamlarında geliştirebilir.

Örnek:

```bash
git clone <repository-url>
```

Clone işlemi sonrasında proje dosyaları ve Git geçmişi yerel ortama aktarılır.

***

### Fork

Fork, başka bir kullanıcının repository'sinin kendi hesabına kopyalanması işlemidir.

Genellikle açık kaynak projelerde kullanılır.

Fork sayesinde:

* Orijinal projeye zarar vermeden geliştirme yapılabilir.
* Kendi repository'niz üzerinde değişiklik yapabilirsiniz.
* Değişiklikler Pull Request ile ana projeye gönderilebilir.

Fork süreci:

```
Orijinal Repository
          |
          | Fork
          ▼
Kullanıcı Repository'si
          |
          | Pull Request
          ▼
Orijinal Repository
```

***

### Collaborator Yönetimi

Repository sahibi, projeye erişebilecek kullanıcıları belirleyebilir.

Collaborator izinleri sayesinde:

* Kullanıcı ekleme
* Yetki belirleme
* Erişim kaldırma

işlemleri gerçekleştirilebilir.

Yaygın izin seviyeleri:

| Yetki    | Açıklama               |
| -------- | ---------------------- |
| Read     | Repository görüntüleme |
| Write    | Değişiklik yapabilme   |
| Maintain | Repository yönetimi    |
| Admin    | Tam yönetim yetkisi    |

***

### Repository Ayarları

GitHub repository'lerinde çeşitli ayarlar yapılandırılabilir:

#### Genel Ayarlar

* Repository adı değiştirme
* Açıklama düzenleme
* Görünürlük değiştirme
* Repository silme

#### Branch Ayarları

* Varsayılan branch belirleme
* Branch koruma kuralları oluşturma
* Merge izinlerini düzenleme

#### Güvenlik Ayarları

* Güvenlik analizlerini etkinleştirme
* Bağımlılık kontrollerini yönetme
* Hassas bilgi taramalarını kullanma

***

### README, .gitignore ve Lisans Ekleme

Repository oluşturulurken veya sonrasında aşağıdaki dosyalar eklenebilir:

#### README.md

Proje hakkında bilgi vermek için kullanılır.

#### .gitignore

Git tarafından takip edilmemesi gereken dosyaları belirler.

#### LICENSE

Projenin kullanım ve dağıtım koşullarını belirler.

***

### İyi Bir Repository Yapısı İçin Öneriler

Düzenli bir repository oluşturmak için:

* Açıklayıcı repository isimleri kullanılmalıdır.
* README dosyası hazırlanmalıdır.
* Gereksiz dosyalar `.gitignore` ile hariç tutulmalıdır.
* Branch yapısı belirlenmelidir.
* Commit mesajları düzenli tutulmalıdır.
* Erişim izinleri dikkatli yönetilmelidir.

Repository yönetimi, GitHub üzerinde sürdürülebilir ve düzenli projeler oluşturmanın temel adımlarından biridir. Doğru yapılandırılmış bir repository, hem bireysel geliştiriciler hem de ekipler için daha verimli bir geliştirme süreci sağlar.
