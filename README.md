Metro Ağ Sistemi (MetroAgi) - README
Proje Açıklaması
Bu proje, bir şehirdeki metro hattındaki istasyonlar arasındaki rotaları bulmak için tasarlanmış bir MetroAgi (Metro Ağ Sistemi) simülasyonudur. Kullanıcı, belirli istasyonlar arasında iki temel şekilde rota arayabilir:

En Az Aktarmalı Rota (BFS Algoritması): Başlangıç istasyonundan hedef istasyonuna ulaşmak için en az aktarma yapılan rotayı bulur.

En Hızlı Rota (A Algoritması):* Başlangıç istasyonundan hedef istasyonuna en hızlı şekilde ulaşan rotayı, toplam süreyi (dakika) ile birlikte bulur.

Sınıflar ve Metodlar
Istasyon Sınıfı
Atributlar:

idx: İstasyonun benzersiz kimliği (string).

ad: İstasyonun adı (string).

hat: İstasyonun ait olduğu hattın adı (string).

komsular: Komşu istasyonları ve aralarındaki seyahat süresini tutan liste.

Metodlar:

komsu_ekle: Bir istasyonu komşu olarak ekler.

__lt__: İstasyonları sıralamak için kullanılır (istasyon id'sine göre).

MetroAgi Sınıfı
Atributlar:

istasyonlar: İstasyonları, id'lerine göre saklayan bir sözlük.

hatlar: Hattaki istasyonları tutan bir sözlük.

Metodlar:

istasyon_ekle: Yeni bir istasyon ekler.

baglanti_ekle: İki istasyon arasındaki bağlantıyı ve süreyi ekler.

en_az_aktarma_bul: BFS algoritmasını kullanarak en az aktarmalı rotayı bulur.

en_hizli_rota_bul: A* algoritmasını kullanarak en hızlı rotayı bulur.

Kullanım Örneği
Metro ağını oluşturmak ve test senaryolarını çalıştırmak için aşağıdaki adımlar takip edilebilir:

İstasyonlar ve Bağlantılar Ekleyin:

istasyon_ekle metodu ile istasyonları ve hangi hatta ait olduklarını ekleyebilirsiniz.

baglanti_ekle metodu ile istasyonlar arasında seyahat sürelerini ekleyebilirsiniz.

En Az Aktarmalı Rota Bulma:

en_az_aktarma_bul metodu ile iki istasyon arasındaki en az aktarmalı rotayı bulabilirsiniz.

En Hızlı Rota Bulma:

en_hizli_rota_bul metodu ile iki istasyon arasındaki en hızlı rotayı ve toplam süreyi öğrenebilirsiniz.

Test Senaryoları
Aşağıda bazı test senaryoları verilmiştir:

AŞTİ'den OSB'ye: Hem en az aktarmalı rota hem de en hızlı rota hesaplanmaktadır.

Batıkent'ten Keçiören'e: Yine her iki rota türü için hesaplamalar yapılır.

Keçiören'den AŞTİ'ye: Bu senaryo ile de her iki rota türü denenebilir.
