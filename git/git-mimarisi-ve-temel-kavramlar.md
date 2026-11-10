# Git Mimarisi ve Temel Kavramlar

Git'in etkin bir şekilde kullanılabilmesi için öncelikle çalışma yapısının ve temel bileşenlerinin anlaşılması gerekmektedir. Git, dosyalarda yapılan değişiklikleri belirli aşamalardan geçirerek yönetir ve her aşamada değişikliklerin durumunu takip eder. Bu mimari sayesinde geliştiriciler, hangi dosyaların değiştirildiğini, hangilerinin kayıt altına alınacağını ve hangi sürümlerin oluşturulduğunu kolayca yönetebilir.

Git'in çalışma yapısı temel olarak **Working Directory**, **Staging Area**, **Local Repository** ve **Remote Repository** olmak üzere dört ana bileşenden oluşmaktadır. Bunun yanında **Repository**, **Commit**, **HEAD** ve **Branch** gibi kavramlar da Git'in temel yapı taşları arasında yer almaktadır.

***

### Repository

Repository (Depo), bir projenin dosyalarını ve sürüm geçmişini içeren çalışma alanıdır. Git ile yönetilen her proje bir repository içerisinde bulunur.

Repository iki farklı şekilde kullanılabilir:

* **Local Repository:** Geliştiricinin kendi bilgisayarında bulunan depo.
* **Remote Repository:** GitHub, GitLab veya GitBucket gibi platformlarda bulunan uzak depo.

***

### Working Directory

Working Directory (Çalışma Dizini), proje dosyalarının üzerinde aktif olarak çalışılan bölümüdür. Kod yazma, dosya oluşturma, düzenleme veya silme gibi işlemler bu alanda gerçekleştirilir.

Bu aşamada yapılan değişiklikler henüz Git tarafından sürüm geçmişine eklenmemiştir.

***

### Staging Area

Staging Area (Hazırlık Alanı), commit işleminden önce değişikliklerin toplandığı geçici alandır.

Working Directory üzerinde yapılan değişiklikler, **git add** komutu ile Staging Area'ya eklenir. Böylece hangi dosyaların commit edileceği geliştirici tarafından belirlenebilir.

***

### Local Repository

Local Repository, commit işlemlerinin kaydedildiği yerel depodur.

Staging Area'daki değişiklikler **git commit** komutu ile Local Repository'ye kaydedilir. Böylece proje için yeni bir sürüm oluşturulmuş olur.

***

### Remote Repository

Remote Repository, proje dosyalarının internet üzerindeki ortak depoda saklandığı alandır.

GitHub, GitLab ve GitBucket gibi platformlar Remote Repository hizmeti sunmaktadır. Geliştiriciler **git push** komutu ile yerel değişikliklerini uzak depoya gönderebilir, **git pull** komutu ile ise diğer geliştiricilerin yaptığı değişiklikleri kendi bilgisayarlarına alabilir.

***

### Commit

Commit, belirli bir anda projenin durumunu kayıt altına alan sürümdür.

Her commit benzersiz bir kimliğe (Commit ID) sahiptir ve yapılan değişikliklerin geçmişte izlenebilmesini sağlar.

***

### Branch

Branch (Dal), ana projeyi etkilemeden bağımsız geliştirme yapılmasını sağlayan yapıdır.

Yeni özellik geliştirme, hata düzeltme veya farklı çalışmalar genellikle ayrı branch'lerde gerçekleştirilir. Çalışmalar tamamlandıktan sonra ilgili branch ana projeyle birleştirilebilir.

***

### HEAD

HEAD, Git'in o anda üzerinde çalışılan branch'i veya commit'i gösteren referansıdır.

Varsayılan olarak HEAD, aktif branch'in en son commit'ini işaret eder. Yeni commit oluşturulduğunda HEAD otomatik olarak en güncel commit'e taşınır.

***

### Git'in Çalışma Yapısı

Git'te yapılan işlemler aşağıdaki sıra ile ilerler:

```
Working Directory
        │
    git add
        │
        ▼
 Staging Area
        │
  git commit
        │
        ▼
Local Repository
        │
   git push
        │
        ▼
Remote Repository
```

Bu yapı sayesinde yapılan değişiklikler kontrol edilerek aşamalı bir şekilde kayıt altına alınır ve gerektiğinde diğer geliştiricilerle paylaşılır.
