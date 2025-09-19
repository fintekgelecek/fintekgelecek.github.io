# Yapay Zekâ ve Ajan Teknolojileri

Bu bölümde, yapay zekânın finansal hizmet süreçlerini nasıl dönüştürdüğüne odaklanan fikirleri topladım.

- **Otonom Finansal Ajanlar (Autonomous Finance Agents)**

**Tanım / Örnek Senaryo**  
Ajan, müşterinin aylık nakit akışını, yaklaşan fatura ve borçlarını, kart kesim tarihlerini ve piyasa koşullarını izler. Belirlenen hedefler doğrultusunda (likidite ≥ X, gecikme = 0, birikim = Y) planlama yapar ve gerekli eylemleri (ödeme talimatı, vadeliye geçiş, mikro-yatırım) kendi başına tetikler. Ardından denetim kaydı üretir, geri alma seçeneği sunar ve müşteriyi bilgilendirir.  
Müşterinin girdiği sınırlar (limitler, risk iştahı, yetkiler) **policy-as-code** yaklaşımıyla uygulanır. Banka tarafında ajan, uçtan uca süreçleri (ör. itiraz/chargeback) “toplayıcı → kararlayıcı → icracı” alt-ajanlar ile orkestre eder. “Onaylı otomasyon” ilkesiyle kritik adımlarda **HITL (human-in-the-loop)** kontrol noktaları bulunur.  

**Trend ve Değerlendirme**  
2025 itibarıyla agentik AI bankacılıkta operasyonel ölçeğe geçmiş durumda:  
- McKinsey’nin Haziran 2025 tarihli *Seizing the agentic AI advantage* raporu, dikey (vertical) ajanların karmaşık iş akışlarını otomasyona çekerek ölçekli değer yarattığını ve ajanın hedefe yönelik planlama kabiliyetini vurguluyor.  
- McKinsey’nin aynı ay yayımladığı *Digital Banking: speed, scale, and the agentic arms race* analizi, bankacılıkta ajanik yarışın “hız ve ölçek” ekseninde ilerlediğini ortaya koyuyor.  
- Ağustos 2025’te yayımlanan *Is agentic AI a financial crime game changer?* başlıklı rapor, finansal suçla mücadelede uçtan uca KYC/AML akışı için “ajan fabrikası” örneğini öne çıkarıyor.  

Bu üç rapor birlikte değerlendirildiğinde, teknolojinin artık bir “demo”dan çıkarak bankacılık operasyonlarının çekirdeğine yerleştiğini gösteriyor. Başka bir deyişle, ajanik AI bugün için rekabet avantajı değil, operasyonel gereklilik hâline geliyor.  

**Teknik Bileşenler**  
- Olay tabanlı mikro servisler + olay akışı (Event-driven microservices + event streaming)  
- Saga / telafi desenleri (Saga / compensation patterns)  
- Ajan orkestrasyonu (agent orchestration: planlama, araç kullanımı, görev ayrımı), araç çağırma (tool calling), policy-as-code (yetki, limit, zaman penceresi)  
- Bilgi getirme destekli üretim (Context/RAG: retrieval-augmented generation) + koruma önlemleri (guardrails: prompt/response doğrulama, güvenlik)  
- Özellik deposu (Feature store)  
- Model kayıt ve yönetişim (Model registry / governance)  
- Gözlemlenebilirlik (Observability: telemetri, metrik, izleme)  
- Risk ve adalet (Risk & fairness: bias detection)  
- İnsan denetim adımları (HITL control steps)  
- Değiştirilemez denetim izi (Immutable audit log)  

**Ölçülebilir Etki (KPI)**  
STP ↑ · AHT ↓ · FCR ↑ · NPS ↑ · Operasyonel kesinti ↓

- **Kişiselleştirilmiş AI Bankacı (Tokenize Finansal Kimlik)**

## Tanım / Örnek Senaryo
Müşteriye ait ve bankanın içinde çalışan bir “dijital bankacı” persona tanımlanır. Bu persona; risk iştahı, iletişim tonu, ödeme disiplini, hedefler ve yasaklar ile yapılandırılır.  
Niyet (**intent**) tespitinden gelen sinyallere dayanarak proaktif öneriler ve eylemler üretir:  
- “Bugün maaş yattı → otomatik birikim %X ayrıldı.”  
- “Kart kesimi yarın → likidite ayırdım.”  
- “Döviz kuru Y seviyesinin altına düştü → belirlediğin oranda mikro-alım yaptım.”  
- “Yaklaşan tatil için uçak bileti harcamanı takibe aldım → kredi kartı limitini geçici olarak yükselttim.”  

Tüm işlemler scope’lu yetki belirteçleriyle (scoped tokens) yürütülür ve geri alma seçeneği her zaman müşteriye sunulur.  

## Trend ve Değerlendirme
McKinsey’nin Haziran 2025 tarihli *Seizing the agentic AI advantage* raporu, “genel amaçlı copilots” yerine dikey ve süreç-özgü ajanların değer yarattığını ortaya koyuyor.  
Aynı dönemde yayımlanan *The future of customer experience: embracing agentic AI* analizi, kurumların müşteri deneyimini yeniden tasarlarken profil/niyet/olay sinyallerini gerçek zamanlı işleyen bir çekirdek veri omurgasına ihtiyaç duyduğunu vurguluyor.  

Bu perspektif, “AI bankası” yaklaşımının artık kavramsal bir vizyon değil, müşteri etkileşiminde operasyonel bir tasarım ilkesi hâline geldiğini gösteriyor.  

## Teknik Bileşenler
- Kimlik çözümleme (Identity resolution)  
- Olay akışı / değişim veri yakalama (Event streaming / CDC: change data capture)  
- Vektör temsilleri (Vector representations / embeddings)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + koruma önlemleri (guardrails)  
- Scope’lu yetki belirteçleri (Scoped tokens)  
- Model ve versiyon yönetişimi (Model/version governance)  
- Açık rıza ve izin yönetimi (Consent management)  
- Gözlemlenebilirlik (Observability: telemetri, metrik, izleme)  

## Ölçülebilir Etki (KPI)
Kişiselleştirilmiş teklif dönüşümü ↑ · Proaktif etkileşim ↑ · İlgisiz bildirim ↓ · NPS ↑

- **Intent-First Bankacılık (Niyet Tabanlı Orkestrasyon)**

## Tanım / Örnek Senaryo
Bugüne kadar dijital bankacılık sistemleri **API-first** mantığıyla kurgulandı: belirli bir işlem yapmak için kullanıcı doğru endpoint’i çağırmak zorundaydı. **Intent-first** yaklaşımında ise kullanıcı niyetini belirtir, sistem geri kalan işlemleri kendi başına orkestre eder.

**Müşteri örnekleri:**  
- “Yurt dışına çıkıyorum” dediğinde, sistem şu akışları otomatik tetikler:  
  - Döviz kuru önerisi ve anında dönüşüm  
  - Seyahat sigortası teklifi  
  - Kartın yurt dışı kullanım onayı  
  - Veri dolaşımı ve güvenlik kontrolü  
- “Ev almayı düşünüyorum” ifadesi: kredi ön-teklifi, ekspertiz süreci ve sigorta paketini aynı orkestrasyon katmanında toplar.  

**Banka çalışanı örneği:**  
- Müşteri temsilcisi “müşteri sadakat riski yüksek” intent’ini seçtiğinde, sistem proaktif kampanya, indirim veya iletişim stratejisini otomatik önerir.  
- Operasyon ekibi “yüksek sahtecilik riski” intent’i seçtiğinde, sistem ek doğrulama, anlık blokaj ve denetim adımlarını otomatik bağlar.  

Bu sayede işlem bazlı modüller yerine, niyet odaklı bütünleşik deneyim yaratılır.  

## Trend ve Değerlendirme
- McKinsey (Haziran 2025) ve Accenture (2025) raporları, bankacılıkta niyet tabanlı orkestrasyonun hiper-kişiselleşme ve operasyonel verimlilik için kritik hale geldiğini vurguluyor.  
- Gartner (2024), “AI-driven orchestration” trendini finansal hizmetlerde API-first paradigmasının ötesine geçiş olarak tanımlıyor.  
- WSJ (Haziran 2025), finans kurumlarının agentic AI ile modüler değil bütünleşik akışlar sunduğunu örneklerle aktarıyor.  

Bu gelişmeler birlikte değerlendirildiğinde, intent-first yaklaşımı müşteri deneyiminde basit bir inovasyon değil, rekabet için temel bir mimari değişim olarak öne çıkıyor.  

## Teknik Bileşenler
- Niyet tespiti ve sınıflandırma (Intent detection & classification: NLP tabanlı modeller)  
- Orkestrasyon motoru (Orchestration engine: workflow automation + policy-as-code)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + koruma önlemleri (guardrails)  
- Olay tabanlı mikro servisler (Event-driven microservices)  
- Kimlik ve erişim yönetimi (IAM: Identity & Access Management) + öznitelik tabanlı erişim kontrolü (ABAC: Attribute-Based Access Control)  
- Değiştirilemez denetim izi (Immutable audit log)  

## Ölçülebilir Etki (KPI)
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel kesinti ↓ · Gelir/çalışan ↑ · Müşteri memnuniyeti ↑

- **Yapay Zekâyla Yönetilen Mikrobankalar**

## Tanım / Örnek Senaryo
“Her müşteri kendi bankasını yaratır” fikri, klasik “tek tip ürün/arayüz” yaklaşımını yıkar.  
Müşteri onboarding sırasında AI tabanlı bir **mikro-banka kurulum asistanı** ile karşılaşır. Bu asistan, müşterinin:  
- Risk toleransı  
- Hedefleri  
- İletişim tercihleri (ör. SMS yerine WhatsApp veya yalnızca mobil bildirim)  
- Dil seçimi  
- Ürün tercihleri (ör. faizsiz ürünler, sürdürülebilir yatırımlar)  

gibi parametreleri sorar ve bu verilerle kişisel **mikro-banka profili** oluşturur.  

**Örnek müşteri tipleri:**  
- Emekli → düşük risk, düşük sürtünme; düzenli ödeme hatırlatıcıları ve tasarruf odaklı öneriler.  
- Girişimci → yüksek risk toleransı; nakit akışı tahmini, yatırım fırsatları, vergi hatırlatıcıları.  
- Öğrenci → düşük bütçe yönetimi; harcama limiti önerileri, mikro-tasarruf planları, kampüs odaklı teklifler.  

Arka planda bankanın AI orkestrasyonu, her müşteriye özel mikrobankacılık akışlarını yönetir. Bu bir UI özelleştirmesinden öte, davranışsal otomasyon ve niyet tabanlı orkestrasyon anlamına gelir.  

Banka tarafında “mikrobankalar” toplulaştırıldığında kurumun elinde binlerce farklı müşteri-bankası senaryosu olur. Bu çeşitlilik, ürün geliştirme ve müşteri segmentasyonu için benzersiz bir öğrenme kaynağına dönüşür.  

## Trend ve Değerlendirme
- McKinsey (2025), hiper-kişiselleşmenin bankacılıkta farklılaşmanın tek sürdürülebilir yolu olduğunu vurguluyor.  
- Gartner (2024), müşteri başına “AI-curated experience layer” trendini öne çıkarıyor.  
- Accenture (2025), “AI-personalized banking instances” kavramını ölçeklenebilir müşteri deneyimi inovasyonu olarak tanımlıyor.  
- WSJ (2025), finans kurumlarının artık “tek uygulama” değil, kişiselleşmiş mikro-hizmet kümeleri üzerinden değer yarattığını aktarıyor.  

Bu gelişmeler, mikrobankacılığın yalnızca müşteri arayüzü değil, bankacılığın çekirdek iş modeli dönüşümü olduğuna işaret ediyor.  

## Teknik Bileşenler
- Persona kurucu + AI orkestrasyonu (Persona builder + AI orchestration)  
- Politika-kod yaklaşımı (Policy-as-code: risk ve ürün seçim limitlerinin şeffaf uygulanması)  
- Bilgi getirme destekli üretim (Context/RAG: retrieval-augmented generation)  
- Olay tabanlı mikro servisler (Event-driven microservices: profil bazlı tetikleme)  
- Kimlik ve erişim yönetimi (IAM/ABAC: Identity & Access Management / Attribute-Based Access Control)  
- Değiştirilemez denetim izi (Immutable audit log: kişiselleştirilmiş tüm akışların kaydı)  

## Ölçülebilir Etki (KPI)
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel kesinti ↓ · Gelir/çalışan ↑ · Churn ↓

- **Zincirleme Finansal Ajanlar (Multi-Agent Orchestration)**

## Tanım / Örnek Senaryo
“Zincirleme Finansal Ajanlar”, farklı uzmanlık rollerinde çalışan birden fazla AI ajanın çıktılarının orkestre edildiği yapıdır. Tek bir “süper ajan” yerine, her biri belirli göreve odaklanan mikro-ajanlar aynı bağlam üzerinde iş birliği yapar.

**Müşteri örneği:**  
Müşteri mobil uygulamadan “yatırım yapmak istiyorum” der:  
- **Ajan-1 (Finansal Analiz):** Mevcut nakit akışı, likidite ve borç/gelir oranını inceler.  
- **Ajan-2 (Piyasa Taraması):** Güncel faiz, enflasyon, döviz, borsa ve fon getirilerini toplar.  
- **Ajan-3 (Risk Profili):** Müşterinin risk iştahı, yatırım süresi ve kayıp toleransına göre profil çıkarır.  
- **Ajan-4 (Karar Orkestratörü):** Önceki ajanlardan gelen çıktıları birleştirerek “bu portföy senin için uygun” önerisini sunar.  
- **Ajan-5 (Uyum Kontrolü):** Önerinin mevzuata, banka politikalarına ve müşteri limitlerine uygunluğunu kontrol eder.  

Sonuç: Müşteri ekranında tek bir öneri görünür, fakat arka planda çok ajanlı orkestrasyon çalışmıştır.  

**Banka örneği:**  
Kredi onayı sürecinde; KYC/AML kontrolü, kredi skorlama, teminat doğrulama, mevzuat uyumu ve nihai onay adımları farklı ajanlara dağıtılarak modüler ve ölçeklenebilir bir yapı sağlanır.  

## Trend ve Değerlendirme
- McKinsey (2025) *The Rise of Agentic AI* raporu, dikey odaklı çoklu ajanların iş akışlarını yeniden şekillendirdiğini vurguluyor.  
- Gartner (2024), tek bir model yerine rol bazlı ajanların doğruluk ve hızda üstünlük sağladığını belirtiyor.  
- OpenAI ve Anthropic’in 2025’te tanıttığı “multi-agent orchestration” deneyleri, bankacılıkta ilk kez müşteri uygulamalarına entegre edilmeye başlandı.  

Çok ajanlı mimari, bankacılığın kompleks süreçlerini “ajan fabrikası” mantığıyla modüler ve güvenli hale getiriyor.  

## Teknik Bileşenler
- Olay tabanlı mikro servisler (Event-driven microservices: her ajan ayrı servis)  
- Bağlam yöneticisi (Context manager: ortak bağlam katmanı)  
- Bilgi getirme destekli üretim (RAG: retrieval-augmented generation) + güvenli prompt katmanı (guardrails)  
- Özellik deposu (Feature store: ortak veri özellik havuzu)  
- Gözlemlenebilirlik (Observability: telemetri, metrik, tracing)  
- Kimlik ve erişim yönetimi (IAM/ABAC: role-based & attribute-based access control)  
- Değiştirilemez denetim izi (Immutable audit log: her ajan adımının kaydı)  

## Ölçülebilir Etki (KPI)
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Sahtekârlık engelleme ↑ · Kesinti süresi ↓ · Gelir/çalışan ↑

- **Dijital Finansal Takma Akıl (Co-Thinker)**

## Tanım / Örnek Senaryo
“Dijital Finansal Takma Akıl”, klasik bir ajan (agent) değil, karar destek ortağıdır. Kullanıcıya doğrudan “şunu yap” demek yerine, farklı açılardan düşünür, artı-eksi yönleriyle öneriler sunar. Amaç, rehberlik değil refleksiyon sağlamaktır.

**Örnek senaryolar:**  
- Kullanıcı “Bugün döviz almalı mıyım?” diye sorar → Sistem: “Almak mantıklı çünkü yarın maaşın yatıyor, likidite açığın yok. Ancak risk şu: kur volatilitesi yüksek, kısa vadede zarar görebilirsin.”  
- Müşteri “Krediyi yapılandırmalı mıyım?” der → Sistem: “Aylık ödemen düşer ama toplam maliyetin artar.”  
- Müşteri “Biriktirmeye mi başlamalıyım, yoksa yatırıma mı yönelmeliyim?” diye danışır → Sistem: “Tasarruf fonu seni daha güvenli kılar, yatırım ise getiri potansiyeli sağlar.”  

Bu yapı, müşterinin finansal farkındalığını artırarak kendi kararlarını daha bilinçli vermesine yardımcı olur.  

## Trend ve Değerlendirme
- McKinsey (Haziran 2025), AI’nin sadece otomasyon değil, insan farkındalığını güçlendirme rolünü de vurguluyor.  
- Accenture (Ocak 2025), “augmented decision making”i bankacılığın yeni farklılaşma alanı olarak öne çıkarıyor.  
- Gartner (Ekim 2024), agentic AI yanında “decision intelligence” kavramını ön plana taşıyor.  

Bu yaklaşım, kararın sorumluluğunu müşteride bırakırken, yapay zekâyı bir “düşünce ortağı” olarak konumlandırıyor.  

## Teknik Bileşenler
- Doğal dil anlama (NLU: Natural Language Understanding)  
- Bilgi getirme destekli üretim (RAG: Retrieval-Augmented Generation) + güvenli prompt katmanı (guardrails)  
- Açıklanabilir yapay zekâ (Explainable AI) → karar gerekçelerinin şeffaf sunumu  
- Politika-kod yaklaşımı (Policy-as-Code) → risk limitleri ve regülasyon kısıtlarının uygulanması  
- İnsan-içinde-döngü (Human-in-the-Loop) → kritik senaryolarda insan danışman entegrasyonu  
- Değiştirilemez denetim izi (Immutable audit log) → karar zincirlerinin kaydı  

## Ölçülebilir Etki (KPI)
NPS ↑ · FCR ↑ · AHT ↓ · Müşteri bağımsızlık skoru ↑ · Operasyonel verimlilik ↑


- **AI-Driven Governance (Kurum Kendi Kendini Yönetir)**

## Tanım / Örnek Senaryo
“AI-Driven Governance”, kurum içi yönetişim mekanizmalarının bir kısmının otonom AI sistemlerine devredilmesi yaklaşımıdır. İnsan yöneticiler politika ve çerçeveyi belirlerken, uygulama ve taktiksel karar alma süreçleri yapay zekâ tarafından yürütülür. Bu yalnızca süreç otomasyonu değil, organizasyonel özerklik sağlar.

**Örnek senaryolar:**  
- **Kredi başvuruları:** AI hafta içi beklenmedik artışı tespit eder → limit koyar, risk modellerini günceller ve yönetime özet rapor gönderir.  
- **Kampanya optimizasyonu:** Düşük performanslı segmentte kampanyayı durdurur, yüksek ROI vaat eden segmentlerde otomatik optimize eder.  
- **Operasyonel optimizasyon:** Altyapı kaynak kullanımını izler, gerektiğinde ölçekleme, throttling veya önceliklendirme kararlarını insan müdahalesi olmadan uygular.  

Sonuç: Banka karar alma hızını artırır, riskleri daha erken yönetir, yönetim kadrosunu stratejiye odaklar.  

## Trend ve Değerlendirme
- **McKinsey (2025):** Bankaların “agentic AI-first” mimarilere geçmesi gerektiğini, karar döngüsünün otonom hale gelmesinin kritik olduğunu vurguluyor.  
- **Gartner (2024):** Agentic AI’ı en kritik teknoloji trendi olarak belirtiyor; self-governing (kendi kendini yöneten) sistemler öne çıkarılıyor.  
- **Accenture (2025):** Rekabet avantajı için yalnızca ürün değil, organizasyonel karar mekanizmalarının da AI ile dönüşmesi gerektiğini söylüyor.  
- **WSJ (2025):** BNY Mellon örneğiyle, “dijital çalışanlar”ın operasyonel karar süreçlerinde aktif görev aldığını aktarıyor.  

## Teknik Bileşenler
- Event-driven microservices → olay bazlı tetikleyiciler  
- Feature store → kredi, kampanya ve operasyon verilerinin tek kaynağı  
- RAG + güvenli prompt katmanı → karar gerekçelerinin şeffaf raporlanması  
- Human-in-the-Loop (HITL) → kritik noktalarda yönetici onayı  
- IAM / ABAC → karar yetkilendirmelerinin kimlik ve bağlama göre kontrolü  
- Immutable audit log → AI kararlarının şeffaf ve denetlenebilir kaydı  

## Ölçülebilir Etki (KPI)
NPS ↑ · STP ↑ · AHT ↓ · FCR ↑ · Operasyonel maliyet ↓ · Gelir/çalışan ↑
