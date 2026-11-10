# Pull Request

Pull Request (PR), bir geliştiricinin kendi branch'inde yaptığı değişiklikleri başka bir branch'e dahil etmek için oluşturduğu istektir. Pull Request süreci sayesinde yapılan kod değişiklikleri doğrudan ana branch'e aktarılmadan önce ekip üyeleri tarafından incelenebilir, değerlendirilebilir ve gerekli kontrollerden geçirilebilir.

Pull Request, özellikle ekip çalışmalarında kod kalitesini artırmak ve hatalı değişikliklerin ana kod tabanına ulaşmasını önlemek amacıyla kullanılır.

***

### Pull Request Süreci

Genel olarak bir Pull Request süreci aşağıdaki adımlardan oluşur:

1. Geliştirici yeni bir branch oluşturur.
2. Geliştirme işlemlerini kendi branch'i üzerinde gerçekleştirir.
3. Değişikliklerini commit eder.
4. Branch'i uzak repository'ye gönderir.
5. Pull Request oluşturur.
6. Ekip üyeleri kod değişikliklerini inceler.
7. Gerekli düzenlemeler yapıldıktan sonra Pull Request onaylanır.
8. Değişiklikler hedef branch ile birleştirilir.

***

### Pull Request İçeriği

Bir Pull Request genellikle aşağıdaki bilgileri içerir:

#### Başlık

Yapılan değişikliği kısa ve anlaşılır şekilde açıklayan başlıktır.

Örnek:

```
Kullanıcı giriş doğrulaması eklendi
```

***

#### Açıklama

Pull Request içerisinde yapılan değişikliklerin detaylı olarak açıklandığı bölümdür.

Açıklamada genellikle şu bilgiler bulunur:

* Yapılan değişiklikler
* Çözülmüş problemler
* Test bilgileri
* Dikkat edilmesi gereken noktalar

***

#### Değişiklikler (Changes)

Pull Request üzerinde hangi dosyaların değiştirildiği ve hangi satırlarda güncelleme yapıldığı görüntülenebilir.

Bu bölüm, kod inceleme sürecinin temelini oluşturur.

***

### Pull Request'in Avantajları

Pull Request kullanımı birçok avantaj sağlar:

* Kod değişiklikleri ana branch'e aktarılmadan önce incelenir.
* Ekip üyeleri arasında bilgi paylaşımı sağlanır.
* Hataların erken tespit edilmesine yardımcı olur.
* Kod kalitesinin korunmasını sağlar.
* Proje geçmişinin daha düzenli tutulmasına katkıda bulunur.

***

### Pull Request ve Merge İlişkisi

Pull Request oluşturmak, değişikliklerin otomatik olarak birleştirildiği anlamına gelmez.

Pull Request yalnızca birleştirme isteğidir. Birleştirme işlemi gerçekleştirilmeden önce:

* Kod incelemesi yapılabilir.
* Otomatik testler çalıştırılabilir.
* Gerekli onaylar alınabilir.

Tüm kontroller tamamlandıktan sonra Pull Request kabul edilerek ilgili branch'ler birleştirilir.

***

### Pull Request Kullanımında Dikkat Edilmesi Gerekenler

* Pull Request'ler küçük ve anlaşılır değişiklikler içermelidir.
* Açıklama bölümü detaylı hazırlanmalıdır.
* Gereksiz dosya değişikliklerinden kaçınılmalıdır.
* Kod incelemesi sırasında yapıcı geri bildirim verilmelidir.
* Birleştirme öncesinde test süreçleri tamamlanmalıdır.

Pull Request, modern yazılım geliştirme süreçlerinde ekip çalışmasının temel parçalarından biridir. Geliştiriciler arasında kontrollü bir iş akışı oluşturarak kod kalitesinin artırılmasını ve daha güvenli bir geliştirme süreci yürütülmesini sağlar.
