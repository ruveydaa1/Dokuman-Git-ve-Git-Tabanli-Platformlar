# GitBucket Mimarisi

GitBucket mimarisi, Git versiyon kontrol sistemi üzerine kurulmuş hafif ve modüler bir web uygulaması yapısına sahiptir. GitBucket, kullanıcıların Git repository'lerini kendi sunucuları üzerinde barındırmasına ve web arayüzü üzerinden yönetmesine olanak sağlar.

GitBucket'ın temel mimarisi; **Server**, **Repository**, **User**, **Organization**, **Database** ve **Plugin** bileşenlerinden oluşur.

Bu bileşenler birlikte çalışarak Git işlemlerinin yönetilmesini, kullanıcı yetkilendirmelerinin yapılmasını ve proje süreçlerinin takip edilmesini sağlar.

***

## GitBucket Server Yapısı

GitBucket, Java tabanlı bir web uygulaması olarak çalışır.

Sunucu üzerinde çalışan GitBucket:

* Web arayüzünü sağlar.
* Kullanıcı isteklerini yönetir.
* Repository işlemlerini gerçekleştirir.
* Git komutlarıyla iletişim kurar.
* Verileri yönetir.

Genel çalışma yapısı:

```
                Kullanıcı

                    |
                    ▼

              GitBucket Web UI

                    |
                    ▼

            GitBucket Server

          /          |          \

 Repository     Database     Plugins

```

***

## Repository Yapısı

GitBucket'ın temel bileşeni repository'lerdir.

Her repository içerisinde:

* Kaynak kod dosyaları
* Commit geçmişi
* Branch'ler
* Tag'ler
* Issue kayıtları
* Pull Request bilgileri

bulunur.

GitBucket, Git'in kendi repository yapısını kullanır ve uzak repository yönetimi sağlar.

***

## User Yönetimi

GitBucket içerisinde kullanıcı hesapları oluşturularak erişim yönetimi yapılabilir.

Kullanıcılar:

* Repository oluşturabilir.
* Projelere katkı sağlayabilir.
* Kod değişiklikleri gönderebilir.
* Pull Request oluşturabilir.

Kullanıcı yetkileri sayesinde hangi kişinin hangi işlemleri yapabileceği kontrol edilir.

***

## Organization Yapısı

GitBucket, projeleri kullanıcı grupları altında yönetmek için Organization yapısını destekler.

Organization sayesinde:

* Birden fazla proje gruplanabilir.
* Ekip üyeleri yönetilebilir.
* Ortak erişim izinleri belirlenebilir.

Örnek:

```
Organization

      |
      ├── Project A
      |
      ├── Project B
      |
      └── Project C
```

***

## Database Yapısı

GitBucket, kullanıcı bilgileri, ayarlar ve platform verilerini yönetmek için veritabanı kullanır.

Database içerisinde genellikle:

* Kullanıcı bilgileri
* Repository bilgileri
* Yetkilendirme verileri
* Issue kayıtları
* Pull Request bilgileri

saklanır.

Kaynak kodların kendisi ise Git repository yapısında tutulur.

***

## Git İşlemleri ile İlişkisi

GitBucket, Git komutlarının çalışmasını sağlayan uzak repository sunucusu olarak görev yapar.

Temel işlem akışı:

```

Developer

   |
   | git commit

   ▼

Local Repository

   |
   | git push

   ▼

GitBucket Server

   |
   | Repository Güncelleme

   ▼

Remote Repository

```

GitBucket, Git'in sunduğu:

* Commit
* Branch
* Merge
* Push
* Pull

işlemlerini destekler.

***

## Plugin Mimarisi

GitBucket, eklenti desteği sayesinde genişletilebilir bir yapıya sahiptir.

Plugin'ler ile:

* Yeni özellikler eklenebilir.
* Mevcut özellikler geliştirilebilir.
* Harici araçlarla entegrasyon sağlanabilir.

Bu yapı GitBucket'ın ihtiyaçlara göre özelleştirilebilmesine olanak sağlar.

***

## GitBucket Mimarisi Bileşenleri

| Bileşen      | Açıklama                                         |
| ------------ | ------------------------------------------------ |
| Server       | GitBucket uygulamasının çalıştığı ana yapı       |
| Repository   | Kaynak kodların ve Git geçmişinin tutulduğu alan |
| User         | Kullanıcı hesapları                              |
| Organization | Grup ve proje yönetimi                           |
| Database     | Platform bilgilerinin saklandığı alan            |
| Plugin       | Ek özellik sağlayan modüller                     |

***

## GitBucket Mimarisinin Özellikleri

GitBucket mimarisinin öne çıkan özellikleri:

* Hafif ve sade yapı
* Kolay kurulabilir mimari
* Self-hosted kullanım desteği
* Git ile tam uyumlu çalışma
* Eklenti desteği
* Düşük sistem gereksinimleri

GitBucket mimarisi, büyük DevOps platformlarının karmaşık yapılarına kıyasla daha basit bir yaklaşım sunar. Bu nedenle küçük ve orta ölçekli ekipler veya kendi Git sunucusunu oluşturmak isteyen kullanıcılar için uygun bir çözüm olarak kullanılabilir.
