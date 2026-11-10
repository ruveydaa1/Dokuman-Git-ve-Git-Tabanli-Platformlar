# Branch İşlemleri

Branch (dal), Git'te ana projeyi etkilemeden bağımsız olarak geliştirme yapılmasını sağlayan yapıdır. Yeni özellik geliştirme, hata düzeltme veya farklı çalışmalar genellikle ayrı branch'ler üzerinde gerçekleştirilir. Çalışmalar tamamlandıktan sonra ilgili branch ana branch ile birleştirilir.

Bu bölümde branch oluşturma, görüntüleme, değiştirme, birleştirme ve silme işlemlerinde kullanılan temel Git komutları açıklanmaktadır.

***

### git branch

Repository'de bulunan branch'leri listelemek veya yeni bir branch oluşturmak için kullanılır.

#### Sözdizimi

Mevcut branch'leri listelemek için:

```bash
git branch
```

Yeni bir branch oluşturmak için:

```bash
git branch <branch_adı>
```

#### Örnek

```bash
git branch feature-login
```

Bu komut yalnızca yeni branch'i oluşturur, aktif branch'i değiştirmez.

***

### git branch -a

Yerel ve uzak depoda bulunan tüm branch'leri listeler.

#### Sözdizimi

```bash
git branch -a
```

***

### git switch

Mevcut branch'i değiştirmek için kullanılır.

#### Sözdizimi

```bash
git switch <branch_adı>
```

#### Örnek

```bash
git switch feature-login
```

***

### git switch -c

Yeni bir branch oluşturur ve doğrudan o branch'e geçiş yapar.

#### Sözdizimi

```bash
git switch -c <branch_adı>
```

#### Örnek

```bash
git switch -c feature-register
```

***

### git checkout

Git'in eski sürümlerinde branch değiştirmek için kullanılan komuttur.

#### Sözdizimi

```bash
git checkout <branch_adı>
```

#### Örnek

```bash
git checkout main
```

Yeni Git sürümlerinde branch değiştirme işlemleri için **git switch** komutunun kullanılması önerilmektedir.

***

### git checkout -b

Yeni bir branch oluşturur ve oluşturulan branch'e geçiş yapar.

#### Sözdizimi

```bash
git checkout -b <branch_adı>
```

#### Örnek

```bash
git checkout -b feature-profile
```

Bu komut, **git branch** ve **git switch** işlemlerini tek adımda gerçekleştirir.

***

### git merge

Bir branch'te yapılan değişiklikleri başka bir branch ile birleştirmek için kullanılır.

#### Sözdizimi

```bash
git merge <branch_adı>
```

#### Örnek

```bash
git merge feature-login
```

Bu işlem, belirtilen branch'teki değişiklikleri aktif branch'e aktarır.

***

### git branch -d

Artık kullanılmayan bir branch'i silmek için kullanılır.

#### Sözdizimi

```bash
git branch -d <branch_adı>
```

#### Örnek

```bash
git branch -d feature-login
```

Git, henüz merge edilmemiş branch'lerin silinmesini engeller.

***

### git branch -D

Merge edilmemiş olsa bile branch'i zorla silmek için kullanılır.

#### Sözdizimi

```bash
git branch -D <branch_adı>
```

#### Örnek

```bash
git branch -D feature-login
```

Bu komut dikkatli kullanılmalıdır. Çünkü merge edilmemiş değişiklikler kaybedilebilir.

***

### Branch İşlemleri Komutlarının Özeti

<table data-search="false"><thead><tr><th>Komut</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>git branch</code></td><td>Branch'leri listeler veya yeni branch oluşturur.</td></tr><tr><td><code>git branch -a</code></td><td>Yerel ve uzak branch'leri listeler.</td></tr><tr><td><code>git switch</code></td><td>Mevcut branch'i değiştirir.</td></tr><tr><td><code>git switch -c</code></td><td>Yeni branch oluşturur ve geçiş yapar.</td></tr><tr><td><code>git checkout</code></td><td>Branch değiştirir (eski kullanım).</td></tr><tr><td><code>git checkout -b</code></td><td>Yeni branch oluşturur ve geçiş yapar.</td></tr><tr><td><code>git merge</code></td><td>Branch'leri birleştirir.</td></tr><tr><td><code>git branch -d</code></td><td>Merge edilmiş branch'i siler.</td></tr><tr><td><code>git branch -D</code></td><td>Branch'i zorla siler.</td></tr></tbody></table>

Branch işlemleri, Git'in en güçlü özelliklerinden biridir. Geliştiriciler farklı özellikleri veya hata düzeltmelerini birbirinden bağımsız olarak geliştirebilir, çalışmalarını güvenli bir şekilde test edebilir ve tamamlandığında ana branch ile birleştirebilir. Bu yaklaşım, özellikle ekip çalışmalarında düzenli ve sürdürülebilir bir geliştirme süreci sağlar.
