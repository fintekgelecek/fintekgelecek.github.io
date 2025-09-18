# Türkiye Uyarlaması – Regülasyon, KVKK ve Etik Çerçeve

Finansal kurumlarda yapay zekâ, veri analitiği ve otomasyon çözümlerinin devreye alınması, yalnızca teknik uyumlulukla değil; aynı zamanda düzenleyici kurumların (**BDDK, KVKK, TBB**) çizdiği çerçeve ve etik ilkelerle de yakından ilişkilidir. Bu nedenle, aşağıda yer alan başlıklar farklı düzenlemelerden türetilmiş temel uyum noktalarını özetlemektedir. Her bir madde, hem ilgili mevzuata atıf yapar hem de günlük işleyişe nasıl yansıdığını sade bir dille açıklamaya çalışır.

---

## 1. Açık Bankacılık ve Ekosistem
- **Açık Bankacılık Uyum:** BDDK’nın PSD2 benzeri düzenlemeleri gereği, üçüncü taraf entegrasyonları denetim altında olmalı; güvenlik ve şeffaflık ihmal edilmemelidir.  
- **Geliştirici Denetimi:** Banka dışı geliştirici ekosistemine açılan API’ler için kimlik doğrulama, erişim yetkisi ve denetim süreçleri net şekilde tanımlanmalıdır.  
- **Şeffaf Sözleşmeler:** Değişken koşullu ürünlerde müşteriye tüm senaryoların önceden açıkça bildirilmesi, sözleşmelerin şeffaf tutulması gerekir.  

---

## 2. BDDK – Bankaların Bilgi Sistemleri ve Elektronik Bankacılık Hizmetleri Yönetmeliği (RG: 15.03.2020 / 31069)
- **Amaç Bazlı Kullanım:** Müşteri verisi yalnızca belirlenen amaçla kullanılmalı; tüm işlemler denetim iziyle kayıt altına alınmalıdır.  
- **Davranışsal ve Lokasyon Verileri:** Bu veriler Türkiye içinde işlenmeli; yurtdışına aktarım için SLA, denetim izi ve veri sınırlaması şarttır.  
- **Dış Hizmet Alımı:** Bulut ya da üçüncü taraf hizmetlerde sözleşme, SLA ve denetim izi yükümlülüğü aranır.  
- **Kritik Karar Süreçleri:** Kredi tahsisi, yatırım yönlendirmesi gibi otomatikleşen süreçlerde nihai sorumluluk bankadadır; *human-in-the-loop* noktaları zorunludur.  
- **Mikrobankacılık ve Orkestrasyon:** Müşteri profili ve niyet motoru gibi bileşenler yalnızca Türkiye içi ya da hibrit bulut ortamlarında çalıştırılmalıdır.  
- **Sistem Değişiklikleri:** Bilgi sistemlerinde yapılan her değişiklik için denetim izi tutulmalı, şeffaf raporlama yapılmalıdır.  
- **Veri Yerelliği:** Tüm müşteri ve finansal verilerin Türkiye içinde işlenmesi ve saklanması esastır.  

---

## 3. Çalışan Verisi ve İK Uyumu
- **Kamera ve Gözetim:** Çalışan verileri bireysel kimlik üzerinden değil, anonimleştirilmiş ve süreç odaklı biçimde işlenmelidir.  
- **Kültürel Adaptasyon:** Türkiye’de mobil-first, mikro öğrenme ve hiyerarşik kurumlara uygun dijital mentorluk modelleri ön plandadır.  
- **Performans ve Analitik:** Çalışan verileri yalnızca gelişim amaçlı kullanılmalı; performans cezası veya ödül mekanizması için doğrudan işlenmemelidir.  
- **Sendika / İş Kanunu Uyumu:** İş tanımları, sözleşmeler ve dönüşüm süreçleri sendika yükümlülükleriyle uyumlu kurgulanmalıdır.  
- **Şeffaflık:** Çalışanların kendi skorlarına erişebilmesi ve gelişim önerileri alabilmesi, güven duygusu açısından kritik rol oynar.  

---

## 4. Etik İlkeler
- **Adillik:** Arketip veya davranış etiketleri müşteriye karşı ayrımcılığa yol açmamalı; objektiflik korunmalıdır.  
- **Explainability (Açıklanabilirlik):** Yapay zekâ kararları ve algoritmik öneriler müşteriye anlaşılır biçimde açıklanmalıdır.  
- **İnsan-in-the-Loop (HITL):** Özellikle kritik finansal kararlarda otomatik süreçlerin yanında insana bırakılacak kontrol noktaları bulunmalıdır.  
- **Manipülasyondan Kaçınma:** Nudging ve sessiz uyarılar, bilgilendirme amaçlı kullanılmalı; yönlendirici veya manipülatif tasarımlardan uzak durulmalıdır.  
- **Şeffaf Fayda:** Müşteri verisini paylaştığında elde edeceği fayda açık biçimde tanımlanmalı, bu fayda kayıt altına alınmalıdır.  

---

## 5. Kurum Kültürü ve İşleyiş
- **Bilgi Akışı:** Kişisel ilişkilere dayalı bilgi akışının kaybolmaması için kurumsal hafıza mekanizmaları (ör. why-graph) devreye alınmalıdır.  
- **Hackathon ve İnovasyon:** Türkiye’de kısa süreli hackathon etkinlikleri yaygın olsa da, sürdürülebilir fikir toplama sistemleriyle bu kültür kalıcı hale getirilmelidir.  
- **Şube Gerçekliği:** Türkiye’de şubeler hâlâ müşteriyle kritik temas noktasıdır; hibrit fonksiyonlar bu gerçekliği bozmadan esneklik sağlamalıdır.  
- **Toplantı ve Stres Yönetimi:** Yoğun toplantı ve e-posta trafiğinde çalışanlarda stresin erken tespiti, tükenmişliği önlemek için önemlidir.  

---

## 6. KVKK – Kişisel Verilerin Korunması Kanunu
- **Madde 9 – Yurt dışına aktarım:** Yurtdışına aktarım için ilgili kişinin açık rızası veya Kişisel Verileri Koruma Kurulu’nun izni gerekir.  
- **Amaç Sınırlaması:** Veriler yalnızca önceden belirtilmiş, sınırlı amaçlar için kullanılabilir.  
- **Özel Nitelikli Veriler:** Lokasyon, davranışsal ve finansal veriler özel nitelikli sayıldığından, aktarım ve işleme süreçleri sıkı kurallara tabidir.  
- **Şeffaflık ve Bilgilendirme:** Profil çıkarımı, davranışsal analiz veya nudging gibi kullanımlarda kullanıcı bilgilendirilmeli ve açık rıza alınmalıdır.  

---

## 7. PoC / Pilot Uygulamalar
- **Kuantum / PQC Geçişi:** Yurt dışı hizmetlerle entegrasyon gerekiyorsa sözleşmesel ve teknik kontroller sağlanmalı; sertifika ve anahtar yönetimi güncellenmelidir.  
- **Sentetik Veri:** Pilot aşamalarda gerçek müşteri verisi yerine sentetik veri veya senaryo havuzu kullanılmalıdır.  

---

## 8. TBB – Türkiye Bankalar Birliği Rehberleri
- **Çoklu Kurum Verisi:** Farklı kaynaklardan gelen veriler birleştirilirken müşteri onayı, iptal hakkı ve şeffaf denetim kayıtları zorunludur.  
- **Davranışsal Veriler:** Müşteriye hangi verilerin kullanıldığı net açıklanmalı; öneri sistemleri yalnızca müşteri onayıyla devreye alınmalıdır.  
- **Denetim Kayıtları:** Tüm işlemler denetim loglarına kaydedilmeli ve müşteri tarafından erişilebilir olmalıdır.  
- **Model ve Algoritma Yönetimi:** Kullanılan modellerin etik sınırları, performans parametreleri ve müşteri üzerindeki etkileri açıkça tanımlanmalıdır.  
- **Otomatik Karar Sistemleri:** Yapay zekâ tabanlı karar sistemlerinde müşteri bilgilendirilmeli, “opt-out” hakkı sunulmalıdır.  
- **Şeffaflık ve Geri Alma:** Her işlem sonrası müşteriye bildirim yapılmalı; iptal ve geri alma opsiyonu zorunlu olmalıdır.  

---

## Sonuç
Bu başlıklar, Türkiye’de finansal kurumların yapay zekâ ve veri odaklı çözümleri devreye alırken dikkate alması gereken yasal, etik ve kurumsal çerçeveyi özetlemektedir.  

- **BDDK yönetmelikleri** teknik gereklilikleri,  
- **KVKK** veri koruma boyutunu,  
- **TBB rehberleri** ise müşteri iletişimi ve şeffaflık beklentilerini belirler.  

Etik ilkeler ve kurum kültürü ise bu düzenlemelerin ötesinde güveni pekiştiren tamamlayıcı unsurlardır. **Uyumun sağlanması, yalnızca riskleri azaltmakla kalmaz; müşteri güvenini ve kurum itibarını da güçlendirir.**
