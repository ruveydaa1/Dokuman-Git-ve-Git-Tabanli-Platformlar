# Dosya İşlemleri

Git'te dosya işlemleri, proje içerisinde oluşturulan, düzenlenen, taşınan veya silinen dosyaların sürüm yönetimine dahil edilmesini sağlar. Dosyalar üzerinde yapılan değişiklikler doğrudan sürüm geçmişine eklenmez. Öncelikle ilgili dosyaların Staging Area'ya eklenmesi ve ardından commit edilmesi gerekir.

Bu bölümde Git'te dosya yönetimi sırasında kullanılan temel komutlar açıklanmaktadır.

***

### git add

Belirtilen dosya veya dosyaları Staging Area'ya eklemek için kullanılır.

#### Sözdizimi

```bash
git add <dosya_adı>
```

#### Örnek

```bash
git add app.js
```

Bu komut yalnızca belirtilen dosyayı Staging Area'ya ekler.

***

### git add .

Çalışma dizinindeki tüm yeni ve güncellenmiş dosyaları Staging Area'ya ekler.

#### Sözdizimi

```bash
git add .
```

#### Örnek

```bash
git add .
```

Bu komut, birden fazla dosyada yapılan değişikliklerin tek seferde hazırlanmasını sağlar.

***

### git rm

Bir dosyayı hem çalışma dizininden hem de Git repository'sinden kaldırmak için kullanılır.

#### Sözdizimi

```bash
git rm <dosya_adı>
```

#### Örnek

```bash
git rm eski-dosya.txt
```

Dosya silindikten sonra yapılan değişiklik commit edildiğinde repository'den de kaldırılmış olur.

***

### git mv

Bir dosyanın adını değiştirmek veya farklı bir konuma taşımak için kullanılır.

#### Sözdizimi

```bash
git mv <eski_ad> <yeni_ad>
```

#### Örnek

```bash
git mv app.js main.js
```

Bu komut dosyayı yeniden adlandırır ve yapılan değişikliği Git tarafından takip edilecek şekilde hazırlar.

***

### git diff

Henüz commit edilmemiş değişiklikleri görüntülemek için kullanılır.

Bu komut sayesinde hangi satırların eklendiği, silindiği veya değiştirildiği ayrıntılı olarak incelenebilir.

#### Sözdizimi

```bash
git diff
```

#### Örnek

```bash
git diff
```

Staging Area'ya eklenmiş değişiklikleri görüntülemek için ise aşağıdaki komut kullanılabilir.

```bash
git diff --staged
```

***

### Dosya İşlemleri Komutlarının Özeti

| Komut               | Açıklama                                                  |
| ------------------- | --------------------------------------------------------- |
| `git add <dosya>`   | Belirli bir dosyayı Staging Area'ya ekler.                |
| `git add .`         | Tüm yeni ve güncellenmiş dosyaları Staging Area'ya ekler. |
| `git rm`            | Dosyayı çalışma dizininden ve repository'den siler.       |
| `git mv`            | Dosyanın adını değiştirir veya farklı bir konuma taşır.   |
| `git diff`          | Commit edilmemiş değişiklikleri görüntüler.               |
| `git diff --staged` | Staging Area'daki değişiklikleri görüntüler.              |

Dosya işlemleri, Git ile sürüm yönetiminin temelini oluşturur. Dosyalar üzerinde yapılan değişiklikler bu komutlar aracılığıyla yönetilir ve daha sonra commit işlemi ile proje geçmişine kaydedilir.
