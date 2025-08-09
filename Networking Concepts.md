# OSI Model ve Ağ Temelleri

OSI (Open System Interconnection) modeli, **International Organization for Standardization (ISO)** tarafından geliştirilmiş, bilgisayarların network ile iletişim kurabilmesi için teorik bir modeldir.

Aşağıda OSI modelinin katmanları ve her katmanın kısa açıklaması ile örnekleri bulunmaktadır.

---

## OSI Model Katmanları ve Açıklamaları

1. **Physical Layer (Fiziksel Katman)**  
   - Donanım ve fiziksel bağlantıların sağlandığı katmandır.  
   - Elektriksel sinyaller, kablolar, hub gibi cihazlar bu katmandadır.  
   - **Örnek:** Ethernet kablosu, Wi-Fi sinyalleri fiziksel katmanda işler.

2. **Data Link Layer (Veri Bağı Katmanı)**  
   - İki cihaz arasındaki doğrudan bağlantıyı ve veri aktarımını sağlar.  
   - Hataların tespiti ve düzeltmesi burada yapılır.  
   - **Örnek:** MAC (Media Access Control) adresleri bu katmandadır.

3. **Network Layer (Ağ Katmanı)**  
   - Verinin kaynak cihazdan hedef cihaza nasıl ulaşacağını belirler.  
   - IP adresleme ve yönlendirme (routing) bu katmanda yapılır.  
   - **Örnek:** IPv4 ve IPv6 protokolleri.

4. **Transport Layer (Taşıma Katmanı)**  
   - Uygulamalar arası veri transferinin güvenilirliğini sağlar.  
   - TCP ve UDP protokolleri bu katmandadır.  
   - **Örnek:** TCP ile bağlantı kurulması veya UDP ile düşük gecikmeli veri iletimi.

5. **Session Layer (Oturum Katmanı)**  
   - İki cihaz arasındaki oturumun kurulması, yönetimi ve sonlandırılmasından sorumludur.  
   - **Örnek:** Bir dosya transferi oturumu veya uzak masaüstü bağlantısı.

6. **Presentation Layer (Sunum Katmanı)**  
   - Verinin anlaşılır forma dönüştürülmesini sağlar.  
   - Şifreleme, sıkıştırma ve format dönüşümleri bu katmanda yapılır.  
   - **Örnek:** SSL/TLS şifrelemesi, JPEG görüntü formatı.

---

## Önemli Kavramlar

### MAC (Media Access Control) Adresi  
- Donanım tabanlı benzersiz ağ adresidir.  
- Genellikle hexadecimal sistemle gösterilir.  
- Örnek: `d4:c3:f0:85:ac:2d`  
- İlk 3 oktet üretici (vendor) bilgisi, son 3 oktet benzersiz cihaz kimliği (unique).

---

### IP Adresi  
- Ağ üzerindeki cihazları tanımlar, posta kutusu gibidir.  
- IPv4 adresi 4 oktetten oluşur, her oktet 0-255 arası değer alır.  
- Örnek: `192.168.1.1`  
- Toplamda 2^32 ≈ 4.29 milyar IPv4 adresi vardır.

#### IP Adresi Türleri ve Örnekleri:

- **Network Adresi:** Ağın kendisini belirtir, cihazlara atanmaz. Örnek: `192.168.1.0`  
- **Broadcast Adresi:** Ağdaki tüm cihazlara mesaj gönderir. Örnek: `192.168.1.255`  
- **Subnet Mask:** Ağın büyüklüğünü belirler. Örnek: `255.255.255.0`  

> Örnek IP Aralığı:  
> `192.168.1.0` - `192.168.1.255`  
> Kullanılabilir Host IP’leri: `192.168.1.1` - `192.168.1.254`

---

### Private ve Public IP Adresleri  

### Private ve Public IP Adresleri  

| Tür        | Aralıklar                      | Kullanım Amacı                  |
|------------|-------------------------------|--------------------------------|
| Private IP | 10.0.0.0 – 10.255.255.255     | Yerel ağlarda kullanılır       |
| Private IP | 172.16.0.0 – 172.31.255.255   | Yerel ağlarda kullanılır       |
| Private IP | 192.168.0.0 – 192.168.255.255 | Yerel ağlarda kullanılır       |
| Public IP  | Diğer tüm IP adresleri         | İnternet üzerinde cihazları tanımlar |


---

## UDP (User Datagram Protocol)

- **Transport Layer (Taşıma Katmanı)**'nda yer alır.  
- Bağlantısızdır, paketlerin karşı tarafa ulaşıp ulaşmadığını garanti etmez.  
- Düşük gecikmeli uygulamalar için uygundur (video, oyun, ses).  
- Paketler yolda kaybolabilir.

---

## TCP (Transmission Control Protocol)

- **Transport Layer (Taşıma Katmanı)** protokolüdür.  
- Bağlantı kurulumu yapılır (3 Yönlü El Sıkışma).  
- Gönderilen her veri baytına sıra numarası atanır (sequence number).  
- Veri kaybı veya karışıklığında yeniden gönderim sağlanır.  
- Güvenilir veri iletimi sağlar.

### TCP Bağlantı Kurulumu (Three-Way Handshake)

1. Gönderici **SYN** paketi gönderir (bağlantı isteği).  
2. Alıcı **SYN-ACK** ile yanıt verir (bağlantı kabul).  
3. Gönderici **ACK** paketi ile yanıtlar (bağlantı onayı).

---

## Port Numaraları

- IP adresi cihazı tanımlarken, port numarası cihazdaki uygulamayı tanımlar.  
- 16 bitlik sayı (0-65535 arası), 0 genellikle rezervlidir.  
- Örnek:  
  - IP: `192.168.1.10`  
  - Port: `80` (HTTP web sunucusu)  
  - Yani `192.168.1.10:80` → Web tarayıcısına bağlanır.

---

## Encapsulation (Kapsülleme)

- Veri iletişiminde, her katmanda veri üzerine katmanla ilgili başlık (header) eklenir.  
- Kaynak veriden başlayarak, veriler katman katman paketlenir ve hedefte ters işlemle çözülür.  
- Örnek:  
  - Uygulama verisi → TCP header eklenir → IP header eklenir → Ethernet frame eklenir → Fiziksel katmanda iletilir.

---

## Telnet (Teletype Network)

- Uzak bir sisteme bağlanmak için kullanılan protokol.  
- Komut satırı üzerinden metin tabanlı iletişim sağlar.  
- Güvenli olmayan bağlantılar için alternatif olarak SSH kullanılır.

---

*Bu doküman OSI modeli ve temel ağ kavramlarını özetlemekte olup, öğrenme ve referans amaçlı hazırlanmıştır.*
