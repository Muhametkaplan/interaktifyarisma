🎓 Kampüs Etkinlik Platformu

Üniversite toplulukları, kulüpler, sınıflar ve etkinlikler için geliştirilmiş; gerçek zamanlı (real-time), interaktif ve mobil uyumlu web tabanlı bir etkinlik yönetim platformudur. Öğretmenler ve moderatörler dev ekranda etkinlikleri yönetirken, öğrenciler hiçbir uygulama indirmeden sadece bir PIN kodu ile telefonlarından anında katılabilirler.

🚀 İçerisindeki Modüller (Araçlar)

Bu platform, tek bir ana menü (Hub) üzerinden 6 farklı interaktif araca erişim sağlar:

1. 🧠 Bilgi Yarışması (Kahoot Clone)

Gerçek zamanlı bilgi yarışmaları düzenleyin. Öğretmenler kendi Google hesaplarıyla giriş yaparak özel soru paketleri oluşturur. Öğrenciler süreye karşı yarışır, doğru cevaplar anlık olarak dev ekranda bar grafikleriyle gösterilir ve oyun sonunda podyum belirir.

Yönetici: yarisma-admin.html

Öğrenci: yarisma.html

2. 📊 Canlı Anket & Oylama (Live Polls)

Topluluk kararları veya ders içi geri bildirimler için anlık anketler oluşturun. Katılımcılar telefonlarından oy verdikçe, sonuçlar ana ekranda orantılı bar grafikleriyle büyür.

Yönetici: anket-admin.html

Katılımcı: anket.html

3. ❓ Anonim Soru-Cevap Tahtası (Q&A Board)

Katılımcılar anonim olarak soru sorar ve başkalarının sorularını beğenebilir (Upvote). En çok beğeni alan sorular dev ekranda en üste çıkar.

Yönetici: qa-admin.html

Katılımcı: qa.html

4. 👥 Rastgele Takım Kurucu (Team Generator)

İsim listesini yapıştırın ve kaç takım istediğinizi seçin. Sistem, herkesi adil olarak renkli takımlara böler.

Araç: takim-kurucu.html

5. 🎡 Çarkıfelek (Spin the Wheel)

Eğlenceli etkinlikler ve rastgele seçimler için isim listesini girip çarkı çevirin.

Araç: carkifelek.html

6. 🎁 Çekiliş Aracı (Raffle Tool)

Asil ve yedek talihlilerinizi şeffaf ve animasyonlu bir şekilde belirleyin.

Araç: cekilis.html

🛠️ Kullanılan Teknolojiler

Frontend: HTML5, Vanilla JavaScript, CSS3

Stil: Tailwind CSS

Backend: Firebase (Firestore & Auth)

📂 Dosya Yapısı

📁 kampus-etkinlik-platformu

├── index.html            # Ana Menü (Giriş Ekranı)

├── yarisma-admin.html    # Bilgi Yarışması Yönetici

├── yarisma.html          # Bilgi Yarışması Öğrenci

├── anket-admin.html      # Canlı Anket Yönetici

├── anket.html            # Canlı Anket Katılımcı

├── qa-admin.html         # Soru-Cevap Yönetici

├── qa.html               # Soru-Cevap Öğrenci

├── takim-kurucu.html     # Takım Dağıtıcı

├── carkifelek.html       # Çarkıfelek

└── cekilis.html          # Çekiliş Aracı


🛡️ Güvenlik ve Veri Gizliliği

Yöneticiler Google Authentication ile giriş yapar.

Öğrenciler tamamen Anonim olarak bağlanır.

Soru paketleri her kullanıcının kendi UID'sine özel saklanır.
