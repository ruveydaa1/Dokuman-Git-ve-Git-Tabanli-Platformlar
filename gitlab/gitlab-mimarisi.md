# GitLab Mimarisi

GitLab mimarisi, Git versiyon kontrol sistemi üzerine kurulmuş ve yazılım geliştirme yaşam döngüsünü destekleyecek şekilde tasarlanmış bir yapıya sahiptir. GitLab; repository yönetimi, ekip çalışması, CI/CD süreçleri, güvenlik analizleri ve proje yönetimi özelliklerini tek bir platform içerisinde birleştirir.

GitLab'ın temel çalışma yapısı; **Instance**, **Group**, **Project**, **Repository**, **Branch**, **Merge Request** ve **Runner** bileşenleri üzerine kuruludur.

***

## GitLab Instance

GitLab Instance, GitLab platformunun çalıştığı ana sistem yapısını ifade eder.

Bir GitLab instance içerisinde:

* Kullanıcılar,
* Gruplar,
* Projeler,
* Repository'ler,
* Ayarlar

bulunur.

GitLab iki farklı şekilde kullanılabilir:

#### GitLab.com

GitLab tarafından sunulan bulut tabanlı hizmettir. Kullanıcılar doğrudan GitLab sunucuları üzerinden projelerini yönetebilir.

#### Self-Managed GitLab

GitLab'ın kurumların kendi sunucularına kurulabildiği versiyondur.

Bu yapı sayesinde kurumlar:

* Verilerini kendi altyapılarında tutabilir.
* Güvenlik politikalarını kendileri belirleyebilir.
* Sistem yönetimini kontrol edebilir.

***

## Group Yapısı

GitLab'da projeler doğrudan kullanıcı altında bulunabileceği gibi **Group** yapıları içerisinde de yönetilebilir.

Group, birden fazla projenin ortak şekilde yönetilmesini sağlayan yapıdır.

Group içerisinde:

* Projeler,
* Kullanıcı izinleri,
* Roller,
* Ayarlar

yönetilebilir.

Örnek:

```
Company Group

 ├── Web Application Project
 │
 ├── Mobile Application Project
 │
 └── Backend Service Project
```

Bu yapı özellikle büyük ekiplerde proje organizasyonunu kolaylaştırır.

***

## Project

GitLab'da her yazılım çalışması bir **Project** olarak adlandırılır.

Project içerisinde:

* Kaynak kodlar,
* Repository,
* Branch'ler,
* Commit geçmişi,
* Issues,
* Merge Request'ler,
* CI/CD yapılandırmaları

bulunur.

GitHub'daki repository kavramına benzer bir yapıdır.

***

## Repository Yapısı

GitLab repository yapısı Git'in temel çalışma mantığını kullanır.

Repository içerisinde:

* Dosyalar,
* Commit geçmişi,
* Branch'ler,
* Tag'ler

saklanır.

Geliştiriciler değişikliklerini local ortamda yaparak GitLab üzerindeki uzak repository'ye gönderir.

Genel akış:

```
Local Repository

        |
        | git push
        ▼

GitLab Repository

        |
        | git pull
        ▼

Local Repository
```

***

## Branch Yapısı

GitLab projelerinde branch'ler farklı geliştirme süreçlerini yönetmek için kullanılır.

Örnek:

```
main
 |
 ├── feature-login
 |
 ├── feature-payment
 |
 └── bugfix-error
```

Geliştiriciler kendi branch'lerinde çalışır ve tamamlanan değişiklikleri Merge Request aracılığıyla hedef branch'e gönderir.

***

## Merge Request Yapısı

GitLab'da ekip çalışmaları genellikle Merge Request süreci üzerinden gerçekleştirilir.

Merge Request:

* Kod değişikliklerinin incelenmesini,
* Tartışılmasını,
* Onaylanmasını,
* Birleştirilmesini

sağlar.

Akış:

```
Developer Branch

        |
        ▼

Merge Request

        |
        ▼

Code Review

        |
        ▼

Merge

        |
        ▼

Main Branch
```

***

## GitLab Runner

GitLab Runner, CI/CD pipeline işlemlerini çalıştıran bileşendir.

Runner sayesinde:

* Testler çalıştırılır.
* Kod derlenir.
* Uygulamalar dağıtılır.
* Otomasyon görevleri gerçekleştirilir.

Runner türleri:

#### Shared Runner

GitLab tarafından sağlanan ve birden fazla proje tarafından kullanılabilen runner'lardır.

#### Specific Runner

Belirli bir proje veya grup için özel olarak yapılandırılan runner'lardır.

#### Group Runner

Bir grup içerisindeki tüm projeler tarafından kullanılabilen runner'lardır.

***

## GitLab CI/CD Pipeline Yapısı

GitLab mimarisinin önemli parçalarından biri CI/CD pipeline yapısıdır.

Pipeline temel olarak:

```
Commit

  ↓

Build

  ↓

Test

  ↓

Deploy
```

aşamalarından oluşabilir.

Bu süreçler `.gitlab-ci.yml` dosyası içerisinde tanımlanır.

***

## GitLab Temel Bileşenleri

<table data-search="false"><thead><tr><th>Bileşen</th><th>Açıklama</th></tr></thead><tbody><tr><td>Instance</td><td>GitLab sisteminin genel yapısı</td></tr><tr><td>Group</td><td>Proje gruplarının yönetildiği alan</td></tr><tr><td>Project</td><td>Yazılım projesi alanı</td></tr><tr><td>Repository</td><td>Kaynak kodların tutulduğu alan</td></tr><tr><td>Branch</td><td>Bağımsız geliştirme alanı</td></tr><tr><td>Merge Request</td><td>Kod inceleme ve birleştirme süreci</td></tr><tr><td>Runner</td><td>CI/CD işlemlerini çalıştıran yapı</td></tr><tr><td>Pipeline</td><td>Otomasyon süreçleri</td></tr></tbody></table>

***

GitLab mimarisi, Git'in temel versiyon kontrol özelliklerini DevOps süreçleriyle birleştiren kapsamlı bir yapı sunar. Group ve Project organizasyonu, Merge Request süreçleri ve yerleşik CI/CD desteği sayesinde özellikle ekip tabanlı ve kurumsal yazılım geliştirme süreçlerinde güçlü bir platform olarak kullanılmaktadır.
