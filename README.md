#🎓 Kampüs Etkinlik Platformu

Üniversite toplulukları, kulüpler, sınıflar ve etkinlikler için geliştirilmiş; gerçek zamanlı (real-time), interaktif ve mobil uyumlu web tabanlı bir etkinlik yönetim platformudur. Öğretmenler ve moderatörler dev ekranda etkinlikleri yönetirken, öğrenciler hiçbir uygulama indirmeden sadece bir PIN kodu ile telefonlarından anında katılabilirler.

🚀 İçerisindeki Modüller (Araçlar)

Bu platform, tek bir ana menü (Hub) üzerinden 6 farklı interaktif araca erişim sağlar:

1. 🧠 Bilgi Yarışması (Kahoot Clone)

Gerçek zamanlı bilgi yarışmaları düzenleyin. Öğretmenler kendi Google hesaplarıyla giriş yaparak özel soru paketleri oluşturur. Öğrenciler süreye karşı yarışır, doğru cevaplar anlık olarak dev ekranda bar grafikleriyle gösterilir ve oyun sonunda podyum belirir.

Yönetici: admin.html

Öğrenci: yarisma.html

2. 📊 Canlı Anket & Oylama (Live Polls)

Topluluk kararları veya ders içi geri bildirimler için anlık anketler oluşturun. Katılımcılar telefonlarından oy verdikçe, sonuçlar ana ekranda orantılı bar grafikleriyle (canlı animasyonlarla) büyür.

Yönetici: anket-admin.html

Katılımcı: anket.html

3. ❓ Anonim Soru-Cevap Tahtası (Q&A Board)

Kalabalık seminerler veya dersler için idealdir. Katılımcılar anonim olarak soru sorar ve başkalarının sorularını beğenebilir (Upvote). En çok beğeni alan sorular dev ekranda en üste çıkar.

Yönetici: qa-admin.html

Katılımcı: qa.html

4. 👥 Rastgele Takım Kurucu (Team Generator)

Projeler, hackathonlar veya münazaralar için isim listesini yapıştırın ve kaç takım istediğinizi seçin. Sistem, animasyonlu bir şekilde herkesi adil olarak renkli takımlara böler. (Veritabanı gerektirmez, anında çalışır).

Araç: takim-kurucu.html

5. 🎡 Çarkıfelek (Spin the Wheel)

Eğlenceli etkinlikler, rastgele seçimler veya hediye dağıtımı için isim listesini girip çarkı çevirin. Seçilen kişiyi "Listeden Çıkar" seçeneğiyle eleyerek devam edebilirsiniz.

Araç: carkifelek.html

6. 🎁 Çekiliş Aracı (Raffle Tool)

Asil ve yedek talihlilerinizi şeffaf bir şekilde belirleyin. Listeyi yapıştırın, asil/yedek sayısını girin ve konfetiler eşliğinde çekilişi tamamlayın.

Araç: cekilis.html

🛠️ Kullanılan Teknolojiler

Frontend (Arayüz): HTML5, Vanilla JavaScript, CSS3

Stil Kütüphanesi: Tailwind CSS (CDN üzerinden)

Backend & Veritabanı: Firebase (Firestore Database)

Kimlik Doğrulama: Firebase Authentication (Google Sign-In ve Anonim Giriş)

İkonlar: SVG formatında inline ikonlar (Lucide & Custom)

⚙️ Kurulum ve Dağıtım (Deployment)

Bu proje doğrudan tarayıcı üzerinde (Statik HTML/JS olarak) çalışır. Node.js veya sunucu kurulumuna ihtiyaç yoktur. Ancak Firebase servislerinin çalışması için kendi Firebase projenizi bağlamanız gereklidir.

1. Firebase Ayarları

Firebase Console üzerinden yeni bir proje oluşturun.

Firestore Database oluşturun ve güvenlik kurallarını (Rules) uygun şekilde ayarlayın.

Authentication sekmesinden Google ve Anonymous (Anonim) giriş yöntemlerini aktif edin.

Settings > Authorized Domains kısmına projenizi yayınlayacağınız alan adını (örn: username.github.io) ekleyin.

2. Projeyi Klonlama ve Ayarlama

git clone [https://github.com/KULLANICI_ADINIZ/kampus-etkinlik-platformu.git](https://github.com/KULLANICI_ADINIZ/kampus-etkinlik-platformu.git)


Her bir HTML dosyasının <script type="module"> etiketi içerisindeki firebaseConfig değişkenini kendi Firebase proje ayarlarınızla değiştirin.

3. Yayınlama (Hosting)

Proje klasörünü doğrudan GitHub Pages, Vercel veya Netlify üzerinden ücretsiz yayınlayabilirsiniz. Sadece index.html dosyasının ana dizinde olduğundan emin olun.

📂 Dosya Yapısı

📁 kampus-etkinlik-platformu
├── index.html          # Ana Menü (Tüm araçlara yönlendirme ve Google Login)

├── admin.html          # Bilgi Yarışması (Yönetici Paneli)

├── yarisma.html        # Bilgi Yarışması (Öğrenci / Katılımcı Arayüzü)

├── anket-admin.html    # Canlı Anket (Yönetici Paneli)

├── anket.html          # Canlı Anket (Katılımcı Arayüzü)

├── qa-admin.html       # Soru-Cevap (Yönetici / Projeksiyon Ekranı)

├── qa.html             # Soru-Cevap (Öğrenci Soru Sorma Ekranı)

├── takim-kurucu.html   # Rastgele Takım Dağıtıcı

├── carkifelek.html     # Çarkıfelek Uygulaması

└── cekilis.html        # Animasyonlu Çekiliş Aracı


🛡️ Güvenlik ve Veri Gizliliği

Yöneticiler sisteme Google Authentication ile girer.

Öğrenciler kişisel veri (e-posta vb.) paylaşmadan, tamamen Anonim (Anonymous Auth) olarak Firebase'e bağlanır.

Her öğretmenin kendi yarışma ve soru paketleri Firebase üzerinde o kişinin UID'sine özel (Private) bir koleksiyonda (users/{uid}/...) şifreli olarak saklanır.
