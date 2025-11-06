Kütüphane Kitap Takip Sistemi / Library Book Tracking System
📚 Proje Tanımı | Project Description

Bu proje, basit bir Kütüphane Kitap Takip Sistemi uygulamasıdır.
Kullanıcı, kitapları bir ComboBox üzerinden seçebilir ve "Ödünç Al" veya "Teslim Et" butonlarını kullanarak kitapların durumunu değiştirebilir.
Uygulama, kitapların mevcut olup olmadığını görüntüler ve tüm bilgiler modelde saklanır.

This project is a simple Library Book Tracking System.
Users can select a book from a ComboBox, borrow or return it using the corresponding buttons, and view the current status of each book in a text area.
All book information and states are managed through a separate model class.

🧩 Sınıf Yapısı | Class Structure
1. LibraryModel

Kitap listesini ve durumlarını (true = ödünçte, false = müsait) tutar.

Kitap ödünç alma ve teslim etme işlemlerini yönetir.

Veriler bir HashMap<String, Boolean> içinde saklanır.

Main functions:

isAvailable(String kitapAdi) → Checks if the book is available.

oduncAl(String kitapAdi) → Marks a book as borrowed.

teslimEt(String kitapAdi) → Marks a book as returned.

2. LibraryApp

Swing GUI bileşenlerini içerir: JComboBox, JButton, JTextArea.

Kullanıcı etkileşimini yönetir ve LibraryModel ile bağlantı kurar.

"Ödünç Al" ve "Teslim Et" butonlarına tıklanınca kitap durumu güncellenir.

GUI Components:

JComboBox → Kitap seçimi

JButton → İşlemler ("Ödünç Al", "Teslim Et")

JTextArea → Kitap durumu ve mesajlar

⚙️ Nasıl Çalışır | How It Works

Program başlatıldığında kullanıcı kitap listesinden seçim yapar.

Kullanıcı “Ödünç Al” butonuna basarsa:

Eğer kitap müsaitse ödünç alınır.

Eğer zaten ödünçteyse uyarı mesajı gösterilir.

Kullanıcı “Teslim Et” butonuna basarsa:

Eğer kitap ödünçteyse teslim edilir.

Eğer zaten teslim edilmişse bilgi mesajı gösterilir.

Her işlem JTextArea içinde görüntülenir.

💻 Kullanım | Usage Instructions
🔧 Derleme (Compile)
javac LibraryModel.java LibraryApp.java

▶️ Çalıştırma (Run)
java LibraryApp


Eğer paket (package) kullandıysan:

javac p/LibraryModel.java p/LibraryApp.java
java p.LibraryApp

🧱 Örnek Ekran Görüntüsü | Example Screenshot
Kitap Seç: [1984 ▼]  [Ödünç Al] [Teslim Et]

> 1984 ödünç alındı.
> Suç ve Ceza zaten ödünçte.
> Sefiller teslim edildi.

📦 Teknolojiler | Technologies Used

Java SE 17+

Swing (javax.swing)

AWT (java.awt)

Collections (HashMap)

🧑‍💻 Geliştirici | Developer

Ad: Safia Ashraf
Üniversite: İstanbul Gelişim Üniversitesi
Bölüm: Yazılım Mühendisliği
Proje: B Grubu – Lab 3: Kütüphane Kitap Takip Sistemi

🌟 Notlar | Notes

Tüm kitaplar başlangıçta müsait (false) durumundadır.

Kullanıcı arayüzü sade ve anlaşılır olacak şekilde tasarlanmıştır.

statusArea bileşeni sadece bilgi gösterir, düzenlenemez.

Kod iki sınıfa ayrılmıştır: model (veri kısmı) ve app (arayüz kısmı).
