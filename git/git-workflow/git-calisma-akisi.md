# Git Çalışma Akışı

Git, proje üzerinde yapılan değişiklikleri doğrudan sürüm geçmişine kaydetmez. Bunun yerine değişiklikler belirli aşamalardan geçirilerek kontrol edilir ve daha sonra kayıt altına alınır. Bu çalışma modeli sayesinde geliştiriciler hangi dosyaların kaydedileceğini, hangi değişikliklerin paylaşılacağını ve proje geçmişine nelerin ekleneceğini kontrol edebilir.

Git'in temel çalışma akışı dört ana bileşenden oluşmaktadır:

```
Working Directory
        │
   git add
        ▼
 Staging Area
        │
 git commit
        ▼
Local Repository
        │
  git push
        ▼
Remote Repository
```

### Working Directory

Working Directory (Çalışma Dizini), proje dosyalarının bulunduğu ve geliştiricinin aktif olarak çalıştığı alandır. Yeni dosya oluşturma, mevcut dosyaları düzenleme veya silme gibi işlemler bu aşamada gerçekleştirilir.

Bu aşamada yapılan değişiklikler henüz Git tarafından sürüm geçmişine eklenmemiştir.

***

### Staging Area

Staging Area (Hazırlık Alanı), commit işleminden önce değişikliklerin toplandığı geçici alandır.

Geliştirici, **`git add`** komutunu kullanarak hangi dosyaların bir sonraki commit işlemine dahil edileceğini belirler. Böylece tüm değişiklikleri değil, yalnızca istenen dosyaları sürüm geçmişine eklemek mümkün olur.

***

### Local Repository

Staging Area'ya eklenen değişiklikler **`git commit`** komutu ile Local Repository'ye kaydedilir.

Commit işlemi tamamlandığında proje için yeni bir sürüm oluşturulur ve bu sürüm Git tarafından benzersiz bir Commit ID ile kayıt altına alınır. Bu sayede proje geçmişindeki tüm değişiklikler izlenebilir ve gerektiğinde önceki sürümlere geri dönülebilir.

***

### Remote Repository

Local Repository'de bulunan commit'ler yalnızca geliştiricinin kendi bilgisayarında saklanır.

Bu değişikliklerin diğer ekip üyeleriyle paylaşılması için **`git push`** komutu kullanılarak uzak depoya (Remote Repository) gönderilmesi gerekir. Uzak depolar genellikle GitHub, GitLab veya GitBucket gibi platformlarda barındırılır.

Benzer şekilde, ekip üyeleri tarafından yapılan güncellemeleri yerel depoya almak için **`git pull`** komutu kullanılır.

***

### Git Çalışma Akışının Özeti

Git'in çalışma süreci aşağıdaki adımlardan oluşur:

1. Proje dosyaları üzerinde değişiklik yapılır (**Working Directory**).
2. Kaydedilmesi istenen değişiklikler **`git add`** komutu ile **Staging Area**'ya eklenir.
3. Değişiklikler **`git commit`** komutu ile **Local Repository**'ye kaydedilir.
4. Oluşturulan commit'ler **`git push`** komutu ile **Remote Repository**'ye gönderilir.
5. Diğer geliştiricilerin yaptığı değişiklikler gerektiğinde **`git pull`** komutu ile yerel depoya alınır.

Bu aşamalı çalışma modeli sayesinde Git, yapılan değişikliklerin kontrollü bir şekilde yönetilmesini, proje geçmişinin güvenli olarak saklanmasını ve ekip üyeleri arasında düzenli bir iş birliği yürütülmesini sağlar.
