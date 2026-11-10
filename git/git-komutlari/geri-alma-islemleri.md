# Geri Alma İşlemleri

Yazılım geliştirme sürecinde zaman zaman yapılan değişikliklerin geri alınması veya hatalı işlemlerin düzeltilmesi gerekebilir. Git, dosya değişikliklerini, Staging Area'daki işlemleri ve commit geçmişini güvenli bir şekilde yönetebilmek için çeşitli geri alma komutları sunmaktadır.

Bu bölümde çalışma dizinindeki değişiklikleri geri alma, Staging Area'dan dosya çıkarma ve hatalı commit'leri düzeltme amacıyla kullanılan temel Git komutları açıklanmaktadır.

***

### git restore

Çalışma dizininde (Working Directory) yapılan ancak henüz commit edilmemiş değişiklikleri geri almak için kullanılır.

#### Sözdizimi

```bash
git restore <dosya_adı>
```

#### Örnek

```bash
git restore README.md
```

Bu komut, belirtilen dosyayı son commit durumuna geri döndürür.

***

### git restore --staged

Staging Area'ya eklenen bir dosyayı hazırlık alanından çıkarmak için kullanılır. Dosya üzerindeki değişiklikler korunur, yalnızca Staging Area'dan kaldırılır.

#### Sözdizimi

```bash
git restore --staged <dosya_adı>
```

#### Örnek

```bash
git restore --staged README.md
```

Bu komut, yanlışlıkla Staging Area'ya eklenen dosyaların kolayca geri alınmasını sağlar.

***

### git revert

Daha önce oluşturulmuş bir commit'in etkisini geri alan yeni bir commit oluşturur.

#### Sözdizimi

```bash
git revert <commit_id>
```

#### Örnek

```bash
git revert a1b2c3d
```

`git revert` mevcut commit geçmişini silmez veya değiştirmez. Bunun yerine belirtilen commit'in yaptığı değişiklikleri tersine çeviren yeni bir commit oluşturur. Bu nedenle özellikle ortak (shared) repository'lerde güvenli bir geri alma yöntemi olarak tercih edilir.

***

### Geri Alma İşlemleri Komutlarının Özeti

| Komut                  | Açıklama                                                             |
| ---------------------- | -------------------------------------------------------------------- |
| `git restore`          | Commit edilmemiş dosya değişikliklerini geri alır.                   |
| `git restore --staged` | Dosyayı Staging Area'dan çıkarır ancak dosya değişikliklerini korur. |
| `git revert`           | Belirtilen commit'i geri alan yeni bir commit oluşturur.             |

### Komutların Kullanım Amaçları

Geri alma işlemleri sırasında kullanılacak komut, geri alınmak istenen değişikliğin türüne göre farklılık gösterir.

* **`git restore`**, çalışma dizininde yapılan ancak henüz commit edilmemiş değişiklikleri iptal etmek için kullanılır.
* **`git restore --staged`**, Staging Area'ya eklenen dosyaları hazırlık alanından çıkarmak için kullanılır.
* **`git revert`**, daha önce oluşturulmuş bir commit'in etkisini güvenli bir şekilde geri almak için kullanılır.

Doğru komutun seçilmesi, proje geçmişinin korunması ve veri kaybının önlenmesi açısından önemlidir.
