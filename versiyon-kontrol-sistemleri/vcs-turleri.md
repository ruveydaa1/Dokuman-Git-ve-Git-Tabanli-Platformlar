# VCS Türleri

Versiyon kontrol sistemleri, dosyaların nasıl saklandığı ve geliştiriciler arasında nasıl paylaşıldığına göre farklı türlere ayrılmaktadır. Genel olarak versiyon kontrol sistemleri **Yerel (Local)**, **Merkezi (Centralized)** ve **Dağıtık (Distributed)** olmak üzere üç temel kategori altında incelenmektedir.

### Local Version Control System (LVCS)

Yerel Versiyon Kontrol Sistemi (Local Version Control System - LVCS), dosyaların sürüm geçmişini yalnızca kullanıcının kendi bilgisayarında saklayan en temel versiyon kontrol sistemidir. Tüm değişiklikler tek bir bilgisayar üzerinde tutulduğu için internet bağlantısına ihtiyaç duyulmaz.

Bu yaklaşım küçük ve bireysel projeler için yeterli olabilse de ekip çalışmasına uygun değildir. Ayrıca verilerin yalnızca tek bir cihazda bulunması nedeniyle donanım arızaları veya veri kayıpları durumunda proje geçmişinin tamamen kaybedilme riski bulunmaktadır.

#### Avantajları

* Kurulumu ve kullanımı oldukça basittir.
* İnternet bağlantısı gerektirmez.
* Küçük ve bireysel projeler için uygundur.

#### Dezavantajları

* Ekip çalışmasını desteklemez.
* Değişiklikler yalnızca tek bilgisayarda saklanır.
* Veri kaybı riski yüksektir.

***

### Centralized Version Control System (CVCS)

Merkezi Versiyon Kontrol Sistemi (Centralized Version Control System - CVCS), tüm proje dosyalarının merkezi bir sunucuda tutulduğu yapıdır. Geliştiriciler projeye doğrudan bu merkezi sunucu üzerinden erişir ve yaptıkları değişiklikleri sunucuya gönderir.

Bu yaklaşım ekip çalışmasını kolaylaştırsa da sistem tamamen merkezi sunucuya bağımlıdır. Sunucunun erişilemez hale gelmesi veya arızalanması durumunda geliştiriciler çalışmaya devam etmekte zorlanabilir.

**SVN (Apache Subversion)** ve **Perforce** merkezi versiyon kontrol sistemlerine örnek olarak gösterilebilir.

#### Avantajları

* Ekip çalışmasını destekler.
* Tüm proje tek bir merkezden yönetilir.
* Kullanıcı yetkilendirmesi ve erişim kontrolü kolaydır.

#### Dezavantajları

* Merkezi sunucuya bağımlıdır.
* Sunucu kesintilerinde çalışma süreci aksayabilir.
* Tam geçmişe erişim için sunucu bağlantısı gerekir.

***

### Distributed Version Control System (DVCS)

Dağıtık Versiyon Kontrol Sistemi (Distributed Version Control System - DVCS), her geliştiricinin projenin tam bir kopyasına sahip olduğu versiyon kontrol modelidir. Kullanıcılar yalnızca dosyaları değil, tüm sürüm geçmişini de kendi bilgisayarlarında saklar.

Bu yapı sayesinde geliştiriciler internet bağlantısı olmadan da commit oluşturabilir, branch işlemleri gerçekleştirebilir ve proje geçmişine erişebilir. Yapılan değişiklikler daha sonra uzak depoya (Remote Repository) gönderilerek diğer ekip üyeleriyle paylaşılır.

**Git**, günümüzde en yaygın kullanılan dağıtık versiyon kontrol sistemidir. GitHub, GitLab ve GitBucket gibi platformlar ise Git tabanlı uzak depo yönetimi ve ekip çalışması hizmetleri sunmaktadır.

#### Avantajları

* Her kullanıcı projenin tam bir kopyasına sahiptir.
* İnternet bağlantısı olmadan çalışılabilir.
* Veri kaybı riski oldukça düşüktür.
* Branch ve merge işlemleri hızlıdır.
* Büyük ekipler için yüksek performans sunar.

#### Dezavantajları

* İlk öğrenme süreci diğer modellere göre daha karmaşık olabilir.
* Tüm proje geçmişi yerel bilgisayarda tutulduğu için daha fazla depolama alanı kullanabilir.

***

### VCS Türlerinin Karşılaştırılması

| Özellik             | LVCS        | CVCS                  | DVCS                     |
| ------------------- | ----------- | --------------------- | ------------------------ |
| Çalışma Yapısı      | Yerel       | Merkezi Sunucu        | Dağıtık                  |
| İnternet Bağlantısı | Gerekmez    | Genellikle Gereklidir | Gerekmeden çalışılabilir |
| Ekip Çalışması      | Desteklemez | Destekler             | Destekler                |
| Veri Kaybı Riski    | Yüksek      | Orta                  | Düşük                    |
| Performans          | Orta        | Sunucuya bağlı        | Yüksek                   |
| Örnek Sistemler     | RCS         | SVN, Perforce         | Git                      |

Dağıtık versiyon kontrol sistemleri sundukları esneklik, performans ve güvenilirlik sayesinde günümüzde yazılım geliştirme projelerinde en yaygın kullanılan yaklaşım haline gelmiştir. Özellikle Git, güçlü branch yapısı, hızlı çalışma prensibi ve geniş ekosistemi sayesinde bireysel geliştiricilerden büyük ölçekli yazılım ekiplerine kadar geniş bir kullanıcı kitlesi tarafından tercih edilmektedir.
