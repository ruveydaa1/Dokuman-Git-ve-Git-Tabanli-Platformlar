# Merge Request

Merge Request (MR), bir geliştiricinin kendi branch'inde yaptığı değişikliklerin başka bir branch ile birleştirilmesi için oluşturduğu istektir. Merge Request süreci, değişikliklerin ana branch'e aktarılmadan önce incelenmesini, değerlendirilmesini ve gerekli kontrollerden geçirilmesini sağlar.

Merge Request kavramı özellikle GitLab tarafından kullanılan bir terimdir. GitHub ve bazı diğer Git tabanlı platformlarda aynı süreç için genellikle **Pull Request** ifadesi kullanılır.

Her iki kavramın temel amacı aynıdır: Yapılan kod değişikliklerini kontrollü bir şekilde incelemek ve uygun görüldüğünde hedef branch ile birleştirmek.

***

### Merge Request Süreci

Genel bir Merge Request süreci aşağıdaki adımlardan oluşur:

1. Geliştirici yeni bir branch oluşturur.
2. Geliştirme işlemlerini kendi branch'i üzerinde gerçekleştirir.
3. Değişiklikleri commit eder.
4. Branch'i uzak repository'ye gönderir.
5. Merge Request oluşturur.
6. Ekip üyeleri değişiklikleri inceler.
7. Kod incelemesi ve gerekli kontroller tamamlanır.
8. Merge işlemi gerçekleştirilerek değişiklikler hedef branch'e aktarılır.

***

### Merge Request İçeriği

Bir Merge Request içerisinde genellikle aşağıdaki bilgiler bulunur:

#### Başlık

Yapılan değişikliği açıklayan kısa ve anlaşılır başlıktır.

Örnek:

```
Arama özelliği geliştirildi
```

***

#### Açıklama

Yapılan değişikliklerin neden yapıldığını ve hangi işlemleri içerdiğini açıklayan bölümdür.

Açıklama içerisinde aşağıdaki bilgiler yer alabilir:

* Yapılan geliştirmeler
* Düzeltilen hatalar
* Test sonuçları
* Ek açıklamalar

***

#### Değişiklik Karşılaştırması (Diff)

Merge Request içerisinde kaynak branch ile hedef branch arasındaki farklar görüntülenir.

Bu bölüm sayesinde:

* Eklenen satırlar,
* Silinen satırlar,
* Güncellenen dosyalar

incelenebilir.

***

### Merge Request Avantajları

Merge Request kullanımı aşağıdaki avantajları sağlar:

* Kod değişiklikleri kontrol altında tutulur.
* Ana branch korunur.
* Ekip üyeleri değişiklikleri inceleyebilir.
* Kod kalitesi artırılır.
* Hatalar erken aşamada fark edilir.
* Geliştirme süreci daha şeffaf hâle gelir.

***

### Pull Request ve Merge Request Farkı

Pull Request ve Merge Request arasında temel olarak işlevsel bir fark bulunmamaktadır. İki kavram da bir branch'teki değişikliklerin başka bir branch'e aktarılması için kullanılan inceleme ve onay sürecini ifade eder.

| Özellik                  | Pull Request                             | Merge Request                            |
| ------------------------ | ---------------------------------------- | ---------------------------------------- |
| Kullanıldığı platformlar | GitHub, Bitbucket                        | GitLab                                   |
| Temel amacı              | Değişiklikleri incelemek ve birleştirmek | Değişiklikleri incelemek ve birleştirmek |
| Kod inceleme             | Desteklenir                              | Desteklenir                              |
| Otomatik kontroller      | Desteklenir                              | Desteklenir                              |

***

### Merge Request Kullanımında Dikkat Edilmesi Gerekenler

* Merge Request küçük ve anlaşılır değişiklikler içermelidir.
* Açıklama bölümü detaylı hazırlanmalıdır.
* Kod inceleme sürecine önem verilmelidir.
* Birleştirme öncesinde testler tamamlanmalıdır.
* Gerekli onaylar alınmadan ana branch'e aktarım yapılmamalıdır.

Merge Request, özellikle GitLab tabanlı ekip çalışmalarında kullanılan önemli bir geliştirme sürecidir. Düzenli kullanıldığında ekip içi iletişimi güçlendirir, kod kalitesini artırır ve daha güvenli bir yazılım geliştirme ortamı oluşturur.
