# Git Yapılandırması

Git kurulumu tamamlandıktan sonra, sürüm yönetimi işlemlerine başlamadan önce temel kullanıcı bilgilerinin yapılandırılması önerilir. Bu bilgiler, oluşturulan commit'lere otomatik olarak eklenir ve yapılan değişikliklerin hangi kullanıcı tarafından gerçekleştirildiğini gösterir.

Git yapılandırma işlemleri **`git config`** komutu ile gerçekleştirilir. Yapılandırmalar sistem genelinde (**global**) veya yalnızca belirli bir repository (**local**) için tanımlanabilir.

### Global ve Local Yapılandırma

Git yapılandırmaları iki farklı kapsamda uygulanabilir:

* **Global Yapılandırma (`--global`)**: Yapılan ayarlar bilgisayardaki tüm Git repository'leri için geçerli olur.
* **Local Yapılandırma**: Ayarlar yalnızca bulunulan repository için geçerli olur ve diğer projeleri etkilemez.

Genellikle kullanıcı adı ve e-posta adresi global olarak tanımlanır.

***

### Kullanıcı Adı Tanımlama

Git'te oluşturulan commit'lerin hangi kullanıcı tarafından yapıldığını belirtmek için kullanıcı adı tanımlanır.

#### Sözdizimi

```bash
git config --global user.name "<kullanıcı_adı>"
```

#### Örnek

```bash
git config --global user.name "Ahmet Yılmaz"
```

***

### E-posta Adresi Tanımlama

Commit'lere ait kullanıcı bilgilerini tamamlamak için e-posta adresi tanımlanır.

#### Sözdizimi

```bash
git config --global user.email "<e-posta>"
```

#### Örnek

```bash
git config --global user.email "ahmet@example.com"
```

***

### Yapılandırmaları Görüntüleme

Tanımlanan tüm Git yapılandırmaları aşağıdaki komut ile görüntülenebilir.

#### Sözdizimi

```bash
git config --list
```

#### Örnek Çıktı

```
user.name=Ahmet Yılmaz
user.email=ahmet@example.com
core.editor=code --wait
init.defaultBranch=main
```

***

### Belirli Bir Yapılandırmayı Görüntüleme

İstenilen bir yapılandırma değeri tek başına da görüntülenebilir.

#### Kullanıcı Adı

```bash
git config user.name
```

#### E-posta Adresi

```bash
git config user.email
```

***

### Varsayılan Branch Adını Belirleme

Yeni oluşturulan repository'lerde kullanılacak varsayılan branch adı değiştirilebilir.

#### Sözdizimi

```bash
git config --global init.defaultBranch main
```

Bu ayar yapıldığında yeni oluşturulan repository'lerde varsayılan branch **main** olarak oluşturulur.

***

### Varsayılan Editörü Belirleme

Git tarafından kullanılacak varsayılan metin editörü değiştirilebilir.

#### Visual Studio Code

```bash
git config --global core.editor "code --wait"
```

***

### Yapılandırmayı Güncelleme

Daha önce tanımlanmış bir yapılandırma değeri aynı komut tekrar çalıştırılarak güncellenebilir.

Örneğin kullanıcı adını değiştirmek için:

```bash
git config --global user.name "Yeni Kullanıcı"
```

Git eski değeri otomatik olarak yeni değer ile değiştirir.

***

### Git Yapılandırma Komutlarının Özeti

<table data-search="false"><thead><tr><th>Komut</th><th>Açıklama</th></tr></thead><tbody><tr><td><code>git config --global user.name</code></td><td>Kullanıcı adını tanımlar.</td></tr><tr><td><code>git config --global user.email</code></td><td>E-posta adresini tanımlar.</td></tr><tr><td><code>git config --list</code></td><td>Tüm Git yapılandırmalarını görüntüler.</td></tr><tr><td><code>git config user.name</code></td><td>Kullanıcı adını görüntüler.</td></tr><tr><td><code>git config user.email</code></td><td>E-posta adresini görüntüler.</td></tr><tr><td><code>git config --global init.defaultBranch main</code></td><td>Varsayılan branch adını belirler.</td></tr><tr><td><code>git config --global core.editor</code></td><td>Varsayılan metin editörünü belirler.</td></tr></tbody></table>

Git yapılandırması tamamlandıktan sonra repository oluşturma, dosya yönetimi, commit işlemleri ve diğer Git komutları kullanılmaya başlanabilir.
