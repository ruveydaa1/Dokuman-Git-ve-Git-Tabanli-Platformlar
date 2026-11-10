# Merge Conflict

Merge Conflict (Birleştirme Çakışması), iki veya daha fazla branch üzerinde aynı dosyanın aynı bölümünde yapılan farklı değişikliklerin Git tarafından otomatik olarak birleştirilemediği durumdur. Bu durumda Git, hangi değişikliğin korunacağına karar veremez ve merge işlemini durdurarak geliştiriciden çakışmayı çözmesini ister.

Merge conflict, ekip çalışmalarında karşılaşılabilecek doğal bir durumdur. Düzenli branch yönetimi ve sık aralıklarla yapılan güncellemeler sayesinde bu tür çakışmaların sayısı azaltılabilir.

### Merge Conflict Nasıl Oluşur?

Merge conflict genellikle aşağıdaki durumlarda meydana gelir:

* Aynı dosyanın aynı satırları farklı branch'lerde değiştirilmişse,
* Bir branch'te silinen bir dosya, diğer branch'te düzenlenmişse,
* Aynı dosya farklı branch'lerde farklı isimlerle yeniden adlandırılmışsa.

Bu gibi durumlarda Git, hangi değişikliğin korunması gerektiğini belirleyemediği için otomatik birleştirme işlemini gerçekleştiremez.

### Merge Conflict Süreci

Bir merge conflict oluştuğunda genel süreç aşağıdaki şekilde ilerler:

1. Merge işlemi başlatılır.
2. Git çakışan dosyaları tespit eder.
3. Merge işlemi durdurulur.
4. Geliştirici çakışan dosyaları inceleyerek gerekli düzenlemeleri yapar.
5. Düzenlenen dosyalar tekrar Staging Area'ya eklenir.
6. Merge işlemi tamamlanır ve yeni bir commit oluşturulur.

### Çakışma İşaretleri

Merge conflict oluştuğunda Git, çakışan bölümleri dosya içerisine özel işaretlerle ekler.

Örnek:

```
<<<<<<< HEAD
Mevcut branch'teki içerik
=======
Birleştirilen branch'teki içerik
>>>>>>> feature-login
```

Bu işaretlerin anlamı şöyledir:

* **`<<<<<<< HEAD`** : Bulunulan branch'teki değişiklikleri gösterir.
* **`=======`** : İki değişiklik arasındaki ayırıcıdır.
* **`>>>>>>> feature-login`** : Birleştirilmeye çalışılan branch'teki değişiklikleri gösterir.

Geliştirici, hangi kodun korunacağına karar verdikten sonra bu işaretleri silerek dosyayı düzenlemelidir.

### Merge Conflict Oluşmasını Azaltmak İçin Öneriler

Merge conflict tamamen engellenemese de aşağıdaki uygulamalar çakışma ihtimalini azaltabilir:

* Branch'ler uzun süre güncellenmeden bırakılmamalıdır.
* Düzenli olarak uzak depodaki güncellemeler alınmalıdır.
* Küçük ve bağımsız geliştirmeler tercih edilmelidir.
* Anlamlı branch yapıları kullanılmalıdır.
* Merge işleminden önce kod incelemesi yapılmalıdır.
* Ekip üyeleri birbirlerinin çalışmaları hakkında iletişim hâlinde olmalıdır.

### Merge Conflict Sonrası Kontroller

Çakışmalar çözüldükten sonra yapılan değişikliklerin dikkatlice gözden geçirilmesi ve uygulamanın test edilmesi önerilir. Böylece merge sırasında oluşabilecek hatalar erken aşamada tespit edilebilir ve proje bütünlüğü korunabilir.

Merge conflict, Git ile çalışan ekiplerin zaman zaman karşılaştığı doğal bir süreçtir. Çakışmaların doğru şekilde yönetilmesi, proje geçmişinin korunmasını ve geliştirme sürecinin güvenli bir şekilde devam etmesini sağlar.
