# GitLab Özellikleri

GitLab, yalnızca Git repository'lerini barındıran bir platform değildir. Yazılım geliştirme yaşam döngüsünün farklı aşamalarını desteklemek amacıyla proje yönetimi, kod inceleme, otomasyon, paket yönetimi, konteyner yönetimi ve izleme gibi birçok özellik sunar.

GitLab'ın sunduğu bu özellikler sayesinde ekipler geliştirme süreçlerini tek bir platform üzerinden yönetebilir ve farklı araçlara olan ihtiyacı azaltabilir.

***

## Issues

GitLab Issues, projelerdeki görevleri, hataları ve geliştirme fikirlerini takip etmek için kullanılan proje yönetimi aracıdır.

Issues ile:

* Hata kayıtları oluşturulabilir.
* Görevler tanımlanabilir.
* Geliştirme önerileri takip edilebilir.
* Ekip üyelerine görev atanabilir.

Her issue içerisinde:

* Başlık
* Açıklama
* Etiketler (Labels)
* Sorumlu kişi (Assignee)
* Milestone bilgileri

bulunabilir.

***

## Issue Boards

Issue Boards, oluşturulan görevlerin görsel olarak takip edilmesini sağlayan Kanban tabanlı bir yönetim aracıdır.

Görevler farklı durumlara göre sınıflandırılabilir.

Örnek:

```
Open
 |
 ▼
In Progress
 |
 ▼
Testing
 |
 ▼
Closed
```

Issue Boards sayesinde ekipler geliştirme sürecinin hangi aşamada olduğunu kolayca takip edebilir.

***

## Milestones

Milestones, belirli bir hedef veya sürüm için yapılacak işlerin gruplanmasını sağlar.

Örneğin:

```
Version 1.0 Release

 ├── Login geliştirmesi
 ├── Profil sayfası
 └── Test işlemleri
```

Milestones kullanılarak:

* Sürüm planlaması yapılabilir.
* İlerleme takip edilebilir.
* Belirli hedeflere bağlı görevler yönetilebilir.

***

## Wiki

GitLab Wiki, proje dokümantasyonu oluşturmak için kullanılan bir özelliktir.

Wiki içerisinde:

* Kurulum bilgileri
* Kullanım rehberleri
* Teknik açıklamalar
* Proje dokümanları

saklanabilir.

Özellikle büyük projelerde bilgi paylaşımını kolaylaştırır.

***

## Snippets

GitLab Snippets, küçük kod parçalarının veya metin içeriklerinin paylaşılmasını sağlayan özelliktir.

Kullanım alanları:

* Kod örnekleri paylaşma
* Komut dosyaları saklama
* Yardımcı kod parçaları oluşturma

Snippets, tam bir repository oluşturmaya gerek kalmadan küçük içeriklerin yönetilmesini sağlar.

***

## Container Registry

GitLab Container Registry, Docker container image'larının saklanmasını ve yönetilmesini sağlayan özelliktir.

Bu özellik sayesinde:

* Docker image'ları GitLab içerisinde tutulabilir.
* CI/CD süreçleri ile entegre çalışabilir.
* Uygulama dağıtım süreçleri kolaylaştırılabilir.

Örnek akış:

```
Source Code

   ↓

Build

   ↓

Docker Image

   ↓

Container Registry

   ↓

Deployment
```

***

## Package Registry

GitLab Package Registry, yazılım paketlerinin saklanmasını sağlayan bir paket yönetim sistemidir.

Desteklenen paket türleri arasında:

* npm
* Maven
* NuGet
* PyPI
* Composer

gibi paket formatları bulunur.

Bu özellik sayesinde ekipler kendi özel paketlerini güvenli şekilde yönetebilir.

***

## Entegrasyonlar

GitLab birçok harici araç ile entegre çalışabilir.

Örnek entegrasyonlar:

* Slack
* Jira
* Kubernetes
* Docker
* CI/CD araçları
* İzleme sistemleri

Bu entegrasyonlar sayesinde geliştirme süreçleri farklı araçlarla birlikte yönetilebilir.

***

## Monitoring

GitLab Monitoring özellikleri, uygulamaların çalışma durumunu takip etmeye yardımcı olur.

Kullanım alanları:

* Performans takibi
* Hata analizi
* Uygulama izleme
* Sunucu durumu kontrolü

Bu özellikler sayesinde uygulama dağıtımı sonrasında sistem davranışları takip edilebilir.

***

## GitLab Features Özeti

<table data-search="false"><thead><tr><th>Özellik</th><th>Açıklama</th></tr></thead><tbody><tr><td>Issues</td><td>Hata ve görev takibi</td></tr><tr><td>Issue Boards</td><td>Görsel görev yönetimi</td></tr><tr><td>Milestones</td><td>Hedef ve sürüm planlama</td></tr><tr><td>Wiki</td><td>Dokümantasyon oluşturma</td></tr><tr><td>Snippets</td><td>Kod parçaları paylaşma</td></tr><tr><td>Container Registry</td><td>Docker image yönetimi</td></tr><tr><td>Package Registry</td><td>Paket yönetimi</td></tr><tr><td>Integrations</td><td>Harici araç bağlantıları</td></tr><tr><td>Monitoring</td><td>Sistem ve uygulama izleme</td></tr></tbody></table>

***

GitLab'ın sunduğu bu özellikler, yazılım geliştirme süreçlerini tek bir platform üzerinde yönetmeyi mümkün hâle getirir. Proje yönetimi, kod geliştirme, dağıtım ve izleme süreçlerinin aynı ortam içerisinde yürütülebilmesi GitLab'ı güçlü bir DevOps platformu yapan temel özelliklerden biridir.
