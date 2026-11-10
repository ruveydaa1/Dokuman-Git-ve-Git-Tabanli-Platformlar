# Remote İşlemleri

Git'te Remote Repository (Uzak Depo), proje dosyalarının internet üzerindeki ortak bir depoda saklandığı yapıdır. Geliştiriciler yerel ortamda yaptıkları değişiklikleri uzak depoya gönderebilir, diğer geliştiriciler tarafından yapılan güncellemeleri kendi bilgisayarlarına alabilir ve ekip çalışmasını etkin bir şekilde sürdürebilir.

Bu bölümde uzak depoların yönetimi ve uzak depolar ile veri alışverişi sırasında kullanılan temel Git komutları açıklanmaktadır.

***

### git remote

Repository'ye tanımlı uzak depoları listelemek için kullanılır.

#### Sözdizimi

```bash
git remote
```

#### Örnek

```bash
git remote
```

Örnek çıktı:

```
origin
```

***

### git remote -v

Tanımlı uzak depoların adlarını ve bağlantı adreslerini görüntüler.

#### Sözdizimi

```bash
git remote -v
```

#### Örnek Çıktı

```
origin  https://github.com/kullanici/proje.git (fetch)
origin  https://github.com/kullanici/proje.git (push)
```

***

### git remote add

Repository'ye yeni bir uzak depo eklemek için kullanılır.

#### Sözdizimi

```bash
git remote add <isim> <repository-url>
```

#### Örnek

```bash
git remote add origin https://github.com/kullanici/proje.git
```

Genellikle ilk uzak depo **origin** adıyla tanımlanır.

***

### git fetch

Uzak depodaki güncel değişiklikleri indirir ancak çalışma dizinine uygulamaz.

#### Sözdizimi

```bash
git fetch
```

Bu komut, değişiklikleri incelemek isteyen geliştiriciler için güvenli bir yöntem sunar.

***

### git pull

Uzak depodaki güncel değişiklikleri indirir ve mevcut branch ile birleştirir.

#### Sözdizimi

```bash
git pull
```

Bu komut, **git fetch** ve **git merge** işlemlerini tek adımda gerçekleştirir.

***

### git push

Yerel depoda bulunan commit'leri uzak depoya gönderir.

#### Sözdizimi

```bash
git push
```

#### Örnek

```bash
git push origin main
```

Bu komut, **main** branch'indeki değişiklikleri **origin** isimli uzak depoya gönderir.

***

### git push -u

Yerel branch ile uzak branch arasında takip (tracking) ilişkisi oluşturur.

#### Sözdizimi

```bash
git push -u <remote> <branch>
```

#### Örnek

```bash
git push -u origin main
```

Bu işlemden sonra aynı branch için yalnızca **git push** ve **git pull** komutlarını kullanmak yeterli olur.

***

### Remote İşlemleri Komutlarının Özeti

<table data-search="false"><thead><tr><th>Komut</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>git remote</code></td><td>Tanımlı uzak depoları listeler.</td></tr><tr><td><code>git remote -v</code></td><td>Uzak depoları adresleriyle birlikte görüntüler.</td></tr><tr><td><code>git remote add</code></td><td>Yeni bir uzak depo ekler.</td></tr><tr><td><code>git fetch</code></td><td>Uzak depodaki değişiklikleri indirir.</td></tr><tr><td><code>git pull</code></td><td>Değişiklikleri indirir ve mevcut branch ile birleştirir.</td></tr><tr><td><code>git push</code></td><td>Yerel commit'leri uzak depoya gönderir.</td></tr><tr><td><code>git push -u</code></td><td>Takip ilişkisi oluşturarak ilk gönderimi gerçekleştirir.</td></tr></tbody></table>

Remote işlemleri, Git'in ekip çalışmasını destekleyen en önemli özelliklerinden biridir. Bu komutlar sayesinde geliştiriciler yerel ortamda yaptıkları çalışmaları uzak depolar ile senkronize edebilir, proje güncellemelerini takip edebilir ve ortak geliştirme süreçlerini verimli bir şekilde yönetebilir.
