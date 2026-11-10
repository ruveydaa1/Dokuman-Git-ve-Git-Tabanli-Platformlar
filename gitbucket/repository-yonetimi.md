# Repository Yönetimi

GitBucket repository yönetimi, Git projelerinin oluşturulması, saklanması, erişim izinlerinin düzenlenmesi ve ekip üyeleriyle birlikte geliştirilmesini kapsar.

GitBucket üzerinde her proje bir repository içerisinde yönetilir. Repository içerisinde kaynak kod dosyaları, commit geçmişi, branch'ler ve proje ile ilgili diğer Git verileri bulunur.

GitBucket, Git'in temel repository yapısını kullanarak geliştiricilere merkezi bir kod yönetim ortamı sağlar.

***

## Repository Oluşturma

GitBucket üzerinde yeni bir repository oluşturularak yeni bir proje başlatılabilir.

Repository oluşturulurken aşağıdaki bilgiler belirlenir:

* Repository adı
* Açıklama
* Görünürlük ayarı
* README dosyası
* Başlangıç dosyaları

Oluşturulan repository, Git işlemleri için uzak depo olarak kullanılabilir.

***

## Repository Görünürlüğü

GitBucket repository'lerinde erişim seviyeleri belirlenebilir.

Temel görünürlük seçenekleri:

### Public Repository

Herkese açık repository türüdür.

Özellikleri:

* Tüm kullanıcılar görüntüleyebilir.
* Açık kaynak projelerde kullanılabilir.
* Katkı süreçlerine izin verir.

***

### Private Repository

Sadece yetkilendirilmiş kullanıcıların erişebildiği repository türüdür.

Kullanım alanları:

* Özel projeler
* Kurum içi yazılımlar
* Ekip çalışmaları

***

## Repository Klonlama (Clone)

GitBucket üzerinde bulunan bir repository'nin yerel bilgisayara kopyalanması işlemidir.

Clone işlemi ile geliştiriciler projeyi kendi ortamlarına alarak geliştirme yapabilir.

Örnek:

```bash
git clone <repository-url>
```

Clone işlemi sonrasında:

* Proje dosyaları,
* Commit geçmişi,
* Branch bilgileri

yerel ortama aktarılır.

***

## Fork

Fork, başka bir repository'nin kullanıcı hesabına kopyalanması işlemidir.

Özellikle açık kaynak projelerde kullanılır.

Fork ile:

* Orijinal projeden bağımsız geliştirme yapılabilir.
* Yapılan değişiklikler korunabilir.
* Pull Request ile ana projeye katkı gönderilebilir.

Fork akışı:

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

## Kullanıcı ve Yetki Yönetimi

GitBucket üzerinde repository erişimleri kullanıcı bazında yönetilebilir.

Kullanıcılara farklı yetkiler verilerek hangi işlemleri yapabilecekleri belirlenir.

Yetki kapsamında:

* Repository görüntüleme
* Kod değişikliği yapma
* Push işlemi gerçekleştirme
* Yönetim işlemleri

kontrol edilebilir.

***

## Branch Yönetimi

GitBucket, Git branch yapısını destekler.

Branch'ler farklı geliştirme süreçlerini birbirinden ayırmak için kullanılır.

Örnek:

```
main

 ├── feature-login

 ├── feature-search

 └── bugfix-error
```

Geliştiriciler kendi branch'lerinde çalışarak tamamlanan değişiklikleri ana branch'e aktarabilir.

***

## Pull Request Yönetimi

GitBucket, geliştiricilerin yaptıkları değişiklikleri inceleme ve birleştirme sürecini Pull Request üzerinden yönetmesini sağlar.

Pull Request süreci:

1. Yeni branch oluşturulur.
2. Kod geliştirmesi yapılır.
3. Değişiklikler commit edilir.
4. Repository'ye gönderilir.
5. Pull Request oluşturulur.
6. İnceleme sonrası merge işlemi yapılır.

Bu yapı ekip çalışmalarında kod kalitesinin korunmasına yardımcı olur.

***

## Repository Ayarları

GitBucket repository'lerinde çeşitli ayarlar yönetilebilir.

Yapılabilecek işlemler:

* Repository adını değiştirme
* Açıklama güncelleme
* Kullanıcı izinlerini düzenleme
* Repository silme
* Varsayılan branch belirleme

***

## GitBucket Repository Yönetimi İçin Öneriler

Düzenli bir repository yapısı için:

* Açıklayıcı repository isimleri kullanılmalıdır.
* Commit mesajları anlaşılır olmalıdır.
* Branch yapısı belirlenmelidir.
* Yetkilendirmeler dikkatli yapılmalıdır.
* README dosyası eklenmelidir.
* Gereksiz dosyalar `.gitignore` ile hariç tutulmalıdır.

GitBucket repository yönetimi, Git'in temel özelliklerini web tabanlı bir ortam üzerinden kullanmayı sağlar. Basit ve hafif yapısı sayesinde küçük ve orta ölçekli ekiplerin kaynak kodlarını düzenli şekilde yönetmesine yardımcı olur.
