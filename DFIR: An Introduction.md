# DFIR

## DFIR Nedir?
**Açılımı Digital Forensics and Incident Response dır** _Anlam olarak dijital adli tıb ve olaya müdaheledir._

## DFIR'a Neden İhtiyaç Duyarı ?
- Saldırgan etkinliğine dair kanıt bulmak ve doğruluğunu incelemek.
- Saldırganın erişimini engellemek böylece daha fazla zarar vermesi engellenir.
- Yaşanan saldırı veya olayların zaman çizelgesini tutmak çalışma arkadaşları için önemlidir.
- Soruna yol açan açıkları bulup neler yapılabilceği hakkında düşünmek.
- Bir saldırgan gibi düşünüp oluşabilcek açıkların düzeltilmesi.
- Saldırgan hakkındaki bilgilerin toplanım kominite ile paylaşılması.

## DFIR'ın temel kavramları
- Kalıntı : Saldırganın arkasında bıraktığı kanıtlar ve kalıntılar toplanır. Tbikide suçlunun yaptığı suçu kanıtlayabilceğimiz kanıtlar toplanır.
- Kanıtların Korunması :  Kopyası alınıp onun üzerinde çalışılır ana kanıt bozulmasın diye.
- Kanıtın Takibi : Kanıtlar güvenli bir konumda saklanmalı ve herkese kanıtla çalışma izni verilmemeli üzerinde çalışan kişilerinde kaydı tutulmalıdır. İşi olmayan insanların girmesine izin verilmemeli.
- Kanıtların sırası : Bilgisayarlarda bazı depolama cihazları bilgisayar kapanınca silinceğinden ilk olarak onlara bakılmalı. Örneğin ram öncelik taşır çünkü PC kapanırsa olası bilgiler kaybedilebilir.
- Zamanlama Sırası : Saldırganın yaptığı olaylar ve bulunan kanıtların zamana göre kaydı tutulmalıdır.

## Incident Response (Olaya Müdahale) sırası
** Bazı şirketlerin standartlaştırdığı adımlar vardır. Bunların Sırası Kabaca şöyledir :  **
1. Hazırlık : Bir olay gerçekleşmeden önce,olay durumunda  hazır olunması için hazırlık gerekir. Hazırlık, olayları önlemek ve bunlara yanıt vermek için gerekli kişilere, süreçlere ve teknolojiye sahip olmayı içerir.
2. Tanımlama : Bir olay, tanımlama aşamasındaki bazı olaylar aracılığıyla tanımlanır. Bu olayların daha sonra doğruluğu araştırılır , belgelenir ve ilgili kişilere iletilir.
3. Koruma : Bu evrede saldırıdan oluşan açıklar korunmaya çalışılır engellenir veya daha az zarar görmek için hot fix atılır veya tamamen durdurulur.
4. Düzeltme/Kaldırma : Ardından, tehdit yok edilir. önce uygun bir  analizin yapılması ve tehdidin etkin bir şekilde kontrol altına alınması sağlanmalıdır. Örneğin, tehditin ağa giriş noktası takılı değilse, tehdit etkin bir şekilde ortadan kaldırılmayacak ve tekrar bir dayanak kazanabilecektir.
5. Kurtarma: Tehdit ağdan kaldırıldıktan sonra, kesintiye uğrayan hizmetler olay gerçekleşmeden önceki gibi geri getirilir.
6. Öğrenilen Dersler: Son olarak, olayın gözden geçirilmesi gerçekleştirilir, olay belgelenir ve ekibin bir sonraki benzer olaya nasıl karşılık vericeği çalışılır , kararlaştırılır.


