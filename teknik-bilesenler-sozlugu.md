# Teknik Bileşenler Sözlüğü

## **Mimari & Entegrasyon**  
- **API Gateway — API Geçidi**  
API gateway, farklı servislerin tek bir giriş noktası üzerinden yönetilmesini sağlayan, güvenlik, yönlendirme, hız sınırlama ve izleme gibi yetenekler sunan bir ara katman bileşenidir.  
- **Background Agents — Arka Plan Ajanları**  
Background agents, sürekli veya tetiklemeye bağlı çalışan, sistemin arka planında belirli görevleri (veri temizleme, raporlama, bildirim gönderme gibi) otomatik olarak yerine getiren yazılım bileşenleridir.  
- **Change Data Capture (CDC) — Veri Değişim Yakalama**  
Change Data Capture, veri tabanında gerçekleşen ekleme, güncelleme veya silme işlemlerini gerçek zamanlı olarak yakalayarak sistemler arası senkronizasyon ve akış bazlı işlemeyi mümkün kılan bir tekniktir.  
- **Complex Event Processing (CEP) — Karmaşık Olay İşleme**  
Complex event processing, birden çok kaynaktan gelen veri akışlarını analiz ederek olaylar arasındaki ilişkileri ve desenleri tanıyan, gerçek zamanlı çıkarımlar yapılmasını sağlayan bir teknolojidir.  
- **Developer Sandbox — Geliştirici Oyun Alanı**  
Developer sandbox, geliştiricilerin canlı sistemlere zarar vermeden yeni özellikleri deneyebileceği, test ve geliştirme süreçleri için izole edilmiş güvenli bir ortamdır.  
- **Event-driven Microservices — Olay Tabanlı Mikroservisler**  
Event-driven microservices, servislerin birbiriyle doğrudan çağrı yerine olay mesajları üzerinden iletişim kurduğu, ölçeklenebilirlik ve gevşek bağlılık sağlayan bir mimari yaklaşımdır.  
- **Event Streaming — Olay Akışı**  
Event streaming, sürekli üretilen verilerin (örneğin işlem kayıtları, sensör çıktıları veya kullanıcı etkileşimleri) gerçek zamanlı işlenmesi ve tüketilmesi için kullanılan bir veri işleme modelidir.  
- **Modular UI Framework & Plugin Architecture — Modüler UI Çatısı ve Eklenti Mimarisi**  
Bu yaklaşım, kullanıcı arayüzünü modüllere bölerek bağımsız geliştirme, kolay ölçekleme ve farklı takımların katkıda bulunmasına imkân verir; eklenti yapısı sayesinde işlevler dinamik olarak genişletilebilir.  
- **Saga / Compensation Patterns — Saga / Telafi Desenleri**  
Saga deseni, dağıtık sistemlerde uzun süren işlemleri küçük adımlara böler ve başarısızlık durumunda telafi edici (compensation) işlemlerle tutarlılığı korur.  
- **Secure Containerization (Mini-app Deployment) — Güvenli Konteynerleştirme (Mini Uygulama Dağıtımı)**  
Secure containerization, uygulamaları yalıtılmış konteynerlerde çalıştırarak güvenliği artıran ve mini uygulamaların bağımsız şekilde dağıtımını mümkün kılan bir yöntemdir.  
- **Smart Contract Engine (Opsiyonel) — Akıllı Sözleşme Motoru (Opsiyonel)**  
Smart contract engine, blok zinciri veya dağıtık defter teknolojileri üzerinde çalışan, koşulları önceden belirlenmiş dijital sözleşmelerin otomatik yürütülmesini sağlayan bir yazılım bileşenidir.  
- **Workflow / Orchestration Engine — İş Akışı / Orkestrasyon Motoru**  
Workflow engine, süreçleri adım adım tanımlayıp otomatikleştiren; orkestrasyon motoru ise birden fazla sistem ve servisin koordineli çalışmasını yöneten bileşendir.

---

## **Kimlik, Yetki & Rıza**  
- **Consent Management / Consent Ledger — Rıza Yönetimi / Rıza Defteri**  
Consent management, kullanıcıların kişisel verilerinin işlenmesine dair verdikleri izinlerin kaydedilmesi, yönetilmesi ve gerektiğinde geri alınabilmesini sağlayan sistemdir.  
- **IAM / RBAC / ABAC — Kimlik ve Yetki Yönetimi**  
Identity and Access Management (IAM), Role-Based Access Control (RBAC) ve Attribute-Based Access Control (ABAC), kullanıcıların kimlik doğrulama ve yetkilendirme süreçlerini yöneten, erişim politikalarını roller veya öznitelikler üzerinden belirleyen yaklaşımlardır.  
- **Identity Resolution — Kimlik Çözümleme**  
Identity resolution, farklı kaynaklarda aynı kişiye ait parçalı kimlik bilgilerini eşleştirerek tekil ve bütünleşik bir kullanıcı profili oluşturmayı sağlayan süreçtir.  
- **Scoped Tokens — Kapsamlı Jetonlar**  
Scoped tokens, erişim yetkilerinin belirli bir süre, kapsam veya işlemle sınırlandırıldığı, güvenliği artıran kimlik doğrulama belirteçleridir.

---

## **Veri & AI Temelleri**  
- **Context-aware UI Engine — Bağlama Duyarlı Arayüz Motoru**  
Context-aware UI engine, kullanıcının bağlamına (konum, zaman, cihaz veya geçmiş davranışlar) göre arayüz öğelerini dinamik olarak uyarlayan bir yazılım bileşenidir.  
- **Context Engine — Bağlam Motoru**  
Context engine, kullanıcı veya sistem etkileşimlerinden elde edilen bilgileri bir araya getirerek daha kişiselleştirilmiş ve anlamlı çıktılar üretmeye yarayan bir altyapıdır.  
- **Dynamic Persona Engine — Dinamik Persona Motoru**  
Dynamic persona engine, kullanıcıların davranış ve tercihlerini sürekli analiz ederek güncel persona profilleri oluşturur ve buna uygun özelleştirilmiş deneyimler sunar.  
- **Explainable AI (XAI) — Açıklanabilir Yapay Zekâ**  
Explainable AI, yapay zekâ modellerinin karar süreçlerini şeffaf hale getirerek kullanıcıların neden belirli çıktılar üretildiğini anlamalarını sağlayan yöntemler bütünüdür.  
- **Feature Store — Özellik Deposu**  
Feature store, makine öğrenimi modellerinde kullanılan özelliklerin merkezi olarak saklandığı, tekrar kullanılabildiği ve tutarlılık sağlandığı bir veri yönetim sistemidir.  
- **Guardrails — Koruma Katmanları**  
Guardrails, yapay zekâ sistemlerinin çıktılarında güvenlik, doğruluk ve uygunluk kontrolleri uygulayarak hatalı veya riskli sonuçların önüne geçen teknik mekanizmalardır.  
- **Intent Detection & Classification — Niyet Tespiti ve Sınıflandırma**  
Intent detection, kullanıcı ifadelerinden amaç veya isteğin çıkarılmasını; classification ise bu amaçların önceden tanımlı kategorilere ayrılmasını sağlayan doğal dil işleme yöntemleridir.  
- **Model Governance — Model Yönetişimi**  
Model governance, yapay zekâ modellerinin geliştirilmesi, kullanımı ve güncellenmesi süreçlerinde etik, yasal ve operasyonel standartlara uyumu garanti altına alan yönetim çerçevesidir.  
- **Model Monitoring — Model İzleme**  
Model monitoring, kullanılan yapay zekâ modellerinin performansını sürekli takip ederek sapma (drift), doğruluk veya hatalı sonuç risklerini erken tespit eden süreçtir.  
- **Model Registry & Versioning — Model Kayıt ve Sürümleme**  
Model registry, geliştirilen yapay zekâ modellerinin merkezi bir havuzda saklanmasını sağlarken versioning, modellerin farklı sürümlerinin izlenebilirliğini ve geri dönüşünü mümkün kılar.  
- **NLQ / NLBI (Natural Language Query / Business Intelligence) — Doğal Dil Sorgulama / İş Zekâsı**  
NLQ/NLBI, kullanıcıların teknik sorgu dilleri bilmeden doğal dil ile veri tabanlarına soru sormasını ve iş zekâsı çıktıları üretmesini sağlayan teknolojilerdir.  
- **Observability (Telemetry, Metrics, Traces) — Gözlemlenebilirlik (Telemetri, Metrikler, İzler)**  
Observability, sistemin iç işleyişini anlamak için telemetri verileri, performans metrikleri ve işlem izlerini toplayıp analiz ederek şeffaflık ve hata teşhisi sağlayan bir yaklaşımdır.  
- **RAG (Retrieval-Augmented Generation) — Bilgi Getirmeli Üretim**  
RAG, büyük dil modellerinin yanıt üretmeden önce harici bilgi kaynaklarından içerik alarak daha doğru ve güncel çıktılar vermesini sağlayan bir yöntemdir.  
- **Real-time Optimization (Game Theory + RL) — Gerçek Zamanlı Optimizasyon**  
Real-time optimization, oyun teorisi ve pekiştirmeli öğrenme (reinforcement learning) tekniklerini kullanarak kararların dinamik koşullara göre sürekli optimize edilmesini mümkün kılar.  
- **Recommendation Engine — Öneri Motoru**  
Recommendation engine, kullanıcıların geçmiş davranışlarını ve benzer profilleri analiz ederek kişiselleştirilmiş ürün, içerik veya hizmet önerileri sunan algoritmalardır.  
- **Risk & Fairness (Bias Detection) — Risk ve Adalet (Önyargı Tespiti)**  
Risk & fairness yöntemleri, yapay zekâ modellerinde önyargıların belirlenmesi ve azaltılmasına odaklanır; böylece daha güvenilir ve adil sonuçlar elde edilir.  
- **Scenario / What-if Engine — Senaryo / Ne-olursa Motoru**  
Scenario engine, farklı varsayımlar altında olası sonuçları simüle ederek kullanıcıların alternatif senaryoları değerlendirmesine imkân tanıyan bir analiz aracıdır.  
- **Vector Indexes — Vektör Dizinleri**  
Vector indexes, metin veya görsel gibi içeriklerin vektör temsilini hızlı şekilde aramayı ve benzerlik bazlı eşleştirmeyi mümkün kılan veri yapılarıdır.  
- **Vector Representations (Embeddings) — Vektör Temsilleri**  
Embeddings, metin, görsel veya diğer verileri matematiksel vektörlere dönüştürerek bilgisayarların anlam ilişkilerini ve benzerlikleri öğrenmesini sağlayan yöntemdir.

---

## **Denetim, Uyum & Güvenlik**  
- **Human-in-the-Loop (HITL) — İnsan Döngüde**  
HITL, makine öğrenimi ve yapay zekâ sistemlerinde kritik karar noktalarında insan uzmanların sürece dâhil edilmesini sağlayan yaklaşımdır; böylece model çıktılarının güvenilirliği ve etik uygunluğu artırılır.  
- **Immutable Audit Log / Audit Trail — Değiştirilemez Denetim Kaydı**  
Immutable audit log, bir sistemde yapılan tüm işlemleri değiştirilemez ve silinemez şekilde kaydeden yapıdır; kullanıcı, işlem, zaman ve sonuç bilgilerini geri dönülmez biçimde saklayarak şeffaflık ve hesap verebilirlik sağlar.  
- **Policy-as-Code — Kod Olarak Politika**  
Policy-as-code, güvenlik, erişim veya iş kurallarının yazılım kodu şeklinde tanımlanarak otomatik olarak uygulanmasını sağlayan yaklaşımdır; bu sayede tutarlılık, hız ve regülasyon uyumu elde edilir.  
- **Privacy-Preserving Techniques — Gizlilik Korumalı Teknikler**  
Privacy-preserving techniques, veri mahremiyetini koruyarak yapay zekâ veya analitik işlemler yapılmasını sağlayan yöntemlerdir; bunlar arasında differential privacy (fark gizliliği), federated learning (federe öğrenme), secure multi-party computation (SMPC/MPC) ve zero-knowledge proofs (ZKP) bulunur.  
- **Secure Data Pooling — Güvenli Veri Havuzlama**  
Secure data pooling, farklı kaynaklardan gelen verilerin bir araya getirilerek analiz edilmesini, fakat bu süreçte gizlilik ve güvenlik ilkelerinin korunmasını sağlayan yöntemdir; özellikle bankacılık gibi regülasyonlu sektörlerde önemlidir.

---

## **Ses/Multimodal & Çağrı Merkezi**  
- **ASR + VAD + Diarization — Otomatik Konuşma Tanıma + Ses Aktivitesi Tespiti + Konuşmacı Ayrımı**  
ASR (Automatic Speech Recognition), konuşmayı metne çevirir; VAD (Voice Activity Detection), konuşma anlarını tespit eder; diarization ise farklı konuşmacıları birbirinden ayırır. Bu bileşenler çağrı merkezi otomasyonu ve analizinde temel altyapıyı oluşturur.  
- **Multimodal Fusion (Voice + Text) — Çok Modlu Birleştirme (Ses + Metin)**  
Multimodal fusion, farklı veri türlerini (ör. ses ve metin) birleştirerek daha zengin ve doğru analizler yapılmasını sağlar; çağrı merkezlerinde müşteri deneyimini geliştirmek için kullanılır.  
- **Real-time De-eskalation Önerileri — Gerçek Zamanlı Gerginlik Azaltma Önerileri**  
Real-time de-eskalation önerileri, müşteri temsilcilerine konuşma sırasında duygu analizi ve risk sinyallerine göre sakinleştirici, çözüm odaklı yanıt önerileri sunan yapay zekâ sistemleridir.  
- **SER (Speech Emotion Recognition) — Konuşma Duygu Tanıma**  
SER, konuşma sinyallerindeki prosodi (tonlama, tempo, vurgu) ve spektral özellikleri analiz ederek konuşmacının duygusal durumunu tespit eden yapay zekâ tabanlı yöntemdir.

---

## **İleri Seviye / Kuantum**  
- **Hybrid Workflow Orchestration — Hibrit İş Akışı Orkestrasyonu**  
Hybrid workflow orchestration, klasik ve kuantum tabanlı algoritmaların birlikte çalışmasını sağlayan iş akışı yönetimidir; bu yaklaşım özellikle optimizasyon ve simülasyon problemlerinde hesaplama verimliliğini artırır.  
- **Model Validation & Stress Testing — Model Doğrulama & Stres Testleri**  
Model validation, yapay zekâ ve ML modellerinin amaçlandığı şekilde çalıştığını doğrulayan süreçtir; stres testleri ise uç senaryolarda (ekonomik şok, yüksek hacim, aşırı oynaklık) model dayanıklılığını ölçer.  
- **Post-Quantum Cryptography (PQC) — Kuantum Sonrası Kriptografi**  
PQC, gelecekte kuantum bilgisayarların mevcut şifreleme yöntemlerini kırma riskine karşı dayanıklı algoritmaların geliştirilmesini ifade eder; finansal verilerin uzun vadeli güvenliğini sağlamak için kritik önemdedir.  
- **QKD (Quantum Key Distribution) — Kuantum Anahtar Dağıtımı**  
QKD, kuantum mekaniği prensipleriyle şifreleme anahtarlarının güvenli şekilde paylaşılmasını sağlar; herhangi bir dinleme girişimi kuantum özellikler nedeniyle hemen fark edilir ve anahtar geçersiz kılınır.  
- **Quantum-Inspired Optimization — Kuantum Esinli Optimizasyon**  
Quantum-inspired optimization, kuantum hesaplama prensiplerinden esinlenen ancak klasik donanım üzerinde çalışan algoritmalardır; karmaşık optimizasyon problemlerini daha hızlı ve etkin çözmeyi amaçlar.

---

## **Davranışsal Analitik & Risk**  
- **Anomaly Detection — Anomali Tespiti**  
Anomaly detection, normal davranış örüntülerinden sapmaları tespit eden yöntemdir; finansal dolandırıcılık, operasyonel hata veya güvenlik ihlallerini erken fark etmek için kullanılır.  
- **Behavioral Analytics Engine — Davranışsal Analitik Motoru**  
Davranışsal analitik motoru, kullanıcıların dijital etkileşimlerini inceleyerek risk skorları, segmentasyon veya kişiselleştirilmiş hizmetler üreten yapıdır.  
- **Event Capture & Stream Processing — Olay Yakalama & Akış İşleme**  
Event capture & stream processing, gerçek zamanlı olay verilerinin yakalanıp işlenmesini sağlayan altyapıdır; düşük gecikmeyle karar verme süreçlerini tetikler.  
- **Risk Engine Entegrasyonu — Risk Motoru Entegrasyonu**  
Risk engine entegrasyonu, analitik motorların kredi, dolandırıcılık veya likidite gibi riskleri hesaplayan sistemlere bağlanmasını ifade eder; böylece karar süreçleri otomatik ve tutarlı hale gelir.

---

## **Kurumsal Arama & Bilgi Yönetimi**  
- **Enterprise Search & Knowledge Management — Kurumsal Arama & Bilgi Yönetimi**  
Enterprise search & knowledge management, kurum içi belgeler, veri tabanları ve iletişim kayıtları üzerinde gelişmiş arama ve bilgi yönetimi imkânı sağlayan çözümlerdir; çalışanların doğru bilgiye hızlı ulaşmasını ve kurumsal hafızanın korunmasını destekler.
