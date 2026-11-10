# GitHub Actions

GitHub Actions, GitHub tarafından sunulan bir otomasyon ve CI/CD (Continuous Integration / Continuous Deployment) platformudur. Yazılım geliştirme süreçlerinde tekrar eden işlemleri otomatikleştirmek, kod değişikliklerini test etmek, uygulamaları derlemek ve dağıtım süreçlerini yönetmek için kullanılır.

GitHub Actions sayesinde geliştiriciler, repository içerisinde gerçekleşen belirli olaylara göre otomatik çalışan iş akışları (workflow) oluşturabilir. Bu işlemler `.github/workflows` klasörü içerisinde bulunan YAML dosyaları ile tanımlanır.

***

## CI/CD Nedir?

GitHub Actions'ın çalışma mantığını anlamak için öncelikle CI/CD kavramlarını bilmek gerekir.

### Continuous Integration (CI)

Sürekli Entegrasyon, geliştiricilerin yaptığı kod değişikliklerinin düzenli olarak ana projeye dahil edilmesini ve otomatik kontrollerden geçirilmesini sağlayan süreçtir.

CI süreçlerinde genellikle:

* Kod derleme
* Otomatik test çalıştırma
* Kod kalitesi kontrolü
* Hata tespiti

işlemleri gerçekleştirilir.

***

### Continuous Deployment (CD)

Sürekli Dağıtım, başarılı şekilde test edilen uygulamaların otomatik olarak hedef ortama gönderilmesini sağlayan süreçtir.

CD süreçlerinde:

* Uygulama paketleme
* Sunucuya gönderim
* Yeni sürüm yayınlama

işlemleri otomatikleştirilebilir.

***

## GitHub Actions Çalışma Mantığı

GitHub Actions temel olarak **workflow**, **event**, **job**, **step** ve **runner** kavramları üzerine kuruludur.

***

### Workflow

Workflow, otomatik olarak çalıştırılacak işlemlerin tamamını tanımlayan yapılandırma dosyasıdır.

Workflow dosyaları:

```
.github/
 └── workflows/
      └── build.yml
```

konumunda bulunur.

Bir repository içerisinde birden fazla workflow oluşturulabilir.

Örnek:

* Test workflow'u
* Build workflow'u
* Deployment workflow'u

***

### Event

Event, workflow'un hangi durumda çalışacağını belirleyen tetikleyicidir.

Örnek event'ler:

* Push
* Pull Request
* Issue oluşturulması
* Manuel çalıştırma
* Zamanlanmış görevler

Örnek:

```yaml
on:
  push:
    branches:
      - main
```

Bu yapı, main branch'ine yapılan her push işleminde workflow'un çalışmasını sağlar.

***

### Job

Job, workflow içerisinde gerçekleştirilecek işlemler grubudur.

Bir workflow bir veya daha fazla job içerebilir.

Örnek:

```
Workflow

 ├── Build Job
 │
 ├── Test Job
 │
 └── Deploy Job
```

Job'lar varsayılan olarak paralel çalışabilir veya birbirine bağımlı hâle getirilebilir.

***

### Step

Step, bir job içerisindeki küçük işlem adımlarıdır.

Örneğin:

* Repository'i indirme
* Bağımlılıkları yükleme
* Test çalıştırma
* Uygulamayı derleme

işlemleri step olarak tanımlanır.

***

### Runner

Runner, workflow işlemlerinin çalıştırıldığı ortamdır.

GitHub tarafından sağlanan hazır runner'lar kullanılabilir:

* Ubuntu
* Windows
* macOS

Ayrıca özel sunucular üzerinde self-hosted runner oluşturulabilir.

***

## Örnek GitHub Actions Workflow

Basit bir test workflow örneği:

```yaml
name: Node.js Test

on:
  push:
    branches:
      - main

jobs:
  test:

    runs-on: ubuntu-latest

    steps:
      - name: Repository Checkout
        uses: actions/checkout@v4

      - name: Node.js Kurulumu
        uses: actions/setup-node@v4

      - name: Bağımlılıkları Yükle
        run: npm install

      - name: Testleri Çalıştır
        run: npm test
```

Bu workflow:

1. Main branch'e yapılan değişikliği algılar.
2. Repository'i çalışma ortamına indirir.
3. Node.js ortamını hazırlar.
4. Bağımlılıkları yükler.
5. Testleri otomatik olarak çalıştırır.

***

## GitHub Actions Kullanım Alanları

GitHub Actions birçok farklı amaçla kullanılabilir:

### Otomatik Test

Kod değişikliklerinden sonra testlerin otomatik çalıştırılması sağlanabilir.

### Build İşlemleri

Projelerin otomatik olarak derlenmesi gerçekleştirilebilir.

### Deployment

Uygulamaların otomatik olarak sunucuya veya bulut platformlarına gönderilmesi sağlanabilir.

### Kod Kalitesi Kontrolü

Lint, güvenlik taraması ve analiz araçları çalıştırılabilir.

### Otomasyon İşlemleri

Repository yönetimi ve tekrar eden görevler otomatikleştirilebilir.

***

## GitHub Actions Avantajları

GitHub Actions kullanmanın avantajları:

* GitHub platformu ile doğrudan entegre çalışır.
* YAML dosyaları ile kolay yapılandırılabilir.
* Hazır action bileşenleri kullanılabilir.
* CI/CD süreçlerini otomatikleştirir.
* Geliştirme süreçlerini hızlandırır.
* Hataların erken tespit edilmesini sağlar.

***

## GitHub Actions ve DevOps Süreçleri

GitHub Actions, modern DevOps süreçlerinin önemli araçlarından biridir. Kod geliştirme, test, güvenlik kontrolü ve dağıtım aşamalarının otomatikleştirilmesini sağlayarak yazılım teslim süreçlerini daha hızlı ve güvenilir hâle getirir.

Özellikle ekip çalışmalarında GitHub Actions kullanımı, manuel işlemleri azaltarak daha standart ve sürdürülebilir bir geliştirme süreci oluşturur.
