# Müşteri Deneyimi ve Davranışsal Finans

Bu bölümde, müşteri etkileşimini, kişiselleştirmeyi ve finansal hizmet deneyimini dönüştüren yaklaşımları bir araya getirdim.

## **8. EmoBanking (Duygu Durumuna Duyarlı Bankacılık)**

**Tanım / Örnek Senaryo**  
Çağrı esnasında **speech-to-text (ASR)**, **speaker diarization** ve **speech emotion recognition (SER)** ile öfke/gerilim sinyali tespit edildiğinde:  
- Temsilci ekranında de-eskalasyon metni ve adım adım çözüm önerileri açılır.  
- Aynı sinyal mobil uygulama içinde ton uyarlamalı metin ve düşük sürtünmeli akış tetikler.  

Duygu sinyali karar verici sistemlerde tek başına kullanılamaz; etik/fairness kontrolleri ve **HITL (human-in-the-loop)** ilkesiyle yalnızca yardımcı bağlam olarak işlenir.  

**Trend ve Değerlendirme**  
2025’te yayımlanan **Nature Scientific Reports** ve **Elsevier** çalışmaları, çoklu-mod duygu tanıma (ses + metin) araştırmalarının gerçek diyaloglara yakın veriyle doğruluğu artırdığını ortaya koyuyor.  
**Reuters’ın Mayıs 2024 tarihli haberi**, SoftBank’ın öfkeli müşteri çağrılarını yumuşatmaya yönelik bir ses teknolojisi pilotunu devreye aldığını bildiriyor.  

Bu gelişmeler, empatik etkileşimin artık bankacılık operasyonlarına pratik olarak yerleştirilebileceğini gösteriyor.  

**Teknik Bileşenler**  
- ASR + VAD + diarization  
- SER (prosodi, spektral özellikler)  
- Multimodal fusion (voice + text)  
- Real-time recommendation (de-eskalasyon scripti, akış kısaltma)  
- Model monitoring (drift, precision/recall)  
- Bias & fairness testleri  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · AHT ↓ · FCR ↑ · Churn erken uyarı sinyali ↑ · Şikâyet yoğunluğu ↓

---

## **9. Arayüzsüz / Invisible Bankacılık (Zero-Interface Banking)**

**Tanım / Örnek Senaryo**  
Bankacılık işlemleri bağlam-tetikleyici (**context trigger**) ile arka planda görünmez biçimde gerçekleşir:  
- Ajan, takvim ve veri sinyallerinden **“tatil planı → döviz tamponu oluşturma”**, **“abonelik artışı → iptal önerisi”**, **“gelir değişimi → otomatik birikim başlatma”** gibi akışları otomatik devreye alır.  
- Kullanıcı hiçbir ekran açmadan yalnızca bildirim içinden onay verir.  
- Tüm otomasyonlar geri alınabilir ve **transparency feed** üzerinden sonradan incelenebilir.  
- Ekosistem entegrasyonuyla banka, müşterinin takvim, e-ticaret, ulaşım ve yaşam tarzı verilerinden aldığı ipuçlarını “arka planda kişisel finans asistanı” gibi kullanır.  

**Trend ve Değerlendirme**  
**ISG’nin Temmuz 2025 tarihli *Invisible Banking* analizi**, finansın geleneksel arayüzlerden bağlamsal tetikleyicilere kaydığını ve agentik otomasyon ile birleşerek günlük yaşamın içine görünmez şekilde yerleştiğini vurguluyor.  
**Forbes’un Ağustos 2024 tarihli *The Next Wave Of AI In Banking* yazısı**, bu dönüşümün bankacılıkta “ajan tabanlı işleyişin” ana akıma taşındığını gösterdiğini belirtiyor.  

Bu gelişmeler, bankacılığın müşterinin fark etmeden ama kontrol edebileceği şekilde “arkaplan hizmetine” dönüşmekte olduğunu gösteriyor.  

**Teknik Bileşenler**  
- Karmaşık olay işleme (Complex Event Processing, CEP)  
- Niyet sınıflandırma (Intent classification)  
- Bağlam motoru (Context engine: lokasyon, zaman, cihaz)  
- Arka plan ajanları (Background agents)  
- Güvenli bildirim & geri alma (Secure notifications & undo)  
- Onay defteri (Consent ledger)  
- Denetim izi (Audit trail)  

**Ölçülebilir Etki (KPI)**  
CES ↓ · İşlem tamamlama oranı ↑ · Adım sayısı ↓ · NPS ↑

---

## **10. Zaman Kırılmalı / Olası Zamanlı Bankacılık (Predictive Banking)**

**Tanım / Örnek Senaryo**  
Olası zamanlı bankacılık, yalnızca geçmişe veya “gerçek zamana” odaklanmak yerine, gelecekteki olayları öngören ve buna göre işlem hazırlayan yapay zekâ ajanlarıyla çalışır:  
- Sistem, müşterinin maaş yatırma tarihini, kredi kartı kapanış gününü, fatura kesimlerini, portföy hareketlerini ve piyasa koşullarını sürekli izler.  
- Örnek: “Yarın maaşınız yatacak, fakat bugün kredi kartınızın son ödeme günü. Bu ödemeyi sizin adınıza zamanında yapabilirim, onaylıyor musunuz?”  
- Örnek: “Gelecek hafta otomatik fatura talimatınız var, ancak hesabınızda yeterli bakiye olmayacak görünüyor. Önerim şu anda kısa vadeli mevduattan aktarım yapmanız.”  
- Predictive agent mantığıyla çalışan mikro-ajanlar **“olay tahmini → işlem hazırlığı → müşteri onayı”** zincirini yönetir. Kritik eylemler **HITL (human-in-the-loop)** kontrol noktalarıyla müşteriye sunulur; müşteri onaylarsa işlem gerçekleşir.  
- Banka tarafında uçtan uca süreçler (ör. risk izleme, likidite planlama, nakit yönetimi) önceden tetiklenir; bu, operasyonel verimlilik ve müşteri deneyimi açısından sıçrama yaratır.  

**Trend ve Değerlendirme**  
**McKinsey’nin Haziran 2025 tarihli *Seizing the agentic AI advantage* raporu**, öngörüye dayalı sistemlerin müşteri memnuniyetini %20’ye kadar artırabileceğini ve operasyonel maliyetleri ciddi oranda düşürdüğünü belirtiyor.  
**Gartner’ın Nisan 2025 tarihli *Predictive Banking and Customer Experience* raporu** ile **Accenture’un Mayıs 2025 tarihli *Banking Technology Vision* çalışması**, bankacılığın “reactive (tepkisel)” yapıdan “predictive (öngörücü)” yapıya kaydığını teyit ediyor.  
**WSJ’nin Temmuz 2025 tarihli *AI Forecasting in Consumer Banking* makalesi**, tüketici bankacılığında öngörücü ajanların müşteri deneyimini yeniden tanımladığını aktarıyor.  

Bu gelişmeler, öngörücü ajanların bankacılıkta reaktif süreçleri geride bırakarak proaktif, zaman kırılmalı bir hizmet anlayışına dönüştüğünü gösteriyor.  

**Teknik Bileşenler**  
- Olay tabanlı mikroservisler + olay akışı (Event-driven microservices + event streaming)  
- Öngörücü ajan orkestrasyonu (Predictive agent orchestrator: planlama, senaryo üretimi, görev ayrımı)  
- Özellik deposu + model kayıt/yönetişim (Feature store + model registry/governance)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + güvenlik önlemleri (guardrails)  
- İnsan denetim adımları (HITL control steps)  
- Kimlik ve erişim yönetimi (IAM/ABAC: attribute-based access control)  
- Değiştirilemez denetim izi (Immutable audit log)  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Sahtekârlık engelleme ↑ · Operasyonel kesinti ↓ · Gelir/çalışan oranı ↑

---

## **11. Oyun Teorisi ile Fintech UX (Live Negotiation in Banking)**

**Tanım / Örnek Senaryo**  
Klasik bankacılık ürünleri genellikle “tek taraflı şart” üzerinden sunulur: sabit faiz, standart vade, değişmez ücret.  
Oyun teorisine dayalı Fintech UX yaklaşımında müşteri pasif alıcı değil, dinamik pazarlık masasında aktif bir aktör hâline gelir:  
- Örnek: Bir müşteri kredi başvurusu yapar. Sistem, “Bu krediyi %2,49 faizle verebilirim. Ancak düzenli otomatik ödeme talimatı verirsen %2,39’a düşer; ek sigorta yaptırırsan %2,29 olur” şeklinde gerçek zamanlı pazarlık açar.  
- Müşteri tercihlerine göre parametreleri değiştirir, sistem buna karşılık yeni kombinasyonlar üretir. AI’nin öğrenme kabiliyetiyle her müşteriye özgü esnek teklif akışları oluşur.  
- Sigorta veya mevduatta da aynı model uygulanabilir: “Eğer şu süre boyunca erken çekim yapmazsan daha yüksek getiri sunarım.”  

Bu, müşteri deneyimini tek yönlü “teklif kabul et” yerine karşılıklı müzakereye dönüştürür.  

**Trend ve Değerlendirme**  
**McKinsey’nin Temmuz 2025 tarihli *Banking on gen AI in the credit business* raporu**, kredi ürünlerinde gen AI destekli dinamik tekliflerin değer yaratma potansiyelini ortaya koyuyor.  
**Accenture’un Mayıs 2025 tarihli *Commercial Banking Top Trends* raporu**, kurumsal bankacılıkta esnek ve kişiselleştirilmiş ürün yapılandırmalarının yükselişini işaret ediyor.  
**Gartner’ın Ekim 2024 tarihli *Top Strategic Technology Trends* çalışması**, oyun teorisi ve reinforcement learning tabanlı optimizasyonun müşteri deneyimini yeniden şekillendiren trendler arasında olduğunu vurguluyor.  

Bu gelişmeler, müşteri ile banka arasındaki ilişkinin tek taraflı olmaktan çıkıp dinamik ve öğrenen pazarlık süreçlerine dönüştüğünü gösteriyor.  

**Teknik Bileşenler**  
- Gerçek zamanlı optimizasyon motorları (game theory + reinforcement learning)  
- Event-driven mikroservisler + düşük gecikmeli API’ler  
- RAG (retrieval-augmented generation) ile açıklamalı teklif gerekçeleri  
- Güvenli prompt katmanı + fairness guardrail’leri  
- IAM/ABAC tabanlı erişim kontrolü  
- Değiştirilemez işlem kayıtları (Immutable audit log)  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Teklif kabul oranı ↑ · Churn ↓

---

## **12. Context-Aware Finansal UX (Bağlama Duyarlı Finansal Deneyim)**

**Tanım / Örnek Senaryo**  
Bağlama duyarlı finansal UX, kullanıcının lokasyon, zaman, cihaz, rutin ve niyet gibi sinyallere göre arayüz ve önerilerin otomatik olarak yeniden şekillenmesini ifade eder:  
- **Lokasyon**: Müşteri yurt dışına çıktığında mobil bankacılık ekranı dönüşür; döviz kuru, yurtdışı harcamalar ve seyahat sigortası öne çıkar.  
- **Zaman**: Maaş gününde yatırım ekranı öne çıkar, kredi teklifleri geri planda kalır. Ay sonuna doğru likidite uyarıları ve esnek ödeme planları devreye girer.  
- **Davranış**: Müşteri QR ile ödeme yapıyorsa bu özellik ana ekranda birincil hale gelir; nadiren kullanılan menüler geri plana atılır.  
- **Cihaz**: Tablet kullanan müşteri için görsel yoğun bir dashboard, akıllı saat için hızlı bakiye/ödeme kısayolları sunulur.  

Bu yapı sayesinde uygulama, statik bir menü değil, dinamik ve yaşayan bir deneyim haline gelir.  

**Trend ve Değerlendirme**  
**McKinsey’nin Haziran 2025 tarihli *Hyper-personalization in banking: Competing on context* raporu**, hiper-kişiselleştirilmiş kullanıcı deneyimini bankacılığın en kritik rekabet avantajı olarak tanımlıyor.  
**Gartner’ın Ekim 2024 tarihli *Top Strategic Technology Trends* çalışması**, bağlam-duyarlı servisleri müşteri yolculuğunu sürtünmesiz hale getiren stratejik teknoloji trendleri arasında listeliyor.  
**WSJ’nin Nisan 2025 tarihli *Banks Redesign Apps for Adaptive Customer Journeys* makalesi**, bankaların statik tasarımdan adaptif deneyime geçtiğini ortaya koyuyor.  

Bu gelişmeler, bağlama duyarlı finansal deneyimin artık müşteri beklentisinin bir parçası hâline geldiğini gösteriyor.  

**Teknik Bileşenler**  
- Complex Event Processing (CEP): Lokasyon, zaman, cihaz sinyallerini gerçek zamanlı işlemek  
- Context engine: Farklı bağlam sinyallerini birleştirip karar katmanına aktarmak  
- Event-driven microservices: Bağlama göre ekran ve akış değiştirmek  
- RAG + güvenli prompt katmanı: Bağlamı açıklayıcı, kişiselleştirilmiş yanıtlar üretmek  
- Consent ledger + immutable audit log: Bağlam kullanımının kaydı ve müşteri onayının tutulması  
- IAM/ABAC: Bağlama göre erişim ve teklif sunma yetkilerini denetlemek  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel kesinti ↓ · Gelir/çalışan ↑

---

## **13. Görev Bazlı Bankacılık (Goal-to-Flow Banking)**

**Tanım / Örnek Senaryo**  
“Görev bazlı bankacılık”, müşterinin hayatındaki amaçları proje gibi yöneten AI planlayıcıları ifade eder. Banka artık sadece ürün sunmaz, hedefi gerçekleştirmek için uçtan uca bir “akış” kurgular:  
- **Ev almak**: Müşteri “Ev almak istiyorum” dediğinde, sistem mevcut birikim ve kredi uygunluğunu kontrol eder. Tapu harcı, ekspertiz, sigorta, kredi ödemesi gibi adımları proje planı gibi sıralar. Belgeler, başvurular ve finansal akış otomatik planlanır.  
- **Borç kapatmak**: Kullanıcının farklı bankalardaki borçları konsolide edilir, en uygun refinansman senaryosu hesaplanır ve adım adım uygulama planı çıkarılır.  
- **Yurt dışında okumak**: Burs başvurusu, döviz hesabı, sağlık sigortası, kredi garantisi gibi işlemler tek akışa bağlanır. Kullanıcı tek bir “niyet” beyanıyla süreci yönetebilir.  
- **Yatırım yapmak**: “5 yıl içinde 1 milyon TL biriktirmek istiyorum” diyen kullanıcıya, gelir-gider analizine dayalı aylık yatırım stratejisi sunulur. Sistem volatiliteye göre planı günceller ve ilerleme raporları verir.  

Bu yaklaşım, ürün bazlı bankacılıktan (kredi, mevduat, kart) amaç bazlı bankacılığa (ev, eğitim, yatırım, borç yönetimi) geçişi temsil eder.  

**Trend ve Değerlendirme**  
**McKinsey’nin Nisan 2025 tarihli *From Products to Purpose: Goal-Driven Banking* raporu**, müşteri deneyiminin “amaç merkezli” dönüşümünü rekabette yeni ayrışma hattı olarak tanımlıyor.  
**Accenture’un Şubat 2025 tarihli *Reimagining Customer Journeys in Financial Services* raporu**, hedef bazlı yolculuk tasarımlarının müşteri bağlılığını %20’ye kadar artırabileceğini öngörüyor.  
**Gartner’ın Ekim 2024 tarihli *AI-Driven Orchestration in Banking* analizi**, agentik AI sayesinde “intent orchestration” kavramının geleneksel modüler tasarımları aştığını vurguluyor.  
**WSJ’nin Mart 2025 tarihli *Banks Recast Customer Experience Around Life Goals* makalesi**, bankaların müşteri deneyimini yaşam hedefleri etrafında yeniden şekillendirdiğini aktarıyor.  

Bu gelişmeler, finansal hizmetlerin artık ürün odaklı değil, amaç odaklı tasarlanmasının müşteri deneyiminde yeni bir standart oluşturduğunu gösteriyor.  

**Teknik Bileşenler**  
- Intent detection + AI planning: Kullanıcının amacını tanımlayıp plan çıkarmak  
- Workflow orchestration: Farklı ürünleri tek akışta birleştirmek  
- Event-driven microservices: Tüm işlemleri arka planda tetiklemek  
- RAG + güvenli prompt katmanı: Kullanıcıya şeffaf açıklama ve alternatif senaryolar sunmak  
- Audit log + consent ledger: Her adıma dair denetim izi ve müşteri onayı kaydı tutmak  
- HITL (Human-in-the-Loop): Kritik finansal karar noktalarında insan onayı almak  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel maliyetler ↓ · Gelir/çalışan ↑

---

## **14. Sessiz Uyarı Sistemi (Subtle Nudges)**

**Tanım / Örnek Senaryo**  
“Sessiz Uyarı Sistemi”, klasik bankacılık uygulamalarındaki gürültülü bildirim ve push mesajlarının yerine, sezgisel ve müdahalesiz işaretlerle çalışır. Bu yaklaşım, **NUI (Natural User Interface)** prensiplerini bankacılığa taşır:  
- **Yatırım kaybı**: Kullanıcının portföyünde kayıp oluştuğunda bildirim gönderilmez. Bunun yerine ekranın renk paleti kırmızıya tonlanır, grafikler yalınlaşır ve “aksiyon kartı” öne çıkar.  
- **Tekrarlayan hata**: Müşteri EFT saatini sürekli kaçırıyorsa, sonraki işlemde ekranın üst kısmında küçük bir titreşim ve ikon değişikliğiyle “otomatik planlama” seçeneği hatırlatılır.  
- **Finansal stres**: Kullanıcıya sürekli uyarı yapılmaz; kritik eşiğe gelindiğinde arayüz mikro değişikliklerle dönüşür.  

Amaç, “sürekli uyarı” yaklaşımını “sessiz farkındalık”a dönüştürerek kullanıcıyı boğmadan doğru kararlara yönlendirmektir.  

**Trend ve Değerlendirme**  
**McKinsey’nin 2025 tarihli *Digital Nudges in Finance* raporu**, davranışsal tasarımın müşteri bağlılığını %25 artırabileceğini ortaya koyuyor.  
**Gartner’ın 2024 tarihli *Subtle UX in Banking* çalışması**, agresif bildirimlerin müşteri memnuniyetini düşürdüğünü, sessiz rehberlik yöntemlerinin ise daha yüksek uzun vadeli NPS yarattığını vurguluyor.  
**Accenture’un 2025 tarihli *Next-Gen UX in Financial Services* raporu**, “mindful UX” (bilinçli farkındalık tasarımı) yaklaşımının yükselen trend olduğunu belirtiyor.  
**WSJ’nin 2025 tarihli *Why Banks Are Rethinking Notifications* makalesi**, finans kurumlarının bildirim stratejilerini yeniden tasarladığını aktarıyor.  

Bu gelişmeler, sessiz ve bağlama duyarlı uyarıların kullanıcı deneyiminde yeni standart haline geldiğini gösteriyor.  

**Teknik Bileşenler**  
- Event-driven microservices: Kritik anları algılamak  
- Context-aware UI engine: Ekran renk/pattern değişikliklerini tetiklemek  
- Haptic feedback API: Titreşim ve dokunsal sinyaller  
- Feature store: Kullanıcı davranış motiflerini saklamak  
- Explainable AI layer: Sessiz uyarının gerekçesini açıklamak  
- IAM/ABAC: Erişim kontrolü  
- Immutable audit log: Nudge karar zincirinin kaydı  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Drop-off ↓ · Gelir/çalışan ↑

---

## **15. Etik Skorlama (ESG/Impact Indicators)**

**Tanım / Örnek Senaryo**  
“Etik Skorlama”, kullanıcıya yalnızca finansal getiriyi değil, kararlarının çevresel ve toplumsal etkilerini de görünür kılar. ESG (Environmental, Social, Governance – Çevre, Sosyal, Yönetişim) kriterleri tek etiket yerine ayrı ayrı ölçülerek yansıtılır:  
- **Alışveriş**: Müşteri giyim alışverişi yaptığında, sistem işlemin karbon ayak izini (üretim + lojistik CO₂ salımı), ürünün yerel katkısını ve sosyal etki skorunu hesaplar.  
- **Yatırım fonu seçimi**: Fonun getiri/riski yanında çevresel uyumluluk, sosyal sorumluluk katkısı ve yönetişim şeffaflığı ayrı ayrı skorlanır.  
- **Bildirim**: “Bu alışverişin etik skoru %72. Yerel üretici desteği +15, karbon etkisi -20. Alternatif X ürün seçersen toplam etki +10 puan iyileşebilir.”  

Bu model, finansal bilinç ve etik farkındalığı birleştirerek kullanıcıları yalnızca kâr değil, sürdürülebilir değer odaklı davranmaya yönlendirir.  

**Trend ve Değerlendirme**  
**McKinsey’nin Haziran 2025 tarihli raporları**, bankaların farklılaşmayı artık yalnızca fiyat veya hız değil, etik ve sosyal değer üzerinden sağladığını gösteriyor.  
**Accenture’un 2025 tarihli *Banking Top 10 Trends* raporu**, sürdürülebilir bankacılığın 2030 vizyonunun temel yapıtaşlarından biri olduğunu ve ESG skorlamanın önümüzdeki 5 yılın ana akımı olacağını öngörüyor.  
**Gartner’ın 2024 tarihli *Top Strategic Technology Trends* çalışması**, ESG uyumlu teknolojilerin yalnızca regülasyon değil, müşteri sadakati için de kritik hale geldiğini vurguluyor.  
**WSJ’nin Haziran 2025 tarihli *Digital Workers Have Arrived in Banking* makalesi**, bankacılıkta dijital dönüşümün etik tasarım ve hesap verebilirlik boyutunu da öne çıkarıyor.  

Bu gelişmeler, finansal kararların yalnızca ekonomik değil, çevresel ve toplumsal etkiler üzerinden de değerlendirileceğini gösteriyor.  

**Teknik Bileşenler**  
- Event-driven microservices: ESG verilerini işlem bazlı ayrıştırmak  
- Feature store: Çevre, sosyal, yönetişim özelliklerini ayrı katmanlarda depolamak  
- Explainable AI (XAI): Skorun nasıl oluştuğunu şeffaf biçimde sunmak  
- RAG + güvenli prompt katmanı: ESG açıklamalarını doğru bağlamla üretmek  
- IAM/ABAC: ESG veri erişimini rol tabanlı denetlemek  
- Audit logs: ESG hesaplamalarının regülasyon uyumlu kaydını tutmak  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · Yeni ürün kabul oranı ↑ · Segmentasyon derinliği ↑ · Reputasyon riski ↓ · Gelir/çalışan ↑

---

## **16. Otonom Finansal İyileştirme Döngüsü (Autonomous Financial Recovery Loop)**

**Tanım / Örnek Senaryo**  
“Otonom Finansal İyileştirme Döngüsü”, klasik öneri sistemlerinden farklı olarak, kullanıcının riskli finansal davranışlarında sistemin kendi kendini kısıtlamasını ifade eder. Amaç, müşteriyi cezalandırmak değil, onunla birlikte finansal yeniden yapılanma moduna geçmektir:  
- **Kredi kartı borcu**: Kullanıcı üç ay üst üste yalnızca minimum ödeme yaparsa, kredi teklifleri geri plana alınır, “pasif mod” başlatılır ve ana ekran sadeleşir.  
- **Gecikme alışkanlığı**: Sık sık ödeme gecikmesi yaşayan müşteriye yeni kredi teklifi gösterilmez, yalnızca ödeme kolaylığı, yapılandırma ve farkındalık içerikleri öne çıkar.  
- **Aşırı riskli yatırım**: Riskli işlemler geçici olarak opsiyonel hale gelir, portföy ekranı sadeleştirilir ve kullanıcıya “yeniden başlatma” seçeneği sunulur.  

Bu yaklaşım, bankayı sadece işlem sağlayıcısı değil, davranışsal eşlikçi haline getirir. Sistem, müşterinin zayıf dönemlerinde “durmayı” öğrenir.  

**Trend ve Değerlendirme**  
**McKinsey’nin Haziran 2025 tarihli raporları**, agentik AI’ın artık reaktif değil, proaktif ve duruma göre kısıtlayıcı davranış modelleriyle ölçekli değer yarattığını vurguluyor.  
**Gartner’ın 2024 tarihli *Top Strategic Technology Trends* raporu**, agentic AI’ın en kritik trendlerden biri olduğunu ve risk yönetiminde insan benzeri uyarlanabilirlik kazandırdığını belirtiyor.  
**Accenture’un 2025 tarihli *Banking Top 10 Trends* raporu**, müşteri sadakati için bankaların yalnızca teklif üretmek değil, müşterilerle birlikte yavaşlama ve iyileşme döngülerine girmesi gerektiğini ifade ediyor.  
**WSJ’nin Haziran 2025 tarihli *Digital Workers Have Arrived in Banking* makalesi**, finans sektöründe dijital çalışanların etik ve koruyucu yaklaşımlarla entegre edildiğini aktarıyor.  

Bu gelişmeler, finansal hizmetlerin yalnızca hız ve teklif değil, müşterinin toparlanma dönemlerinde destekleyici rol üstlenmesi gerektiğini gösteriyor.  

**Teknik Bileşenler**  
- Event-driven microservices: Riskli davranış tetikleyicilerini algılamak  
- Feature store: Tekrarlayan borç, gecikme, yüksek riskli yatırım gibi sinyalleri depolamak  
- RAG + güvenli prompt katmanı: Kullanıcıya sade ve güvenli açıklamalar sunmak  
- HITL (Human-in-the-Loop): Kritik durumlarda temsilciye otomatik yönlendirme  
- IAM/ABAC: Kullanıcıya hangi modların uygulanabileceğini tanımlamak  
- Audit logs: Kısıtlamaların gerekçelerini denetlenebilir şekilde kaydetmek  

**Ölçülebilir Etki (KPI)**  
NPS ↑ · AHT ↓ · FCR ↑ · Temerrüt oranı ↓ · Gelir/çalışan ↑