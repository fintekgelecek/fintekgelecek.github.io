# Yapay Zekâ ve Ajan Teknolojileri

Bu bölümde, yapay zekânın finansal hizmet süreçlerini nasıl dönüştürdüğüne odaklanan fikirleri topladım.

## **1. Otonom Finansal Ajanlar (Autonomous Finance Agents)**

**Tanım / Örnek Senaryo**  
Otonom finansal ajanlar, müşteri hedeflerini esas alarak karar alabilen, eylem tetikleyen ve süreçleri kendi kendine orkestre eden yeni nesil yapay zekâ bileşenleridir. Ajan, müşterinin aylık nakit akışını, yaklaşan fatura ve borçlarını, kart kesim tarihlerini ve piyasa koşullarını izler. Belirlenen hedefler doğrultusunda (likidite ≥ X, gecikme = 0, birikim = Y) planlama yapar ve gerekli eylemleri (ödeme talimatı, vadeliye geçiş, mikro-yatırım) kendi başına tetikler. Ardından denetim kaydı üretir, geri alma seçeneği sunar ve müşteriyi bilgilendirir.  
Müşterinin girdiği sınırlar (limitler, risk iştahı, yetkiler) **policy-as-code** yaklaşımıyla uygulanır. Banka tarafında ajan, uçtan uca süreçleri (ör. itiraz/chargeback) “toplayıcı → kararlayıcı → icracı” alt-ajanlar ile orkestre eder. “Onaylı otomasyon” ilkesiyle kritik adımlarda **HITL (human-in-the-loop)** kontrol noktaları bulunur.  

**Trend ve Değerlendirme**  
2025 itibarıyla agentic AI bankacılıkta operasyonel ölçeğe geçmiş durumda:  
- McKinsey’nin Haziran 2025 tarihli *Seizing the agentic AI advantage* raporu, dikey (vertical) ajanların karmaşık iş akışlarını otomasyona çekerek ölçekli değer yarattığını ve ajanın hedefe yönelik planlama kabiliyetini vurguluyor.  
- McKinsey’nin aynı ay yayımladığı *Digital Banking: speed, scale, and the agentic arms race* analizi, bankacılıkta agentic AI yarışının “hız ve ölçek” ekseninde ilerlediğini ortaya koyuyor.  
- Ağustos 2025’te yayımlanan *Is agentic AI a financial crime game changer?* başlıklı rapor, finansal suçla mücadelede uçtan uca KYC/AML akışı için “ajan fabrikası” örneğini öne çıkarıyor.  

Bu üç rapor birlikte değerlendirildiğinde, teknolojinin artık bir “demo”dan çıkarak bankacılık operasyonlarının çekirdeğine yerleştiğini gösteriyor. Başka bir deyişle, agentic AI bugün için rekabet avantajı değil, operasyonel gereklilik hâline geliyor.  

**Teknik Bileşenler**  
- Olay tabanlı mikro servisler + olay akışı (Event-driven microservices + event streaming)  
- Saga / telafi desenleri (Saga / compensation patterns)  
- Ajan orkestrasyonu (agent orchestration: planlama, araç kullanımı, görev ayrımı), araç çağırma (tool calling), policy-as-code (yetki, limit, zaman penceresi)  
- Bilgi getirme destekli üretim (Context/RAG: retrieval-augmented generation) + koruma önlemleri (guardrails: prompt/response doğrulama, güvenlik)  
- Özellik deposu (Feature store)  
- Model kayıt ve yönetişim (Model registry / governance)  
- Gözlemlenebilirlik (Observability: telemetri, metrik, izleme)  
- Risk ve adalet: Önyargı tespiti (Risk & fairness: bias detection)  
- İnsan denetim adımları (HITL control steps)  
- Değiştirilemez denetim izi (Immutable audit log)  

**Ölçülebilir Etki (KPI)**  
STP ↑ · AHT ↓ · FCR ↑ · NPS ↑ · Operasyonel kesinti ↓

---

## **2. Kişiselleştirilmiş AI Bankacı (Tokenize Finansal Kimlik)**

**Tanım / Örnek Senaryo**  
Müşteriye ait ve bankanın içinde çalışan bir “dijital bankacı” persona tanımlanır. Bu persona; risk iştahı, iletişim tonu, ödeme disiplini, hedefler ve yasaklar ile yapılandırılır.  
Niyet (**intent**) tespitinden gelen sinyallere dayanarak proaktif öneriler ve eylemler üretir:  
- “Bugün maaş yattı → otomatik birikim %X ayırdım.”  
- “Kart kesimi yarın → likidite ayırdım.”  
- “Döviz kuru Y seviyesinin altına düştü → belirlediğin oranda mikro-alım yaptım.”  
- “Yaklaşan tatil için uçak bileti harcamanı takibe aldım → kredi kartı limitini geçici olarak yükselttim.”  

Tüm işlemler, sadece ilgili yetkiyi tanımlayan güvenli erişim belirteçleriyle yapılır ve müşteri isterse her zaman işlemi geri alabilir.

**Trend ve Değerlendirme**  
McKinsey’nin Haziran 2025 tarihli *Seizing the agentic AI advantage* raporu, “genel amaçlı copilots” yerine dikey ve süreç-özgü ajanların değer yarattığını ortaya koyuyor.  
Aynı dönemde McKinsey tarafından yayımlanan *The future of customer experience: embracing agentic AI* analizi, kurumların müşteri deneyimini yeniden tasarlarken profil/niyet/olay sinyallerini gerçek zamanlı işleyen bir çekirdek veri omurgasına ihtiyaç duyduğunu vurguluyor.  

Bu perspektif, “AI bankası” yaklaşımının artık kavramsal bir vizyon değil, müşteri etkileşiminde operasyonel bir tasarım ilkesi hâline geldiğini gösteriyor.  

**Teknik Bileşenler**
- Kimlik çözümleme (Identity resolution)  
- Olay akışı / değişim veri yakalama (Event streaming / CDC: change data capture)  
- Vektör temsilleri (Vector representations / embeddings)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + koruma önlemleri (guardrails)  
- Kapsam bazlı erişim belirteçleri (Scoped tokens)  
- Model ve versiyon yönetişimi (Model/version governance)  
- Açık rıza ve izin yönetimi (Consent management)  
- Gözlemlenebilirlik (Observability: telemetri, metrik, izleme)  

**Ölçülebilir Etki (KPI)**
Kişiselleştirilmiş teklif dönüşümü ↑ · Proaktif etkileşim ↑ · İlgisiz bildirim ↓ · NPS ↑

---

## **3. Intent-First Bankacılık (Niyet Tabanlı Orkestrasyon)**

**Tanım / Örnek Senaryo**  
Bugüne kadar dijital bankacılık sistemleri **API-first** mantığıyla kurgulandı: belirli bir işlem yapmak için kullanıcı doğru endpoint’i çağırmak zorundaydı. **Intent-first** yaklaşımında ise kullanıcı niyetini belirtir, sistem geri kalan işlemleri kendi başına orkestre eder.  

**Müşteri örnekleri:**
- “Ev almayı düşünüyorum” ifadesi: kredi ön-teklifi, ekspertiz süreci ve sigorta paketini aynı orkestrasyon katmanında toplar. 
- “Yurt dışına çıkıyorum” dediğinde, sistem şu akışları otomatik tetikler:  
  - Döviz kuru önerisi ve anında dönüşüm  
  - Seyahat sigortası teklifi  
  - Kartın yurt dışı kullanım onayı  
  - Veri dolaşımı ve güvenlik kontrolü  

**Kurum çalışanı örnekleri:**  
- Müşteri temsilcisi “müşteri sadakat riski yüksek” intent’ini seçtiğinde, sistem proaktif kampanya, indirim veya iletişim stratejisini otomatik önerir.  
- Operasyon ekibi “yüksek sahtecilik riski” intent’i seçtiğinde, sistem ek doğrulama, anlık blokaj ve denetim adımlarını otomatik bağlar.  

Bu sayede işlem bazlı modüller yerine, niyet odaklı bütünleşik deneyim yaratılır.  

**Trend ve Değerlendirme**  
2025 itibarıyla bankacılıkta niyet tabanlı orkestrasyon, hiper-kişiselleşme ve operasyonel verimlilik için kritik bir dönüşüm noktası hâline gelmiş durumda:  
- McKinsey’nin Haziran 2025 tarihli *Seizing the agentic AI advantage* raporu ve Accenture’un *Banking Top 10 Trends 2025* analizi, müşteri ihtiyaçlarının niyet odaklı yaklaşımlarla karşılanmasının ölçekli değer yaratmadaki önemini vurguluyor.  
- Gartner’ın Ekim 2024’te yayımladığı *Top Strategic Technology Trends 2025* çalışması, “AI-driven orchestration” eğilimini finansal hizmetlerde API-first paradigmasının ötesine geçiş olarak tanımlıyor.  
- WSJ’nin Haziran 2025 tarihli *Digital Workers Have Arrived in Banking* haberi, finans kurumlarının agentic AI ile modüler değil bütünleşik akışlar sunduğunu örneklerle aktarıyor.  

Bu gelişmeler birlikte değerlendirildiğinde, intent-first yaklaşımı müşteri deneyiminde basit bir inovasyon değil; rekabet için temel bir mimari değişim olarak öne çıkıyor.  

**Teknik Bileşenler**
- Niyet tespiti ve sınıflandırma (Intent detection & classification: NLP tabanlı modeller)  
- Orkestrasyon motoru (Orchestration engine: workflow automation + policy-as-code)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + koruma önlemleri (guardrails)  
- Olay tabanlı mikro servisler (Event-driven microservices)  
- Kimlik ve erişim yönetimi (IAM: Identity & Access Management) + öznitelik tabanlı erişim kontrolü (ABAC: Attribute-Based Access Control)  
- Değiştirilemez denetim izi (Immutable audit log)  

**Ölçülebilir Etki (KPI)**
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel kesinti ↓ · Gelir/çalışan ↑ · Müşteri memnuniyeti ↑

---

## **4. Yapay Zekâyla Yönetilen Mikrobankalar**

**Tanım / Örnek Senaryo**  
Müşteri onboarding sırasında AI tabanlı bir **mikro-banka kurulum asistanı** ile karşılaşır. Burada amaç “Her müşteri kendi bankasını yaratır” fikri ile, klasik “tek tip ürün/arayüz” yaklaşımının dışında bir hizmet sunmaktır. Mikro-banka kurulum asistanı, müşterinin:  
- Risk toleransı  
- Hedefleri  
- İletişim tercihleri (ör. SMS yerine WhatsApp veya yalnızca mobil bildirim)  
- Dil seçimi  
- Ürün tercihleri (ör. faizsiz ürünler, sürdürülebilir yatırımlar)  

gibi parametreleri sorar ve bu verilerle kişisel **mikro-banka profili** oluşturur.  

**Örnek müşteri tipleri:**  
- Emekli → düşük risk; düzenli ödeme hatırlatıcıları ve tasarruf odaklı öneriler.  
- Girişimci → yüksek risk toleransı; nakit akışı tahmini, yatırım fırsatları, vergi hatırlatıcıları.  
- Öğrenci → düşük bütçe yönetimi; harcama limiti önerileri, mikro-tasarruf planları, kampüs odaklı teklifler.  

Arka planda bankanın AI orkestrasyonu, her müşteriye özel mikrobankacılık akışlarını yönetir. Bu bir UI özelleştirmesinden öte, davranışsal otomasyon ve niyet tabanlı orkestrasyon anlamına gelir.  

Banka tarafında “mikrobankalar” bir arada analiz edildiğinde kurumun elinde binlerce farklı müşteri-bankası senaryosu olur. Bu çeşitlilik, ürün geliştirme ve müşteri segmentasyonu için benzersiz bir öğrenme kaynağına dönüşür.  

**Trend ve Değerlendirme**  
2025 itibarıyla hiper-kişiselleşme, bankacılıkta farklılaşmanın temel stratejisi hâline geliyor:  
- Gartner’ın Ekim 2024’te yayımladığı *Top Strategic Technology Trends 2025* çalışması, müşteri başına “AI-curated experience layer” eğilimini öne çıkarıyor.  
- Accenture’un *Banking Top 10 Trends 2025* raporu, “AI-personalized banking instances” kavramını ölçeklenebilir müşteri deneyimi inovasyonu olarak tanımlıyor.  
- WSJ’nin Haziran 2025 tarihli *Digital Workers Have Arrived in Banking* haberi, finans kurumlarının artık “tek uygulama” yerine kişiselleşmiş mikro-hizmet kümeleri üzerinden değer yarattığını aktarıyor.  
- MAS’ın 2024/2025 döneminde yayımladığı *AI in Finance Guidelines*, finans sektöründe kişiselleştirilmiş yapay zekâ uygulamalarının regülasyon çerçevesini tanımlıyor.  

Bu gelişmeler birlikte değerlendirildiğinde, mikrobankacılığın yalnızca müşteri arayüzü değil; bankacılığın çekirdek iş modeli için köklü bir dönüşüm anlamına geldiği görülüyor.  

**Teknik Bileşenler**
- Persona kurucu + AI orkestrasyonu (Persona builder + AI orchestration)  
- Politika-kod yaklaşımı (Policy-as-code: risk ve ürün seçim limitlerinin şeffaf uygulanması)  
- Bilgi getirme destekli üretim (Context/RAG: retrieval-augmented generation)  
- Olay tabanlı mikro servisler (Event-driven microservices: profil bazlı tetikleme)  
- Kimlik ve erişim yönetimi (IAM/ABAC: Identity & Access Management / Attribute-Based Access Control)  
- Değiştirilemez denetim izi (Immutable audit log: kişiselleştirilmiş tüm akışların kaydı)  

**Ölçülebilir Etki (KPI)**
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel kesinti ↓ · Gelir/çalışan ↑ · Churn ↓

---

## **5. Zincirleme Finansal Ajanlar (Multi-Agent Orchestration)**

**Tanım / Örnek Senaryo**  
“Zincirleme Finansal Ajanlar”, farklı uzmanlık rollerinde çalışan birden fazla AI ajanın çıktılarının orkestre edildiği yapıdır. Tek bir “süper ajan” yerine, her biri belirli göreve odaklanan mikro-ajanlar aynı bağlam üzerinde iş birliği yapar. Örneğin,

Müşteri mobil uygulamadan “yatırım yapmak istiyorum” der:  
- **Ajan-1 (Finansal Analiz):** Mevcut nakit akışı, likidite ve borç/gelir oranını inceler.  
- **Ajan-2 (Piyasa Taraması):** Güncel faiz, enflasyon, döviz, borsa ve fon getirilerini toplar.  
- **Ajan-3 (Risk Profili):** Müşterinin risk iştahı, yatırım süresi ve kayıp toleransına göre profil çıkarır.  
- **Ajan-4 (Karar Orkestratörü):** Önceki ajanlardan gelen çıktıları birleştirerek “bu portföy senin için uygun” önerisini sunar.  
- **Ajan-5 (Uyum Kontrolü):** Önerinin mevzuata, banka politikalarına ve müşteri limitlerine uygunluğunu kontrol eder.  

Sonuçta müşteri ekranında tek bir öneri görünür, fakat arka planda çok ajanlı orkestrasyon çalışmıştır.  

Farklı bir örnekte ise kredi onayı süreci; KYC/AML kontrolü, kredi skorlama, teminat doğrulama, mevzuat uyumu ve nihai onay adımları farklı ajanlara dağıtılarak modüler ve ölçeklenebilir bir yapı ile işletilebilir.  

**Trend ve Değerlendirme**  
- McKinsey’nin Haziran 2025’te yayımladığı *The Rise of Agentic AI* raporu, dikey odaklı çoklu ajanların iş akışlarını yeniden şekillendirdiğini vurguluyor.  
- Gartner’ın 2024 tarihli *Multi-Agent Collaboration in Finance* analizi, tek bir model yerine rol bazlı ajanların doğruluk ve hızda üstünlük sağladığını ortaya koyuyor.  
- OpenAI ve Anthropic’in 2025’te tanıttığı *multi-agent orchestration* deneyleri, bankacılıkta ilk kez müşteri uygulamalarına entegre edilmeye başlandı.  

Çok ajanlı mimari, bankacılığın kompleks süreçlerini “ajan fabrikası” mantığıyla modüler ve güvenli hale getiriyor.  

**Teknik Bileşenler**
- Olay tabanlı mikro servisler (Event-driven microservices: her ajan ayrı servis)  
- Bağlam yöneticisi (Context manager: ortak bağlam katmanı)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + güvenli prompt katmanı (guardrails)  
- Özellik deposu (Feature store: ortak veri özellik havuzu)  
- Gözlemlenebilirlik (Observability: telemetri, metrik, tracing)  
- Kimlik ve erişim yönetimi (IAM/ABAC: role-based & attribute-based access control)  
- Değiştirilemez denetim izi (Immutable audit log: her ajan adımının kaydı)  

**Ölçülebilir Etki (KPI)**
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Sahtekârlık engelleme ↑ · Kesinti süresi ↓ · Gelir/çalışan ↑

---

## **6. Dijital Finansal Düşünce Ortağı (Co-Thinker)**

**Tanım / Örnek Senaryo**  
“Dijital Finansal Düşünce Ortağı”, klasik bir ajan (agent) değil, karar destek ortağıdır. Kullanıcıya doğrudan “şunu yap” demek yerine, farklı açılardan düşünür, artı-eksi yönleriyle öneriler sunar. Amaç, rehberlik değil refleksiyon sağlamaktır. Örnek Senaryolar:  

- **Kullanım Senaryosu 1:** Kullanıcı “Bugün döviz almalı mıyım?” diye sorar → Sistem: “Almak mantıklı çünkü yarın maaşın yatıyor, likidite açığın yok. Ancak risk şu: kur volatilitesi yüksek, kısa vadede zarar görebilirsin.” der. 
- **Kullanım Senaryosu 2:**  Müşteri “Krediyi yapılandırmalı mıyım?” der → Sistem: “Aylık ödemen düşer ama toplam maliyetin artar.” der.  
- **Kullanım Senaryosu 3:** Müşteri “Biriktirmeye mi başlamalıyım, yoksa yatırıma mı yönelmeliyim?” diye danışır → Sistem: “Tasarruf fonu seni daha güvenli kılar, yatırım ise getiri potansiyeli sağlar.” diye yönlendirir. 

Bu yapı, müşterinin finansal farkındalığını artırarak kendi kararlarını daha bilinçli vermesine yardımcı olur.  

**Trend ve Değerlendirme**
- McKinsey’nin Haziran 2025’te yayımladığı *Seizing the agentic AI advantage* raporu, AI’nin sadece süreçleri otomatikleştirmekle kalmayıp, insan farkındalığını artırma rolünü de vurguluyor.  
- Accenture’un Ocak 2025 tarihli *Banking Top 10 Trends 2025* analizi, “augmented decision making” yaklaşımını bankacılığın yeni farklılaşma alanı olarak öne çıkarıyor.  
- Gartner’ın Ekim 2024’te yayımladığı *Top Strategic Technology Trends 2025* raporu, agentic AI yanında “decision intelligence” kavramını ön plana taşıyor.  
Bu yaklaşım, kararın sorumluluğunu müşteride bırakırken, yapay zekâyı bir “düşünce ortağı” olarak konumlandırıyor.  

**Teknik Bileşenler**
- Doğal dil anlama (NLU: Natural Language Understanding)  
- Bilgi getirme destekli üretim (RAG: Retrieval-Augmented Generation) + güvenli prompt katmanı (guardrails)  
- Açıklanabilir yapay zekâ (Explainable AI) → karar gerekçelerinin şeffaf sunumu  
- Politika-kod yaklaşımı (Policy-as-Code) → risk limitleri ve regülasyon kısıtlarının uygulanması  
- İnsan-içinde-döngü (Human-in-the-Loop) → kritik senaryolarda insan danışman entegrasyonu  
- Değiştirilemez denetim izi (Immutable audit log) → karar zincirlerinin kaydı  

**Ölçülebilir Etki (KPI)**
NPS ↑ · FCR ↑ · AHT ↓ · Müşteri bağımsızlık skoru ↑ · Operasyonel verimlilik ↑

---

## **7. AI-Driven Governance (Kurum Kendi Kendini Yönetir)**

**Tanım / Örnek Senaryo**  
“AI-Driven Governance”, kurum içi yönetişim mekanizmalarının bir kısmının otonom AI sistemlerine devredilmesi yaklaşımıdır. İnsan politika ve çerçeveyi belirlerken, uygulama ve taktiksel karar alma süreçleri yapay zekâ tarafından yürütülür. Bu yalnızca süreç otomasyonu değil, organizasyonel özerklik sağlar. Örnek Senaryolar:

- **Kredi başvuruları:** AI hafta içi beklenmedik artışı tespit eder → limit koyar, risk modellerini günceller ve yönetime özet rapor gönderir.  
- **Kampanya optimizasyonu:** Düşük performanslı segmentte kampanyayı durdurur, yüksek ROI vaat eden segmentlerde otomatik optimize eder.  
- **Operasyonel optimizasyon:** Altyapı kaynak kullanımını izler, gerektiğinde ölçekleme, throttling veya önceliklendirme kararlarını insan müdahalesi olmadan uygular.  

Nihai olarak finansal kuruluşun karar alma hızını artırır, riskleri daha erken yönetir, yönetim kadrosunu stratejiye odaklar.  

**Trend ve Değerlendirme**  
2025 itibarıyla bankacılıkta agentic AI-first mimarilere geçiş, yalnızca ürün geliştirme değil; karar döngülerinin otonom hale gelmesi açısından da kritik bir dönüşüm alanı olarak öne çıkıyor:  
- McKinsey’nin Haziran 2025’te yayımladığı *Digital Banking: Speed, scale, and the agentic arms race* raporu, bankaların agentic AI-first mimarilere yönelmesi gerektiğini ve karar döngüsünün otonom hale gelmesinin rekabet için kritik olduğunu vurguluyor.  
- Gartner’ın Ekim 2024 tarihli *Top Strategic Technology Trends 2025* raporu, agentic AI’ı en kritik teknoloji trendi olarak işaret ediyor ve self-governing (kendi kendini yöneten) sistemleri ön plana çıkarıyor.  
- Accenture’un Ocak 2025 tarihli *Banking Top 10 Trends 2025* analizi, rekabet avantajı için yalnızca ürünlerin değil, organizasyonel karar mekanizmalarının da AI ile dönüşmesi gerektiğini belirtiyor.  
- WSJ’nin Haziran 2025 tarihli *Digital Workers Have Arrived in Banking* haberi, BNY Mellon örneği üzerinden dijital çalışanların operasyonel karar süreçlerinde aktif görev aldığını aktarıyor.  

Bu gelişmeler birlikte değerlendirildiğinde, agentic AI artık yalnızca teknoloji yatırımı değil; karar döngülerinin yeniden tasarlanmasını zorunlu kılan stratejik bir dönüşüm alanı olarak görülüyor.  

**Teknik Bileşenler**
- Event-driven microservices → olay bazlı tetikleyiciler  
- Feature store → kredi, kampanya ve operasyon verilerinin tek kaynağı  
- RAG + güvenli prompt katmanı → karar gerekçelerinin şeffaf raporlanması  
- Human-in-the-Loop (HITL) → kritik noktalarda yönetici onayı  
- IAM / ABAC → karar yetkilendirmelerinin kimlik ve bağlama göre kontrolü  
- Immutable audit log → AI kararlarının şeffaf ve denetlenebilir kaydı  

**Ölçülebilir Etki (KPI)**
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel maliyet ↓ · Gelir/çalışan ↑
