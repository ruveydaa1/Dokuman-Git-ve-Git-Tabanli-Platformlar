# GitHub Security

GitHub Security, yazılım projelerinin güvenliğini artırmak, güvenlik açıklarını tespit etmek ve geliştiricilere güvenli geliştirme süreçleri sunmak amacıyla kullanılan GitHub güvenlik özellikleri bütünüdür.

Yazılım geliştirme süreçlerinde yalnızca kodun çalışması değil, aynı zamanda güvenli olması da önemlidir. GitHub, geliştiricilerin kodlarını analiz etmelerine, bağımlılıklarını takip etmelerine, hassas bilgileri korumalarına ve güvenlik problemlerini erken aşamada tespit etmelerine yardımcı olan çeşitli araçlar sunar.

***

## GitHub Security Özellikleri

GitHub, proje güvenliğini sağlamak için farklı güvenlik araçları ve yapılandırma seçenekleri sunar.

Temel güvenlik özellikleri:

* Code Scanning
* Secret Scanning
* Dependabot
* Security Advisories
* Dependency Review
* Branch Protection Rules

***

## Code Scanning

Code Scanning, repository içerisindeki kaynak kodları analiz ederek güvenlik açıklarını tespit etmeye yardımcı olan bir güvenlik aracıdır.

Statik analiz yöntemi kullanılarak kod içerisindeki olası güvenlik problemleri bulunabilir.

Tespit edilebilecek bazı sorunlar:

* Güvensiz kod kullanımı
* Kod açıkları
* Riskli fonksiyon kullanımları
* Yaygın güvenlik hataları

Code Scanning sonuçları GitHub üzerinde görüntülenebilir ve geliştiricilere düzeltme önerileri sunulabilir.

***

## Secret Scanning

Secret Scanning, repository içerisinde yanlışlıkla paylaşılmış hassas bilgileri tespit etmek için kullanılır.

Örnek hassas bilgiler:

* API anahtarları
* Erişim token'ları
* Şifreler
* Özel anahtarlar

Bir secret tespit edildiğinde GitHub geliştiriciyi uyarabilir ve gerekli önlemlerin alınmasını sağlar.

Özellikle açık kaynak projelerde hassas bilgilerin yanlışlıkla paylaşılmasını önlemek açısından önemli bir güvenlik özelliğidir.

***

## Dependabot

Dependabot, projelerde kullanılan bağımlılıkları takip eden ve güvenlik açıklarına karşı uyarılar oluşturan GitHub aracıdır.

Bağımlılıklar zaman içerisinde eskiyebilir veya güvenlik açıkları içerebilir. Dependabot bu durumları analiz ederek geliştiricilere bilgi verir.

Dependabot ile:

* Eski paket sürümleri tespit edilebilir.
* Güvenlik açıkları görüntülenebilir.
* Otomatik güncelleme Pull Request'leri oluşturulabilir.

***

## Dependency Review

Dependency Review, bir Pull Request içerisinde değiştirilen bağımlılıkların güvenlik durumunu kontrol eder.

Bu özellik sayesinde yeni eklenen veya güncellenen paketlerin projeye risk oluşturup oluşturmadığı incelenebilir.

Kontrol edilen noktalar:

* Güvenlik açıkları
* Riskli paket sürümleri
* Bağımlılık değişiklikleri

***

## Security Advisories

GitHub Security Advisories, projelerde tespit edilen güvenlik açıklarının takip edilmesini sağlayan özelliktir.

Özellikle açık kaynak projelerde geliştiriciler:

* Güvenlik açığı bildirimleri oluşturabilir.
* Açığın detaylarını inceleyebilir.
* Çözüm önerileri paylaşabilir.

Bu özellik sayesinde güvenlik problemleri kontrollü şekilde yönetilebilir.

***

## Branch Protection Rules

Branch Protection Rules, önemli branch'lerin korunmasını sağlayan GitHub özelliğidir.

Genellikle:

* main
* master

gibi üretim kodlarını içeren branch'lerde kullanılır.

Koruma kuralları ile:

* Doğrudan push engellenebilir.
* Pull Request zorunlu tutulabilir.
* Code Review onayı istenebilir.
* Başarılı CI/CD kontrolleri zorunlu yapılabilir.

Bu sayede kritik branch'lere hatalı kod gönderilmesi önlenir.

***

## GitHub Security Best Practices

GitHub projelerinde güvenliği artırmak için aşağıdaki uygulamalar önerilir:

* Hassas bilgiler repository içerisinde tutulmamalıdır.
* `.env` gibi dosyalar `.gitignore` içerisine eklenmelidir.
* Güçlü erişim izinleri kullanılmalıdır.
* Branch koruma kuralları uygulanmalıdır.
* Bağımlılıklar düzenli olarak güncellenmelidir.
* Güvenlik taramaları aktif edilmelidir.
* Pull Request süreçleri kullanılmalıdır.

***

## GitHub Security'nin Önemi

GitHub Security özellikleri, yazılım geliştirme sürecinin güvenlik odaklı ilerlemesini sağlar. Güvenlik açıklarının erken tespit edilmesi, hassas bilgilerin korunması ve bağımlılıkların kontrol altında tutulması sayesinde daha güvenilir yazılımlar geliştirilebilir.

Modern yazılım geliştirme süreçlerinde güvenlik, geliştirme sürecinin son aşamasında değil, başlangıçtan itibaren dikkate alınması gereken önemli bir unsurdur. GitHub'ın sunduğu güvenlik araçları bu yaklaşımın uygulanmasına yardımcı olur.
