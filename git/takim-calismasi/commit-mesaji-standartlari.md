# Commit Mesajı Standartları

Commit mesajları, yapılan değişikliklerin neden ve ne amaçla gerçekleştirildiğini açıklayan kısa açıklamalardır. Düzenli ve anlaşılır commit mesajları kullanılması, proje geçmişinin kolay takip edilmesini, yapılan değişikliklerin daha hızlı anlaşılmasını ve ekip çalışmalarının daha verimli yürütülmesini sağlar.

Bir proje üzerinde zaman içerisinde çok sayıda commit oluşturulur. Anlamsız veya düzensiz commit mesajları kullanılması durumunda geçmiş değişiklikleri anlamak zorlaşabilir. Bu nedenle ekipler genellikle belirli commit mesajı standartları kullanarak ortak bir yazım düzeni oluşturur.

***

### Commit Mesajlarının Önemi

Düzenli commit mesajları aşağıdaki avantajları sağlar:

* Yapılan değişikliklerin amacı kolayca anlaşılır.
* Proje geçmişi daha okunabilir hâle gelir.
* Hataların hangi değişiklikten kaynaklandığı daha kolay bulunur.
* Ekip üyeleri arasındaki iletişim güçlenir.
* Sürüm yönetimi daha düzenli yapılabilir.
* Otomatik araçlar ve CI/CD süreçleri daha kolay yönetilebilir.

***

### İyi Bir Commit Mesajının Özellikleri

İyi hazırlanmış bir commit mesajı:

* Kısa ve açıklayıcı olmalıdır.
* Yapılan değişikliği belirtmelidir.
* Gereksiz ayrıntılardan kaçınmalıdır.
* Emir kipiyle yazılmalıdır.
* Tek bir değişikliği ifade etmelidir.

#### Kötü Commit Mesajı Örnekleri

```
değişiklik yapıldı
```

```
fix
```

```
son hali
```

Bu tür mesajlar yapılan değişikliğin ne olduğunu açıklamadığı için proje geçmişini takip etmeyi zorlaştırır.

***

### İyi Commit Mesajı Örnekleri

```
Kullanıcı giriş doğrulaması eklendi
```

```
Hata mesajı gösterimi düzeltildi
```

```
Veritabanı bağlantı ayarları güncellendi
```

Bu mesajlar yapılan değişiklik hakkında daha fazla bilgi verir.

***

## Conventional Commits Standardı

Conventional Commits, commit mesajlarının belirli bir kurala göre yazılmasını sağlayan yaygın bir standarttır. Bu standart sayesinde commit geçmişi daha düzenli ve anlaşılır hâle gelir.

Temel format:

```
<type>: <açıklama>
```

Örnek:

```
feat: kullanıcı kayıt özelliği eklendi
```

***

### Conventional Commits Türleri

#### feat

Yeni bir özellik eklemek için kullanılır.

Örnek:

```
feat: kullanıcı profil sayfası eklendi
```

***

#### fix

Hata düzeltmeleri için kullanılır.

Örnek:

```
fix: giriş ekranındaki doğrulama hatası düzeltildi
```

***

#### docs

Dokümantasyon değişiklikleri için kullanılır.

Örnek:

```
docs: kurulum adımları güncellendi
```

***

#### style

Kodun çalışma mantığını değiştirmeyen biçimlendirme değişiklikleri için kullanılır.

Örnek:

```
style: dosya formatları düzenlendi
```

***

#### refactor

Yeni özellik veya hata düzeltmesi içermeyen kod iyileştirmeleri için kullanılır.

Örnek:

```
refactor: kullanıcı servis yapısı düzenlendi
```

***

#### test

Test ekleme veya düzenleme işlemleri için kullanılır.

Örnek:

```
test: kullanıcı servis testleri eklendi
```

***

#### chore

Bakım ve yapılandırma işlemleri için kullanılır.

Örnek:

```
chore: bağımlılık paketleri güncellendi
```

***

### Commit Mesajı Yazarken Dikkat Edilmesi Gerekenler

* Her commit tek bir amacı temsil etmelidir.
* Büyük değişiklikler küçük commit'lere bölünmelidir.
* Commit mesajları yapılan işlemi açıkça belirtmelidir.
* Kişisel veya anlamsız ifadeler kullanılmamalıdır.
* Ekip içerisinde ortak bir standart belirlenmelidir.

***

### Örnek Commit Geçmişi

```
feat: kullanıcı kayıt sistemi eklendi
fix: parola doğrulama hatası düzeltildi
docs: README dosyası güncellendi
refactor: kullanıcı servis yapısı iyileştirildi
test: giriş testleri eklendi
```

Bu şekilde oluşturulan bir commit geçmişi, projenin gelişim sürecini daha anlaşılır hâle getirir.

Commit mesajı standartları, küçük bir ayrıntı gibi görünse de özellikle büyük ekiplerde proje yönetiminin önemli bir parçasıdır. Düzenli commit mesajları sayesinde geliştiriciler geçmiş değişiklikleri kolayca takip edebilir, hataları daha hızlı analiz edebilir ve daha sürdürülebilir bir yazılım geliştirme süreci oluşturabilir.
