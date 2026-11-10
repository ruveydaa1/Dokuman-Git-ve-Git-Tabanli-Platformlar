# Commit İşlemleri

Commit, Git'te belirli bir anda proje üzerinde yapılan değişikliklerin kalıcı olarak kayıt altına alınmasını sağlayan işlemdir. Her commit, projenin o anki durumunu temsil eder ve benzersiz bir kimliğe (Commit ID) sahiptir. Commit işlemleri sayesinde proje geçmişi takip edilebilir, önceki sürümlere dönülebilir ve yapılan değişiklikler ayrıntılı olarak incelenebilir.

Bu bölümde commit oluşturma, commit geçmişini görüntüleme ve commit bilgilerini düzenleme amacıyla kullanılan temel Git komutları açıklanmaktadır.

***

### git commit

Staging Area'da bulunan değişiklikleri Local Repository'ye kaydetmek için kullanılır.

#### Sözdizimi

```bash
git commit
```

Bu komut çalıştırıldığında Git, varsayılan metin düzenleyicisini açarak commit mesajının girilmesini ister.

***

### git commit -m

Commit mesajını komut satırından yazarak doğrudan commit oluşturmayı sağlar.

#### Sözdizimi

```bash
git commit -m "<commit_mesajı>"
```

#### Örnek

```bash
git commit -m "README dosyası güncellendi."
```

Anlamlı ve açıklayıcı commit mesajları kullanılması, proje geçmişinin okunabilirliği açısından önemlidir.

***

### git commit --amend

Son oluşturulan commit üzerinde değişiklik yapmak veya commit mesajını güncellemek için kullanılır.

#### Sözdizimi

```bash
git commit --amend
```

Yeni bir commit oluşturmaz; son commit'i günceller.

***

### git log

Repository'deki commit geçmişini ayrıntılı olarak görüntüler.

#### Sözdizimi

```bash
git log
```

#### Örnek Çıktı

```
commit 8b8d6f5...
Author: Ahmet Yılmaz
Date: ...

    README dosyası güncellendi.
```

***

### git log --oneline

Commit geçmişini kısa ve tek satır halinde görüntüler.

#### Sözdizimi

```bash
git log --oneline
```

#### Örnek Çıktı

```
8b8d6f5 README dosyası güncellendi.
42fd7e1 Yeni dosya eklendi.
```

Bu görünüm, commit geçmişini hızlı bir şekilde incelemek için tercih edilir.

***

### git show

Belirli bir commit'e ait ayrıntıları görüntülemek için kullanılır.

#### Sözdizimi

```bash
git show
```

Belirli bir commit görüntülenmek istenirse Commit ID belirtilir.

```bash
git show <commit_id>
```

Bu komut; commit bilgilerini, commit mesajını ve ilgili değişiklikleri ayrıntılı olarak gösterir.

***

### git tag

Belirli bir commit'i sürüm etiketi (tag) ile işaretlemek için kullanılır.

Tag'ler genellikle uygulamanın yayınlanan sürümlerini (örneğin **v1.0**, **v2.0**) belirtmek amacıyla kullanılır.

#### Sözdizimi

```bash
git tag <etiket_adı>
```

#### Örnek

```bash
git tag v1.0
```

Oluşturulan tüm etiketler aşağıdaki komut ile görüntülenebilir.

```bash
git tag
```

***

### Commit İşlemleri Komutlarının Özeti

<table data-search="false"><thead><tr><th>Komut</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>git commit</code></td><td>Staging Area'daki değişiklikleri commit olarak kaydeder.</td></tr><tr><td><code>git commit -m</code></td><td>Mesaj belirtilerek commit oluşturur.</td></tr><tr><td><code>git commit --amend</code></td><td>Son commit'i günceller.</td></tr><tr><td><code>git log</code></td><td>Commit geçmişini ayrıntılı olarak gösterir.</td></tr><tr><td><code>git log --oneline</code></td><td>Commit geçmişini kısa formatta gösterir.</td></tr><tr><td><code>git show</code></td><td>Commit ayrıntılarını görüntüler.</td></tr><tr><td><code>git tag</code></td><td>Belirli bir commit için sürüm etiketi oluşturur.</td></tr></tbody></table>

Commit işlemleri, Git'in en temel bileşenlerinden biridir. Düzenli ve anlamlı commit mesajları kullanılarak oluşturulan sürüm geçmişi, proje gelişiminin kolayca takip edilmesini ve ekip çalışmalarının daha verimli yürütülmesini sağlar.
