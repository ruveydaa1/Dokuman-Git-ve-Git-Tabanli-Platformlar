# GitLab Güvenlik Özellikleri

GitLab Güvenlik Özellikleri, yazılım geliştirme süreçlerinde güvenliğin geliştirme aşamasından itibaren dahil edilmesini sağlayan DevSecOps yaklaşımının bir parçasıdır.

GitLab, yalnızca kod yönetimi ve CI/CD süreçleri sunmakla kalmaz; uygulama güvenliği, bağımlılık güvenliği, gizli bilgi tespiti ve konteyner güvenliği gibi alanlarda da çeşitli analiz araçları sağlar.

Bu güvenlik özellikleri sayesinde güvenlik açıkları erken aşamada tespit edilerek geliştirme süreçleri daha güvenli hâle getirilebilir.

***

## GitLab Security Dashboard

Security Dashboard, projelerde gerçekleştirilen güvenlik analizlerinin sonuçlarının merkezi olarak görüntülendiği alandır.

Bu panel üzerinden:

* Tespit edilen güvenlik açıkları
* Açıkların önem seviyeleri
* Güvenlik taraması sonuçları
* Çözüm önerileri

takip edilebilir.

Security Dashboard, ekiplerin güvenlik durumunu genel olarak değerlendirmesine yardımcı olur.

***

## SAST (Static Application Security Testing)

SAST, uygulama kaynak kodlarını çalıştırmadan analiz ederek güvenlik açıklarını tespit etmeye yarayan statik analiz yöntemidir.

GitLab SAST özelliği sayesinde kod içerisindeki potansiyel güvenlik problemleri bulunabilir.

Tespit edilebilecek sorunlar:

* Güvensiz kod kullanımı
* Kodlama hataları
* Riskli fonksiyonlar
* Güvenlik açıkları

SAST analizleri CI/CD pipeline içerisine dahil edilerek her kod değişikliğinde otomatik çalıştırılabilir.

***

## DAST (Dynamic Application Security Testing)

DAST, çalışan uygulamaları dışarıdan analiz ederek güvenlik açıklarını tespit etmeye yönelik dinamik analiz yöntemidir.

DAST ile:

* Web uygulaması açıkları
* Güvenlik yanlış yapılandırmaları
* Çalışma zamanı problemleri

tespit edilmeye çalışılır.

SAST kaynak kodu analiz ederken, DAST çalışan uygulamanın davranışlarını inceler.

***

## Dependency Scanning

Dependency Scanning, projelerde kullanılan üçüncü parti kütüphaneleri ve bağımlılıkları analiz eder.

Modern uygulamalar birçok harici paket kullandığı için bu bağımlılıklarda güvenlik açıkları bulunabilir.

Bu özellik ile:

* Güvenlik açığı bulunan paketler tespit edilir.
* Riskli bağımlılıklar görüntülenir.
* Güncelleme önerileri alınabilir.

***

## Secret Detection

Secret Detection, repository içerisinde yanlışlıkla paylaşılmış hassas bilgileri tespit etmek için kullanılır.

Tespit edilebilecek bilgiler:

* API anahtarları
* Erişim token'ları
* Şifreler
* Özel anahtarlar

Geliştiricilerin hassas bilgileri kaynak kod içerisinde paylaşmasını engelleyerek veri güvenliğini artırır.

***

## Container Scanning

Container Scanning, Docker image'larında bulunan güvenlik açıklarını tespit etmek için kullanılır.

Konteyner tabanlı uygulamalarda kullanılan image'lar içerisinde güvenlik riski oluşturabilecek paketler bulunabilir.

Bu özellik sayesinde:

* Image güvenlik açıkları bulunabilir.
* Riskli paketler tespit edilebilir.
* Güvenli container kullanımı sağlanabilir.

Örnek akış:

```

Source Code

    ↓

Docker Image Oluşturma

    ↓

Container Scanning

    ↓

Deployment

```

***

## License Compliance

License Compliance, projede kullanılan açık kaynak bağımlılıkların lisans durumlarını kontrol etmek için kullanılır.

Bu özellik sayesinde:

* Kullanılan paketlerin lisansları incelenebilir.
* Uygunsuz lisans kullanımları tespit edilebilir.
* Yasal uyumluluk süreçleri desteklenebilir.

***

## Vulnerability Management

GitLab Vulnerability Management, tespit edilen güvenlik açıklarının takip edilmesini sağlar.

Bu süreçte:

* Güvenlik açıkları listelenebilir.
* Önceliklendirme yapılabilir.
* Sorumlu kişiler atanabilir.
* Çözüm süreçleri takip edilebilir.

***

## Security Scan'lerin CI/CD ile Kullanımı

GitLab güvenlik analizleri CI/CD pipeline içerisine dahil edilebilir.

Örnek süreç:

```

Code Commit

      ↓

Pipeline Başlatılır

      ↓

SAST Analizi

      ↓

Dependency Scan

      ↓

Container Scan

      ↓

Deployment

```

Bu yapı sayesinde güvenlik kontrolleri otomatikleştirilir.

***

## GitLab Güvenlik Özelliklerinin Özeti

<table data-search="false"><thead><tr><th>Özellik</th><th>Açıklama</th></tr></thead><tbody><tr><td>Security Dashboard</td><td>Güvenlik sonuçlarını görüntüleme</td></tr><tr><td>SAST</td><td>Kaynak kod güvenlik analizi</td></tr><tr><td>DAST</td><td>Çalışan uygulama analizi</td></tr><tr><td>Dependency Scanning</td><td>Bağımlılık güvenliği</td></tr><tr><td>Secret Detection</td><td>Hassas bilgi tespiti</td></tr><tr><td>Container Scanning</td><td>Container güvenliği</td></tr><tr><td>License Compliance</td><td>Lisans kontrolü</td></tr><tr><td>Vulnerability Management</td><td>Güvenlik açıklarının yönetimi</td></tr></tbody></table>

***

## GitLab Security'nin Önemi

GitLab güvenlik özellikleri, güvenliği yazılım geliştirme sürecinin son aşamasında değil, geliştirme sürecinin tamamında ele almayı sağlar.

DevSecOps yaklaşımı ile güvenlik kontrollerinin CI/CD süreçlerine dahil edilmesi, güvenlik açıklarının erken tespit edilmesine ve daha güvenilir yazılımlar geliştirilmesine yardımcı olur.

GitLab'ın geliştirme, otomasyon ve güvenlik süreçlerini tek platformda birleştirmesi, özellikle kurumsal yazılım geliştirme ekipleri için güçlü bir çözüm sunmasını sağlar.
