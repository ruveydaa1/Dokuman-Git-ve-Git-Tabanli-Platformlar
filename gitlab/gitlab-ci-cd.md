# GitLab CI/CD

GitLab CI/CD, yazılım geliştirme süreçlerinde kod değişikliklerinin otomatik olarak test edilmesini, derlenmesini ve dağıtılmasını sağlayan GitLab'ın yerleşik otomasyon sistemidir.

CI/CD yaklaşımı sayesinde geliştiriciler manuel olarak yapılan tekrar eden işlemleri otomatikleştirebilir. Kod repository'ye gönderildiğinde belirlenen kurallara göre test, build ve deployment işlemleri otomatik olarak gerçekleştirilebilir.

GitLab CI/CD, GitLab platformu içerisine doğrudan entegre edilmiştir ve yapılandırma işlemleri `.gitlab-ci.yml` dosyası üzerinden gerçekleştirilir.

***

## CI/CD Nedir?

### Continuous Integration (CI)

Sürekli Entegrasyon, geliştiricilerin yaptığı kod değişikliklerinin düzenli olarak birleştirilmesini ve otomatik kontrollerden geçirilmesini sağlayan süreçtir.

CI süreçlerinde:

* Kod derleme
* Otomatik test çalıştırma
* Kod kalitesi kontrolü
* Hata tespiti

işlemleri gerçekleştirilir.

***

### Continuous Deployment / Delivery (CD)

Sürekli Dağıtım, başarılı şekilde test edilen uygulamaların otomatik olarak yayınlanmasını sağlayan süreçtir.

CD süreçlerinde:

* Uygulamanın paketlenmesi
* Ortama gönderilmesi
* Yeni sürümün yayınlanması

işlemleri otomatikleştirilebilir.

***

## GitLab CI/CD Çalışma Mantığı

GitLab CI/CD temel olarak aşağıdaki bileşenlerden oluşur:

* Pipeline
* Stage
* Job
* Runner
* Artifact
* Environment

Bu bileşenler birlikte çalışarak otomatik geliştirme süreçlerini oluşturur.

***

## Pipeline

Pipeline, bir kod değişikliğinden sonra çalıştırılan tüm otomasyon süreçlerinin genel yapısıdır.

Bir pipeline içerisinde farklı aşamalar (stage) bulunabilir.

Örnek:

```
Pipeline

   |
   ├── Build Stage
   |
   ├── Test Stage
   |
   └── Deploy Stage
```

Pipeline, repository içerisine yapılan bir commit veya merge işlemi ile otomatik olarak tetiklenebilir.

***

## Stage

Stage, pipeline içerisindeki işlem aşamalarını ifade eder.

Yaygın stage örnekleri:

* Build
* Test
* Deploy

Stage'ler genellikle sıralı şekilde çalışır.

Örnek:

```
Build

  ↓

Test

  ↓

Deploy
```

Bir stage başarılı olmadan sonraki aşamaya geçilmez.

***

## Job

Job, bir stage içerisinde gerçekleştirilen tekil görevlerdir.

Örneğin Test stage içerisinde:

* Unit test çalıştırma
* Kod analizi yapma

gibi farklı job'lar bulunabilir.

Örnek:

```
Test Stage

 ├── Unit Test Job
 |
 └── Security Scan Job
```

***

## GitLab Runner

GitLab Runner, CI/CD işlemlerini çalıştıran uygulamadır.

Runner:

* Pipeline job'larını çalıştırır.
* Komutları gerçekleştirir.
* Sonuçları GitLab'a gönderir.

Runner türleri:

### Shared Runner

GitLab tarafından sağlanan ve birçok proje tarafından kullanılabilen runner'lardır.

### Specific Runner

Belirli bir proje için özel olarak yapılandırılan runner'lardır.

### Group Runner

Bir grup içerisindeki tüm projeler tarafından kullanılabilen runner'lardır.

***

## .gitlab-ci.yml Dosyası

GitLab CI/CD yapılandırmaları `.gitlab-ci.yml` dosyası içerisinde tanımlanır.

Bu dosya:

* Pipeline yapısını
* Stage'leri
* Job'ları
* Kullanılacak komutları
* Çalışma koşullarını

belirler.

Örnek:

```yaml
stages:
  - test
  - build

test_job:
  stage: test
  script:
    - npm install
    - npm test

build_job:
  stage: build
  script:
    - npm run build
```

Bu örnekte:

1. Test stage çalışır.
2. Testler başarılı olursa build aşamasına geçilir.
3. Uygulama oluşturulur.

***

## Artifact

Artifact, pipeline sırasında oluşturulan ve sonraki aşamalarda kullanılabilen dosyalardır.

Örnek:

* Build çıktıları
* Paketlenmiş uygulamalar
* Test raporları

Artifact kullanımı sayesinde bir job tarafından oluşturulan dosyalar başka job'lara aktarılabilir.

***

## Environment

Environment, uygulamanın dağıtıldığı çalışma ortamlarını ifade eder.

Örnek:

* Development
* Testing
* Staging
* Production

GitLab CI/CD ile farklı ortamlara otomatik dağıtım yapılabilir.

***

## GitLab CI/CD Kullanım Alanları

GitLab CI/CD birçok farklı amaçla kullanılabilir:

### Otomatik Test

Kod değişikliklerinden sonra testlerin otomatik çalıştırılması sağlanabilir.

### Build İşlemleri

Uygulama paketleme ve derleme işlemleri otomatik yapılabilir.

### Deployment

Uygulamalar farklı ortamlara otomatik olarak gönderilebilir.

### Güvenlik Kontrolleri

Kod analizleri ve güvenlik taramaları pipeline içerisine eklenebilir.

***

## GitLab CI/CD Avantajları

GitLab CI/CD kullanmanın avantajları:

* GitLab ile doğrudan entegre çalışır.
* Otomasyon süreçlerini kolaylaştırır.
* Manuel işlemleri azaltır.
* Hataların erken tespit edilmesini sağlar.
* Yazılım teslim süreçlerini hızlandırır.
* DevOps kültürünü destekler.

***

## GitLab CI/CD ve DevOps

GitLab CI/CD, modern DevOps süreçlerinin önemli bir parçasıdır. Kod geliştirme, test, güvenlik kontrolü ve dağıtım aşamalarının otomatikleştirilmesini sağlayarak yazılım teslim süreçlerinin daha hızlı, güvenilir ve standart hâle gelmesine yardımcı olur.

GitLab'ın CI/CD özelliklerini platform içerisinde yerleşik olarak sunması, onu özellikle sürekli entegrasyon ve sürekli dağıtım süreçleri kullanan ekipler için güçlü bir çözüm hâline getirir.
