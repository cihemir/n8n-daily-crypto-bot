#  N8n Günlük Kripto ve Piyasa Takip Botu

Bu proje, **n8n (Workflow Automation)** aracı kullanılarak geliştirilmiş otonom bir veri çekme ve bildirim otomasyonudur. 
Sistem her sabah belirlenen saatte tetiklenir, dış bir finans API'sine bağlanır, gelen veriyi işler ve kullanıcıya Telegram üzerinden  bir rapor sunar.

##  Kullanılan Teknolojiler
- **n8n:** Görsel iş akışı tasarımı ve zamanlama (Cron jobs)
- **JavaScript:** Gelen veriyi parse etme ve metin manipülasyonu
- **RESTful API:** CoinGecko üzerinden GET request ile anlık veri çekimi
- **JSON:** Veri transferi ve yapılandırma
- **Telegram Bot API:** Kullanıcıya anlık push bildirim gönderimi

##  Nasıl Çalışır?
1. **Schedule Trigger:** Sistem her sabah 09:00'da (veya istenilen saatte) otonom olarak çalışmaya başlar.
2. **HTTP Request:** CoinGecko API'sine bağlanılarak anlık Bitcoin ve Ethereum fiyatları JSON formatında çekilir.
3. **Code Node (JavaScript):** Gelen karmaşık JSON verisi filtrelenir ve sadece ihtiyaç duyulan fiyat bilgileri değişkene atanarak okunabilir bir string (metin) şablonuna dönüştürülür.
4. **Telegram Integration:** Çıkan nihai metin, Telegram botu aracılığıyla kullanıcının şahsi ID'sine gönderilir.

