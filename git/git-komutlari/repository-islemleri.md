# Repository İşlemleri

Repository (Depo), Git tarafından yönetilen proje dosyalarının ve sürüm geçmişinin bulunduğu çalışma alanıdır. Git ile çalışmaya başlanırken ilk olarak yeni bir repository oluşturulur veya mevcut bir repository yerel ortama kopyalanır.

Bu bölümde repository yönetiminde kullanılan temel Git komutları açıklanmaktadır.

***

### git init

Yeni bir Git repository'si oluşturmak için kullanılır. Komut çalıştırıldığında mevcut dizin içerisinde **.git** adlı gizli bir klasör oluşturulur ve ilgili dizin Git tarafından takip edilmeye başlanır.

#### Sözdizimi

```bash
git init
```

#### Örnek

```bash
mkdir proje
cd proje
git init
```

Bu işlem sonucunda **proje** klasörü Git repository'si haline gelir.

***

### git clone

Uzak bir repository'nin yerel bilgisayara kopyalanmasını sağlar.

Repository içerisindeki tüm dosyalar, branch yapıları ve commit geçmişi yerel ortama indirilir.

#### Sözdizimi

```bash
git clone <repository-url>
```

#### Örnek

```bash
git clone https://github.com/kullanici/proje.git
```

Belirli bir klasör adı verilerek de klonlama yapılabilir.

```bash
git clone https://github.com/kullanici/proje.git yeni-proje
```

***

### git status

Repository'nin mevcut durumunu görüntüler.

Hangi dosyaların değiştirildiği, hangilerinin Staging Area'da bulunduğu ve commit edilmeyi bekleyen değişiklikler bu komut ile görülebilir.

#### Sözdizimi

```bash
git status
```

#### Örnek

```bash
git status
```

Örnek çıktı:

```
On branch main

Changes not staged for commit:
    modified: app.js

Untracked files:
    README.md
```

***

### Repository İşlemlerinde Kullanılan Komutların Özeti

| Komut        | Açıklama                                   |
| ------------ | ------------------------------------------ |
| `git init`   | Yeni bir Git repository'si oluşturur.      |
| `git clone`  | Uzak repository'yi yerel ortama kopyalar.  |
| `git status` | Repository'nin mevcut durumunu görüntüler. |

Repository işlemleri, Git ile çalışmanın ilk adımını oluşturur. Repository oluşturulduktan veya klonlandıktan sonra dosya değişiklikleri takip edilebilir ve sürüm yönetimi işlemlerine başlanabilir.
