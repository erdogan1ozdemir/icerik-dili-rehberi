# Negatif Bulgu, Rakip Dili, Veri Kısıtı, Marka-Güvenli Çıktı, Kanal ve Tür-Özel Kurallar

## 1. Negatif Bulgu Çerçevelemesi

Negatif veri saklanmaz; üç stratejiyle sunulur:

1. **Nötr teknik fiil sözlüğü:** düşüş, gerileme, daralma, dalgalanma, baskı, ayrışma, sapma, zayıflama, sınırlı kalmıştır, eksilme. ("Kötü/başarısız/çöktü" yok.)
2. **Bağlama bağlama (dürüst dışsallaştırma):** düşüş teknik/mevsimsel/pazar nedenine bağlanır - ama neden gerçekten destekleniyorsa: "Bu durum performans kaybından ziyade kategori bazlı talep küçülmesine işaret etmektedir", "Ağustos spam update'i geçici dalgalanmalara yol açmış; Aralık itibarıyla görünürlük yeniden ivme kazanmıştır."
3. **Kontrast / telafi cümlesi:** negatif metrik, dayanıklılık gösteren metrikle yan yana verilir: "Session -%11 daralırken Revenue +%19 artmıştır", "9 rakipten 9'u görünürlük kaybı yaşarken marka +%0.3 ile sektörden ayrışmaktadır."

- En sert eleştiri seviyesi "dikkat çekmektedir" kalıbıdır: "Sepete eklendiği halde checkout'a geçmeyen sayfalar dikkat çekmektedir."
- Dikkat gerektiren maddeler ▲ ile işaretlenir ve nötr betimlenir: "▲ Direct kanal revenue düşüşü - Sessions +%313 olmasına rağmen Revenue -%42".
- Beklenti kıyası hafifletici olarak kullanılabilir: "Domain birleştirmede beklenen %10-30 kayıp seviyesinin çok altında, -%2.6."
- Migrasyon/değişim analizlerinde pozitif ve negatif etkiler yan yana, simetrik pencereyle verilir; taraf tutulmaz. Kazanım/kayıp simetrik blok şablonu kullanılabilir: "Geçiş Etkisi - Kazanımlar" / "Geçiş Etkisi - Kayıplar" başlıkları altında aynı cümle iskeleti.
- Yıldızlı bağlam/güncelleme dipnotu tekniği: düşüşün nedeni veya sonraki durumu dipnotla bağlanır: "*2025 Aralık ayında domain geçişi gerçekleşmiştir.", "***Güncelde (Şubat sonu itibarıyla) bu düşüşler düzelmiştir."

---

## 2. Rakip / Karşılaştırma Dili

- Aşağılayıcı karşılaştırma yasak. Rakip zayıflığı marka fırsatı olarak çerçevelenir:
  - "X zayıf" → "X belirli alanlarda öne çıkarken başka alanlarda büyüme potansiyeli taşımaktadır."
  - "X bunu yapıyor, siz yapmıyorsunuz" → "X ilgili alanda çalışıyor; markanın bu alanı değerlendirmesi fırsat sunabilir."
- Rakip güçlüyse açıkça söylenir, ihtiyat ekiyle ve aksiyona bağlanarak: "MediaMarkt, yüksek hacimli Apple odaklı kelimelerde ilk sıralara güçlü şekilde yerleşmiş görünmektedir; TV+ köprüsüyle ilgili trafiğin içeriğe çevrilmesi değerlendirilebilir."
- Aktörler ve markalar isimle belirtilir; "bazı rakipler" denmez: "Koçtaş, Kale, Bauhaus ve Creavit ilk 10'da yer alıyor."
- Ürün/segment boşluğu nötr ve olgusal verilir: "Talebin yoğunlaştığı granit evye segmentinde markanın ürünü bulunmuyor; bu alan bugün Franke ve Blanco'da öne çıkıyor ve değerlendirilmeye açık bir fırsat sunuyor."
- Standart anlatım kalıbı: **kim satıyor → nasıl konumlanmış → markada karşılığı var mı, ne kadar var.**
- Hipotez-sonuç formatı kullanılabilir: "Hipotez: Yavaş site = yüksek bounce. Sonuç: …"
- Rakip domain listesi tek tek dökülmez; URL örneği + KD aralığı + hacim bandı yeterli olabilir.
- "Ele geçirmek, koparmak, domine etmek" gibi agresif fiiller kullanılmaz.

---

## 3. Veri Eksik / Ölçüm Kısıtı Politikası

**Ana kural: eksik veri raporda yumuşatılmış cümlelerle maskelenmez.** "Bu bölüm için ek veri toplanması planlanabilir", "Detaylı ölçüm bir sonraki aşamada derinleştirilebilir", "X bu turda erişime kapalıydı" gibi doldurma iletişimleri rapora yazılmaz. Bunun yerine üç adımlı akış:

1. **Chat'ten bildir:** Veri çekilemediyse / API-araç kısıtı varsa / kaynak taranamadıysa durum raporun içine değil, chat üzerinden kullanıcıya açıkça bildirilir.
2. **Manuel veri iste:** Kullanıcıdan ilgili verinin manuel eklenmesi/iletilmesi istenir.
3. **Eklenemiyorsa alanı kaldır:** Veri sağlanamıyorsa ilgili alan/bölüm rapordan komple çıkarılır ve bu kaldırma da chat'te "önemli" olarak ayrıca belirtilir.

Ek kurallar:
- Rapora boş bölüm, placeholder metrik veya "sonraki aşamada eklenecek" vaadi bırakılmaz.
- Örneklem üzerinden çalışıldıysa dürüst ve sade beyan: "Bu bölüm tüm veriler değil, mevcut örnek üzerinden değerlendirilmiştir."
- **Dramatik kıyas ifadeleri yasak:** "X kat küçümseme", "N kat sapıyor", "aracın verisi güvenilmez" tarzı ifadeler hiçbir çıktıda kullanılmaz. Araçlar arası fark varsa sayılar yorumsuz yan yana verilir veya tek kaynak seçilip diğeri çıkarılır.
- Veri gerçekten yetersizse uydurulmaz; varsayım rakamı yazılmaz.
- Gerçek maliyet verisi yoksa maliyet/bütçe dili tamamen çıkarılır → trafik bazlı yüzde dağılımı kullanılır.
- "LCP iframe'den ölçülemiyor" gibi iç kısıtlar rapora yazılmaz; raporu sunacak kişiye chat üzerinden ayrıca belirtilir/iletilir.
- Çelişkili veride yaklaşım "doğrula + uzlaştır": doğrulanamayan sayı temel alınmaz, şeffaf rozetle işaretlenir ("doğrulanamadı"). Bir kaynak "tutarsız" diye yaftalanmadan önce kontrol edilir; belirsizlik adil çerçevelenir ("yüzdeler AI üretimi, tema düzeyinde kullanıldı").

---

## 4. Marka-Güvenli Çıktı (rapor markaya gidiyor)

- **Araç adı kuralı iki katmanlıdır:**
  - **Yerleşik veri kaynağı araçları** (GSC, GA4, SEOmonitor, Ahrefs, Keyword Planner) kaynak notu olarak yazılabilir ("Kaynak: SEOmonitor", "Hata (Ahrefs Issue)"); her slaytta tekrarlanmaz, bir kez yöntem notu + en altta yeterlidir.
  - **Otomasyon / üretim araçları** (Claude, Claude Code, MCP, skill, Playwright, "Inbound Visibility Tool") müşteri çıktısında asla görünmez. DataForSEO proje tercihine göre jenerikleştirilir ("DfS Doğrulama", "arama motoru veri kaynağı").
- İçsel araç seçimi ve hata gerekçesi ifşa edilmez; yöntem olumlu çerçevelenir: "DataForSEO hata verdiği için Ahrefs kullanıldı" değil "İlgili kelimeler ve trafik verisi analiz edildi."
- Analistin operasyonel adımları anlatılmaz ("önce dosyayı çektim, sonra temizledim" yok); süreç edilgen çatıyla verilir: "listelendi, ölçüldü, karşılaştırıldı, belirlendi." Metodoloji kalıbı: **[Yöntem] ile [aktörler isimle] için [ne yapıldı] → [sonuç].**
- Metodoloji jargonu sadeleştirilir: "breadcrumb + slug token overlap, örtüşmesiz" değil; "İlişkili ürünler, aynı marka ya da kategoriye bağlı ürün sayfalarıdır; her ürün yalnızca bir kez sayılır."
- Önemli notlar görünür ve yapısal: etiketli **NOT / YÖNTEM** blokları halinde, metin içinde kaybolmaz.
- **Kapak kuralı kanala göre ayrışır:** Doküman, HTML rapor ve Excel çıktıları kapak süsü, dekoratif ayraç çizgisi veya "Hazırlayan / Prepared by" bölümü içermez; doğrudan içerikle başlar. Sunumlarda (PPTX) ise kapak slaytı + "SUNUM AKIŞI" ajandası ev standardıdır ve korunur.
- **Tüm sunumlar markaya gidecek varsayımıyla hazırlanır; ayrı bir "iç sürüm" yoktur.** Her tabloya yorum eklenir, her negatife bağlam iliştirilir, taahhüt yerine "Q2 önceliği olarak değerlendirilebilir" düzeyinde öneri verilir. Süreç mutfağı (toplantı rutinleri, erişim süreçleri, iş takip detayları) sunuma yazılmaz. Konuşmacı notlarına iç açıklama bırakılmaz; teslim öncesi notlar taranır/temizlenir.
- İç süreç etiketleri ve dosya adı konvansiyonları müşteri destesine sızdırılmaz: "Blocked / In Progress / Not Started" yerine Türkçe şeffaf durum ("Beklemede / Devam Ediyor / Planlandı"); slayt içi linklerde "(Shared) … // Inbound" gibi iç adlandırmalar temizlenir.
- İç kısıtlar ("LCP iframe'den ölçülemiyor", "veri çekilemedi") rapora yazılmaz; raporu sunacak kişiye chat üzerinden ayrıca iletilir.

---

## 5. Sunum Yapısı ve Akış Ritüelleri

Ev üslubunun sabit iskeleti (değerlendirme sunumları):

1. Kapak: "Marka | [Dönem] [Konu]"
2. "SUNUM AKIŞI" - numaralı içindekiler (01, 02, …)
3. "Nelere Odaklandık? / Neler Yaptık?" - dönem işlerinin isim cümleli listesi (efor kanıtı)
4. Veri bölümleri (pazar → GSC → GA4 → AI trafik → sıralama/görünürlük)
5. Yönetici özeti kullanılacaksa başta: KPI kartları + "KRİTİK TESPİT" kutusu + ✓/▲ işaretli "Dönemin Öne Çıkanları"
6. Kapanış: "[Yıl] Planları" veya numaralı öneri seti (01-06) - giriş ve bitiş dolgu slaytlarına gerek yok
7. Son slayt: "Teşekkürler"

- **Kapanış "özetleyelim" ile değil, bir sonraki adımla yapılır:** "Bu sunumdan sonra ilk adım olarak şu 3 nokta değerlendirilebilir: …" Eğitim sunumlarında karşılığı "Durum & Sonraki Adımlar" / "Akılda Kalması Gerekenler" slaytıdır.
- Tanım/metodoloji kutuları şablonlaşabilir ve tekrar edebilir (GSC Impression/Click tanımı, SEOmonitor Visibility formülü) - tutarlı tekrar sorun değildir.
- Karşılaştırmalı analizlerde metodoloji paragrafı açıkça slayta yazılır: "Time range ve metodoloji: Geçiş öncesi karşılaştırma için … Kasım 2025 ortalamasına bakıldı. Tüm sıralamalar mobil olarak ele alındı."
- Wall-of-text yok: bullet list, kısa başlık, kart/blok grid, etiketli not. Uzun bullet listeleri accordion'da ("Detayları göster ▾") verilebilir.
- Bir bullet = bir fikir, tek cümle. Aksiyon/öneri/adım sıralamaları daima madde listesi; bağlam metinleri paragraf olabilir.
- Sayı gerçek dünya bağlamına oturtulur: "Kasım ayı Efsane Cuma kampanya dönemiyle en yüksek ciroyu oluşturmuş; Mayıs bayram etkisiyle bu seviyeyi aşmıştır."

---

## 6. Sunum / Doküman Türüne Göre Ton Ayarları

Genel kuralları ezmez; örnekler ve vurgular ekler.

### 6.1. SEO / GEO değerlendirme (çeyreklik rapor)
- **Bulgu → yorum → potansiyel aksiyon** akışı korunur. Aksiyonlar plan olarak sertleştirilmez; öneri olarak sunulur.
- Her veri slaytında ➔ insight; her tabloda yorum katmanı (yorumsuz tablo bırakılmaz - müşteri sürümü kuralı).

### 6.2. Paid + Organic sentez
- Paid tarafta bold öneri olmaz; bulgu aktarılır, öneri kipiyle iletilir.
- Maliyet verisi yoksa maliyet dili tamamen çıkarılır → trafik bazlı yüzde.
- Harici faktörler ölçülü: "…kısmen bu dönemin etkisiyle oluştuğu değerlendirilebilir."

### 6.3. Migrasyon / değişim analizleri (SSR, domain geçişi vb.)
- Simetrik pencere karşılaştırması yapıldığı belirtilir; pozitif/negatif etkiler yan yana.
- Karşılaştırma penceresi her veri slaytının altında sabit dipnotla tekrarlanır: "SSR Öncesi: 6 Ocak - 11 Şubat 2026 | SSR Sonrası: 12 Şubat - 22 Mart 2026 | Geçiş Tarihi: 12 Şubat 2026".
- Segment bazında (Brand / Non-Brand / Blog / cihaz / sayfa tipi) ayrıştırılır; segment tanımı şeffaf yazılır: "Brand = gameplus, game+, game plus", "GFN terimleri 3. parti marka olarak non-brand'e dahil edildi."
- Beklenti kıyası kullanılabilir ("beklenen %10-30 kaybın altında").
- Başarı atfı yumuşatılır ("SSR'ın pozitif etkisinin göstergesi olarak değerlendirilebilir"); dış bağlam savunma argümanı olarak kullanılabilir ("arama hacmi -%19 düşerken görünürlüğün korunması").

### 6.4. GEO / AI search odaklı sunumlar
- **"Korkutma → çözüm" değil, "değişimi anlama → fırsatı görme → harekete geçme"** akışı. Tehdit veri olarak verilir, hemen fırsata çevrilir: "Üst sırada olmak artık tıklama getirmiyor; yeni hedef, AI cevabında kaynak olarak seçilmek."
- Rakamlar zaten çarpıcı; ekstra dramatize edilmez. Dengeleme cümlesi eklenir: "bilgi amaçlı içerikte tıklama kaybı artarken, ticari ve marka aramalarında etki daha sınırlı."
- Türkçe kalır: AI Mode Yanıtı, Takip Sorusu, Kaynak Paneli. İngilizce kalır: Query, Citation, Mention, SoV, Visibility.
- **Mention ≠ Citation ayrımı** net kutucukta ayrıştırılır (anılma vs atıf alma).
- Global/yerel kapsam netliği: bir düzenlemenin global mi ülkeye özel mi olduğu açıkça yazılır ("Türkiye notu" kutusu).

### 6.5. Rakip / benchmark analizleri
- Kesin hüküm yok; hipotez-sonuç formatı kullanılabilir; rakip zayıflığı marka fırsatı olarak çerçevelenir (bkz. Bölüm 2).
- Görünürlük payının düşük göründüğü kesitlerde metodolojik açıklama eklenir: "çalışma bilinçli olarak markanın öne çıkmadığı açık alana odaklanmaktadır."

### 6.6. Sosyal dinleme / algı raporu [B]
- Sade, günlük Türkçe; jargon çevrilir. Yüzdeler "yön gösterir, kesin ölçüm değildir" uyarısıyla; sessiz çoğunluğun temsil edilmediği belirtilir.
- Kullanıcı alıntıları birebir korunur (sert/argo dahil), kısa tutulur ve kaynaklanır; raporun kendi sesi nötrleştirilir: alıntı "resmen kandırmak" derken anlatım "kullanıcılar bunu güven kaybı olarak yorumluyor" der.
- Güncel tepki öne; tarih penceresi net; mecra farkı belirtilir (şikayet sitesi ≠ forum ≠ YouTube).
- Yöntem şeffaflığı: hangi araç aileleriyle, kaç adımda çalışıldığı yazılır (araç adları marka-güvenli düzeyde).

### 6.7. AI trafik / analitik rapor
- Fırsat çerçevesi: "Dönüşmeyen sayfalar" değil "Dönüşüm Fırsatı sayfaları".
- Aksiyon adları açık ve kapsayıcı: "GEO İçerik" değil "İçerik Üretimi - Kategori & Ürün".
- Kapsam/sınır dürüst: örneklem, kısmi ay, yaklaşık eşleşme açıkça belirtilir; sayı olduğundan büyük gösterilmez.

### 6.8. Trafik fırsatları / content gap raporu
- Fırsat dili, tahmin değil; hedef click bant olarak ("150-250K ek aylık tık").
- Türkçe hub adları ("Hesaplama Hub'ı"); marka terimleri doğru yazım (Pasaj, TV+, GAME+, lifebox, Superonline).
- Kapsam dışı içerik sızmaz (fal, cezaevi rehberi, hedefsiz genel hub'lar); "bölümün stratejik değeri" tarzı retorik ara not yok.
- Yol haritası fazlarla verilir: Faz 1 Hızlı Kazanım / Faz 2 Yeni Yetkinlik / Faz 3 Otorite Genişletme. Faz sayısı duruma göre artırılıp azaltılabilir; fazlara ay/tarih aralığı yazılmaz.

### 6.9. Eğitim / bilgilendirme sunumu (Google yenilikleri vb.)
- Nötr-analist ton; geniş şimdiki zaman ("-ıyor"). İddialar kaynağa atfedilir ("Google'a göre iki katına çıkıyor").
- Her içerik slaytının sonunda ➔ sentez satırı ("so what" cümlesi).
- Terimler `** terim: tanım` dipnotuyla; büyük rakam kartı + tek cümle açıklama kalıbı; her slaytta "Kaynak:".
- Markalara dönük çıkarımlar "-abiliyor / avantaj sağlayabilir" kipiyle.

### 6.10. Pitch / tanıtım sunumu (yeni iş)
- Tek istisna rejim: birinci çoğul "biz" anlatısı ve hikaye dili serbesttir ("ekibinizin bir parçası olarak konumlanırız").
- **Vaat disiplini korunur:** süreç vaatleri geniş zamanla net ("tasarlar ve uygularız"), sonuç vaatleri "-abilir" ile ("ziyaretleri destekleyebiliriz"); "sağlayacağız / artıracağız" gibi kesin gelecek zaman sonuç vaadi verilmez.
- Kanıt-temelli pitch: müşteriye özel mini denetim bulguları güçlü bir araçtır; bulgular yine nötr dille verilir.
- Case study kartlarında metrikler dönem + baz değer bağlamıyla verilir; kaynak disiplini pitch'te de korunur.
- Sorunlaştırma korkutmadan yapılır; fırsat maliyeti dili kullanılır.

### 6.11. Teknik / PageSpeed optimizasyon sunumu (CWV, CLS, LCP vb.)
- **Katmanlı bulgu anlatımı:** tespit → mekanizma/neden → kullanıcıya etkisi → çözüm. Örnek iskelet: "Bazı web fontlarında font-display ayarı bulunmuyor. Bu nedenle tarayıcı, font inene kadar metinleri gizli tutuyor. Bu durum metinlerin geç görünmesine ve FCP'nin gecikmesine yol açıyor. Tüm fontlara font-display: swap eklenebilir."
- **Kip ayrımı net uygulanır:** ölçülmüş etki bildirme kipiyle ("Bu durum CLS değerini olumsuz yönde etkilemektedir", "17,059 KiB olarak ölçülmüştür"); yalnızca potansiyel/koşullu etkiler "-ebilir" ile ("Aşağıdaki faktörler LCP puanını olumsuz etkileyebilir").
- Çözüm ayrı etiketle işaretlenir ("Çözüm:"); etkilenen element/CSS class adları verbatim listelenir; uygulanabilir kod örneği slayta gömülebilir (kopyala-yapıştır seviyesinde somutlaştırma).
- Bakım/raf ömrü uyarısı eklenir: "Önemli Not: Sayfa tasarımının değişeceği bir durumda bu alanlar yeni tasarıma göre güncellenmelidir."
- Görsel yönlendirme kalıbı ("Aşağıdaki görselde … inceleyebilirsiniz") kullanılabilir; ancak tespitin özü metinde de yazılır - bulgu tamamen görsele delege edilmez.
- Eşik değerler öneri cümlesine gömülür ve resmi eşikler (CLS 0.1, LCP 2.5s) tanım slaytında verilir; dokümantasyon kaynağı "Kaynak: https://web.dev/…" ile bağlanır.
- Ölçüm kısıtları rapora yazılmaz; sunacak kişiye chat'ten iletilir (bkz. Bölüm 3 ve 4).

### 6.12. Aylık statü / proje sunumu (çalışma toplantısı)
- İki kip bir arada kullanılır: **tamamlanan işler** edilgen geçmiş zaman ("proje planları oluşturuldu", "tool kurulumları gerçekleştirildi"); **planlanan işler** "-ması/-mesi" isim-fiil listesi ("Kategori ağacı önerileri çıkarılması") + parantezli durum notu ("(Kanyon - Bekliyor)").
- Proje sağlığı yorumlarında birinci çoğul, dürüst çalışma dili kabul edilir ("Mevcut eforu full kullanarak ilerleyebiliyoruz", "IT tarafındaki işler beklenenden yavaş ilerliyor"); yine de "sıkıntı/sorun" yerine ölçülü karşılıklar tercih edilir.
- Kaynak/efor ihtiyacı koşullu cümleyle iletilir: "Taleplerin benzer devam ettiği durumda ek kaynak ihtiyacı oluşabilir."
- Bu rejim yalnızca çalışma toplantısı destelerinde geçerlidir; çeyreklik değerlendirme sunumuna taşınmaz.

---

## 7. Kanal-Özel Kurallar: HTML Rapor & Excel Audit

### 7.1. HTML rapor

- İlk geçen teknik terim: `<span class="term" data-term="KD">Keyword Difficulty (KD)</span>`. Glossary'de tanımlı terimler: KD, DR, SERP, AI Overview, SGE, GEO, Schema / JSON-LD, Canonical, llms.txt, robots.txt (GPTBot / Google-Extended / PerplexityBot), sitemap.xml, dateModified, LCP, CLS, INP, CWV, GSC, GA4, Indexability, Crawl Budget, Internal Linking, Backlink, Anchor Text, Share of Voice, Mention, Citation, Zero-click, Fan-out Query, PAA, Knowledge Panel, GMB, Breadcrumb, FAQPage Schema, AggregateOffer, Impression, CTR, Visibility Score, Content Gap, Intent, Long-tail, Meta Description, Title Tag, H1, Market Cluster, machine-readable. Glossary dışı terim için span kullanılmaz - düz yazılır.
- Tüm işaretli terimler sonda "Terim Sözlüğü" bölümünde toplanır.
- Türkçe karakterler doğrudan temiz UTF-8 yazılır; `sed`/`perl` ile UTF-8 bilinçsiz düzeltme yapılmaz (Â· tipi çift kodlama üretir), düzeltme Python UTF-8 ile yapılır.
- **Büyük harfli etiketlerde İngilizce terim (lang=tr tuzağı):** `<html lang="tr">` altında CSS `text-transform:uppercase`, İngilizce terimlerin "i" harfini Türkçe kuralıyla "İ"ye çevirir (VİSİBİLİTY, MENTİON, GEMİNİ, CİTATİON, POSİTİON). Bu yüzden büyük harfli etiketler (eyebrow, tablo başlığı, metrik adı, .pk/.th) CSS ile değil kaynakta doğru harflemeyle yazılır: İngilizce terim düz I (VISIBILITY, MENTION, CITATION, POSITION, GEMINI), Türkçe İ (İLK, PERSPEKTİFİ, METNİ). Metin zaten doğru büyük harfliyse CSS transform idempotent kalır (yeniden dönüştürme zarar vermez).
- "Hangi sorgu → hangi URL" tabloları tıklanabilir verilir; SERP sıraları doğrulanmadan yazılmaz.
- Excel / HTML yazı tipi: Arial veya Calibri.
- **Parantez tipi dekoratif belirteç kullanılmaz:** kart/blok kenarına CSS ile yerleştirilen büyük "(" / ayraç biçimli süs öğeleri (kenar boyunca kıvrımlı parantez şeridi vb.) HTML raporlarda kullanılmaz. Kart ayrımı sade arka plan tonu veya ince kenarlıkla yapılır.
- Sunumlarda (PPTX) span kullanılmaz; teknik terim düz İngilizce kalır.

### 7.2. Excel audit / denetim çıktısı dili

Referans: vitraglobal.com Geçiş Sonrası Audit yapısı.

- **Mimari:** "Özet" sheet'i + hata tipi başına detay sheet. Özet başlığı tek satır kimlik: "www.site.com - Geçiş Teknik SEO Audit | Tarama: GG.AA.YYYY".
- **Özet sütunları TR/EN karma:** üst katman etiketler Türkçe (`Önem | Kategori | Hata | Etkilenen URL | İlgili Sheet`), araçtan gelen değerler İngilizce verbatim (Error/Warning/Notice; "Meta description tag missing or empty"). Araç kaynaklı issue adları çevrilmez.
- **SEO Öneri sütunu kalıbı (imza):** Excel sütun-harfi koordinat referansı + bulgu (geniş zaman bildirme kipi) + noktalı virgül + edilgen "-malıdır" önerisi:
  - "A sütunundaki URL adresi 302 (geçici) yönlendirme kullanmaktadır; kalıcı taşınma için 301 status code ile güncellenmelidir."
  - "A sütunundaki sayfada birden fazla title/H1 etiketi bulunmaktadır; sayfa başına tek ve benzersiz title/H1 kalacak şekilde düzeltilmelidir."
  - "A sütunundaki sayfa içerisinde bulunan B sütunundaki linkleme, D sütunundaki final URL ile güncellenmelidir."
- **"-malıdır" bu kanalda ev standardıdır:** Excel audit önerileri kişisiz-normatif gereklilik kipiyle yazılır (geliştiricinin uygulaması için tasarlanmış talimat dili); sunum/rapor gövdesindeki "-ebilir" advisory tonundan bilinçli olarak ayrışır. Emir kipi ("düzeltin") burada da kullanılmaz.
- **Tek-satır-öneri ekonomisi:** öneri sheet'in yalnızca ilk veri satırına yazılır; tablo "veri", öneri "kural" olarak ayrışır. Aynı öneri her satıra kopyalanmaz.
- **Boş bulgu standardı:** temiz çıkan hata tipi sheet'i silinmez; tek satır yazılır: "Bu taramada bu hata tipi için URL tespit edilmedi."
- **Hücre placeholder dili:** eksik/mevcut alanlar parantezli tek kelimeyle: `(mevcut)` / `(boş)`; ikili durum etiketleri Türkçe: `Eşleşiyor / Eşleşmiyor`; veri yoksa `-`.
- **Karar müşteriye bırakılan koşullu kalıp** kullanılabilir: "Önce sayfaların açık kalıp kalmayacağı incelenmeli. - Kapatılacaksa 301 yönlendirmeleri hazırlanacak. - Açık kalacaklar için aksiyon alınmayacak."
- Detay sütunundaki açıklamalarda "İlgili bilgi veya element eklenmeliydi" tarzı gereksiz/geriye dönük yorumlar yazılmaz; ya düzgün açıklama verilir ya boş bırakılır.
- Teknik hijyen: status code'lar tam sayı (404, "404.0" değil), boolean yerine Türkçe etiket, sütun başlıklarında konuşma dili ("açık mı kalacak?") yerine nötr ad ("Açık Kalma Kararı"), benzer içerikli mükerrer sheet açılmaz.
