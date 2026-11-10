# Repository Yönetimi

GitLab repository yönetimi, projelere ait kaynak kodların saklanması, geliştirme süreçlerinin düzenlenmesi ve ekip üyelerinin erişimlerinin kontrol edilmesini kapsar.

GitLab içerisinde repository yapısı doğrudan bir **Project** altında bulunur. Her project; kaynak kodları, commit geçmişini, branch'leri, Merge Request'leri, CI/CD yapılandırmalarını ve proje ayarlarını içerir.

Düzenli bir repository yönetimi, ekip çalışmalarının daha kontrollü ilerlemesini ve proje yaşam döngüsünün daha kolay takip edilmesini sağlar.

***

## GitLab Project Oluşturma

GitLab'da yeni bir proje oluşturularak yeni bir repository başlatılabilir.

Project oluşturulurken aşağıdaki bilgiler belirlenir:

* Proje adı
* Proje açıklaması
* Namespace (kullanıcı veya grup)
* Görünürlük seviyesi
* README dosyası
* Repository başlangıç ayarları

Oluşturulan project içerisinde Git repository otomatik olarak hazırlanır.

***

## Repository Görünürlüğü (Visibility)

GitLab projelerinde erişim seviyeleri visibility ayarları ile belirlenir.

Üç temel görünürlük seviyesi bulunur:

### Private

Sadece yetkilendirilmiş kullanıcıların erişebildiği proje türüdür.

Kullanım alanları:

* Kurumsal projeler
* Özel yazılım projeleri
* Ekip içi çalışmalar

***

### Internal

Aynı GitLab instance içerisinde bulunan kullanıcıların erişebildiği proje türüdür.

Genellikle kurum içi paylaşımlar için kullanılır.

***

### Public

Herkese açık proje türüdür.

Açık kaynak projelerde tercih edilir.

***

## Repository Klonlama (Clone)

GitLab üzerinde bulunan bir projenin yerel bilgisayara alınması işlemidir.

Clone işlemi sayesinde geliştiriciler proje üzerinde kendi ortamlarında çalışabilir.

Örnek:

```bash
git clone <repository-url>
```

Clone işleminden sonra proje dosyaları ve Git geçmişi yerel ortama aktarılır.

***

## Fork

Fork, başka bir kullanıcının veya grubun projesinin kendi hesabına kopyalanması işlemidir.

Fork özellikle açık kaynak projelerde kullanılır.

Fork sayesinde:

* Orijinal projeden bağımsız geliştirme yapılabilir.
* Yapılan değişiklikler korunabilir.
* Merge Request ile ana projeye katkı gönderilebilir.

Fork akışı:

```
Orijinal Project

        |
        | Fork

        ▼

Kullanıcı Project'i

        |
        | Merge Request

        ▼

Orijinal Project
```

***

## Member ve Yetki Yönetimi

GitLab'da projelere erişim kullanıcı bazında yönetilir.

Project sahipleri kullanıcılara farklı roller verebilir.

Temel GitLab rolleri:

| Rol        | Açıklama                      |
| ---------- | ----------------------------- |
| Guest      | Sınırlı erişim                |
| Reporter   | Proje bilgilerini görüntüleme |
| Developer  | Kod üzerinde geliştirme yapma |
| Maintainer | Proje yönetimi                |
| Owner      | Grup seviyesinde tam yetki    |

Bu roller sayesinde ekip üyelerinin hangi işlemleri gerçekleştirebileceği kontrol edilir.

***

## Branch Yönetimi

GitLab projelerinde branch'ler farklı geliştirme süreçlerini yönetmek için kullanılır.

Branch yönetimi ile:

* Yeni özellik geliştirme
* Hata düzeltme
* Sürüm hazırlama

işlemleri birbirinden ayrılabilir.

Örnek:

```
main

 ├── feature-login

 ├── feature-profile

 └── bugfix-error
```

***

## Protected Branch

Protected Branch özelliği, kritik branch'leri korumak için kullanılır.

Genellikle:

* main
* master
* production

branch'lerinde kullanılır.

Koruma kuralları ile:

* Doğrudan push engellenebilir.
* Merge yetkileri sınırlandırılabilir.
* Onay süreçleri zorunlu tutulabilir.

Bu sayede önemli branch'lere kontrolsüz değişiklik yapılması engellenir.

***

## Repository Ayarları

GitLab projelerinde çeşitli repository ayarları yapılandırılabilir.

### Genel Ayarlar

* Proje adı değiştirme
* Açıklama güncelleme
* Visibility değiştirme
* Arşivleme işlemleri

### Repository Ayarları

* Varsayılan branch belirleme
* Protected branch kuralları
* Merge ayarları
* Commit kuralları

### Entegrasyon Ayarları

* CI/CD bağlantıları
* Webhook ayarları
* Harici araç entegrasyonları

***

## İyi Bir GitLab Repository Yapısı İçin Öneriler

Düzenli bir GitLab repository yönetimi için:

* Anlamlı proje isimleri kullanılmalıdır.
* Branch stratejisi belirlenmelidir.
* Yetkiler dikkatli yönetilmelidir.
* README dosyası hazırlanmalıdır.
* Gereksiz dosyalar `.gitignore` ile hariç tutulmalıdır.
* Merge Request süreçleri kullanılmalıdır.
* Protected Branch kuralları uygulanmalıdır.

GitLab repository yönetimi, yalnızca kod saklama işlemi değil; aynı zamanda ekip çalışması, yetkilendirme ve geliştirme süreçlerinin kontrollü şekilde yürütülmesini sağlayan kapsamlı bir yönetim sürecidir.
