# N8N Günlük Piyasa Takip Otomasyonu 🚀

Bu proje, n8n (Workflow Automation) kullanılarak geliştirilmiş otonom bir finansal veri takip botudur. Herhangi bir manuel müdahale gerektirmeden finansal verileri çeker, işler ve raporlar.

## 📌 Özellikler ve İş Akışı (Workflow)
1. **Schedule Trigger:** Sistem her sabah saat 09:00'da otomatik olarak tetiklenir.
2. **REST API Entegrasyonu:** `HTTP Request` node'u ile CoinGecko API'sine GET isteği atılarak güncel piyasa verileri çekilir.
3. **Veri Manipülasyonu:** Gelen karmaşık JSON verisi, `Code Node` içerisinde **JavaScript** kullanılarak parse edilir ve sadece ihtiyaç duyulan veriler ayıklanır.
4. **Bildirim Sistemi:** Temizlenen veri, Telegram Bot API üzerinden kullanıcıya dinamik bir mesaj olarak gönderilir.

## 🛠 Kullanılan Teknolojiler
- **n8n** (Node-based Automation)
- **JavaScript**
- **JSON & RESTful API'ler**

## 🚀 Kurulum ve Kullanım
1. n8n'i bilgisayarınızda (Docker/npm) veya bulutta çalıştırın.
2. Bu repository'deki `workflow.json` dosyasını indirin.
3. n8n arayüzünde sağ üst köşeden **Import from File** seçeneğine tıklayarak dosyayı içeri aktarın.
4. `Telegram'a Gonder` isimli düğüme (node) çift tıklayarak kendi Telegram Bot Token'ınızı ve Chat ID'nizi ekleyin.