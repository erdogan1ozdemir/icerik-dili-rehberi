# Öneri Dili, Insight Formatı, Rakam/Tarih/Kaynak Standardı

## 1. Öneri Dili (Advisory Tone)

Aksiyon önerileri direktif değil, öneri kipiyle iletilir. **Hedging hiyerarşisi:**

1. **Gözlem (veri destekliyorsa) → net yazılır.** "…dönüşüm eğiliminin güçlendiğine işaret eder." (gereksiz "edebilir" eklenmez)
2. **Öneri → yumuşatılır.** "…değerlendirilebilir / önerilebilir / test edilebilir / düşünülebilir / fayda sağlayabilir / gözden geçirilebilir / ele alınabilir / potansiyel taşımaktadır / fırsat sunar"
3. **Nedensellik atfı → ihtiyatlı.** "…kaynaklanabilir / …ile ilişkilendirilebilir / …olarak okunabilir / …olarak değerlendirilebilir / kısmen bu dönemin etkisiyle oluştuğu gözlenmektedir"
4. **Kritik doğrulama (tek sert kademe) →** "…doğrulanmalıdır / gözden geçirilmelidir" (yalnızca veri güvenilirliği konularında)

**Örnekler:**
- "Blog anasayfa yeniden tasarlanmalı" → "Blog anasayfa yapısının daha kullanıcı dostu hale getirilmesi önerilir."
- "Bid'i %20 düşürün" → "Bid azaltma test edilebilir."
- "Süre devrini 30 saate çıkarın" [B] → "Devir hakkının artırılması, 'ödediğim süre boşa gidiyor' algısını azaltabilir."

**Plan/aksiyon maddeleri** örnekteki gibi yazılır (emir kipi doğal olarak devre dışı kalır): "Paket listeleme sayfalarına içerik eklenmesi %7-10 click artışı (250K+ click) sağlayabilir."

**Çifte yumuşatma uyarısı:** olasılık kipleri üst üste bindirilmez. "SSR'ın etkisini yansıtıyor olabilir olarak değerlendirilebilir" gibi ikili/üçlü yumuşatma cümleyi iddiasızlaştırır; cümle başına tek yumuşatma katmanı yeterlidir. "Mutlaka + -ebilir" melezi de kullanılmaz ("mutlaka eklenebilir" değil; ya "eklenmesi önerilir" ya "eklenmelidir").

**Okuyucuya yönlendirme kabulü:** "İnceleyebilirsiniz / görebilirsiniz / dokümanı inceleyebilirsiniz" hitabı emir sayılmaz; görsel ve ek doküman yönlendirmelerinde serbesttir.

**Non-direktif kapanış:** kartlar/bölümler açık soruyla kapatılabilir; önceliklendirme müşteriyle konuşarak ilerlenebilir: "Aksiyonların önceliklendirilmesi [marka] ekibinin stratejik tercihleri ve öncelikleriyle güncellenebilir."

---

## 2. Insight Yazım Formatı

### 2.1. Standart iskelet

```
➔ [Metrik + dönem] + [kontrast/yön fiili] + (parantez içi rakam kanıtı).
  [Sebep-sonuç veya çıkarım cümlesi - hedge fiiliyle bağlanır].
  [Opsiyonel: yumuşak öneri].
```

- Ok karakteri **➔** (→ değil); ok sonrası tek boşluk; her insight tek okla başlar.
- 1-2 cümle ideal; 3. cümle sebep-sonuç için.
- Birinci cümle sayısal ("ne oldu"), ikinci cümle yorum ("ne anlama geliyor"). Yorum katmanı zorunludur - yalın veri bırakılmaz.
- **Kontrast kalıbı** ev üslubunun imzasıdır: "X artarken Y düşmüştür", "Session -%11 daralırken Revenue +%19 artmıştır".
- Tablo altı telegrafik mini-insight'larda " | " ile çoklu madde ayrılabilir: "➔ Banyo Dolabı Rev %16.4 / Purch %4.5 (3.61x) - yüksek-AOV stratejik. | Metropole hem Organic hem Paid'de #1."
- Bölüm sentezinde "Genel tablo, …" kapanış formülü kullanılabilir: "Genel tablo, talep daralmasına rağmen sıralama kazanımlarıyla trafiğin korunduğunu göstermektedir."
- Her veri slaytı sonunda 1 cümlelik özet eklenebilir: `➔ SEO Insight: [özet].`
- Girizgah zarf-fiilleri insight açılışında standarttır: "…kıyaslandığında / bakıldığında / incelendiğinde". Sıralama cümleleri "en yüksek / en çok / en dirençli … olmuştur" kalıbıyla; olumlu ayrışma için sabit deyim: "…%X ile pozitif ayrışmaktadır."
- Her tablonun altında yorum paragrafı üçlüsü: en çarpıcı satır + genelleme + aksiyon önerisi. Düşüş satırı tabloda sessizce bırakılmaz; ya yorumlanır ya dipnotla bağlanır.

### 2.2. Renk vurgulama

| Vurgu tipi | Renk | Örnek |
|---|---|---|
| Düşüş / negatif | Kırmızı (#D32F2F) | `-%37 düşerken`, `-%2.6 YoY` |
| Artış / pozitif | Yeşil (#2E7D32) | `%8 artmıştır`, `+%8.1`, `+1.8 iyileşme ↑` |
| Anahtar terim / dikkat | Coral (#F4845F) | `en yüksek görüntülenme`, `en stabil kategori` |
| Rakamlar / metrik adları | Bold | `595.4K tıklama`, `%4.3 seviyesinde` |

### 2.3. Örnek insight cümleleri

**Karşılaştırma:**
> ➔ 2025'te takip edilen kategorilerde markasız (non-brand) aramalar %18 düşerken, VitrA + kategori aramaları yalnızca %5 düşmüştür. Kategori talebi daralsa da marka talebinin görece daha dayanıklı olduğu görülmektedir.

**Veri metodolojisi:**
> ➔ Property-level ve URL-filtered export arasındaki fark "kayıp" değil, daha hedefli dağılım olarak değerlendirilebilir.

**Kanal analizi (kontrast + ihtiyatlı atıf):**
> ➔ Direct kanalında Sessions +%313 YoY büyürken Revenue -%42 düşmüştür; trafiğin önemli bölümünün düşük dönüşümlü ziyaretçilerden oluştuğu değerlendirilebilir (domain birleşmesi kaynaklı tracking sapması dahil).

**GEO:**
> ➔ Branded web mention'lar AI görünürlüğüyle %X korelasyon gösterirken, backlink korelasyonu %Y seviyesinde kalmaktadır. Marka anılma durumunun ağırlığı artmakta olarak okunabilir.

**Aksiyon önerisi:**
> ➔ Blog yazıları içerisinde paket sayfalarına yönlendirme alanları (CTA banner, sidebar widget) eklenmesi değerlendirilebilir. Aylık 12K+ click dönüşüm potansiyeli taşımaktadır.

---

## 3. Rakam, Tarih ve Kaynak Standardı

Örnek sunumlarda en çok tutarsızlık bu alanda tespit edildi; aşağıdaki tercihler bağlayıcıdır.

### 3.1. Rakam formatı

- Büyük sayılar K/M: `12K click`, `1.2M impression`, `595.4K`. **Ondalık ayırıcı her yerde nokta** (tabloda "2,75%" gibi virgül kullanılmaz).
- **Yüzde: % işareti sayının önünde, işaret %'den önce:** `%18`, `+%6.9`, `-%37`. Tablolarda da aynı format ("34.8%" / "%-3,3" varyantları kullanılmaz).
- Exact sayılar yuvarlanabilir: 434 → "400+"; abartılmaz. Doğrulanmış toplama yakınsa "+" (95M+), %30+ sapma varsa "ort." ile gerçek değere çekilir (ort. 430K); sapma parantez içinde de belirtilebilir.
- Çarpan: `3.6x`, `~3x`; yaklaşıklık `~`; aralıklar bant olarak: "150-250K", "%73-74 bandında", "-%5 ila -%12".
- Pozisyon değişimi pozitif değer iyileşmedir: `10→8 = +2 iyileşme ↑`.
- Matematiksel olarak imkansız yüzdeler yazılmaz (-%131 düşüş olamaz); bin üzeri yüzdelerde (+%6014) mutlak değer de verilir.
- TL: metinde `₺1.49M`; tek çıktıda tek sistem.

### 3.2. Sembol seti

| Sembol | İşlev |
|---|---|
| ➔ | Insight başlatıcı (tek kullanım alanı) |
| → | Önce-sonra / dönüşüm: `13.6 → 9.9`, `online.vitra.com.tr → vitra.com.tr` |
| ↑ ↓ | Yön göstergesi |
| ✓ / ▲ | Pozitif / dikkat gerektiren madde işareti (özet bloklarında; ▲ coral renkle basılır, ⚠ kullanılmaz) |
| ⇒, ➜, emoji oklar | Kullanılmaz (tek sete sadık kalınır) |

### 3.3. Tarih ve dönem

- Çeyrek: **"2026 Q1"** (Q1 26, Q 1 varyantları kullanılmaz). Dar tablo hücresi gibi sığmayan yerlerde kısaltma olarak "'26 Q1" kullanılabilir.
- Ay-yıl: "Mart 2026" (metin), "Mar'26" (dar tablo hücresi).
- Veri kapsamı alt başlıkta parantezle beyan edilir: "Q1 2026 (1 Oca - 31 Mar 2026) & Q1 2025 (1 Oca - 31 Mar 2025) | YoY karşılaştırma".
- Rakip fiyat/paket ve SERP verisi gözlem tarihiyle verilir.

### 3.4. Kaynak gösterimi

- Tek format: **"Kaynak: [Kaynak Adı]"** ("Source:" kullanılmaz; iki dil karıştırılmaz).
- Her veri slaytında/tablosunda kaynak notu bulunur; format: "Kaynak: GA4 - Aylık Agregasyon | 1 Oca 2025 - 31 Mar 2026".
- Aynı kaynak ibaresi her slaytta tekrarlanmaz; bir kez yöntem notunda + en altta "Verilerin Alındığı Kaynaklar" bölümünde toplanabilir.
- Veri kapsamı dipnotları "***" ile işaretlenebilir ve şablonlaşabilir ("*** Karşılaştırma, 2024 Ocak verisi olmadığı için 10 ay üzerinden yapılmıştır.").
- [B] Sosyal dinlemede her veri/alıntı derin linkli: forum `#:~:text=`, sözlük `entry/<id>`, şikayet slug'ı, Reddit permalink.
- Platform kaynaklı metriklere şerh düşülür: "Metriklerin bir bölümü platform veya ajans kaynaklı olduğundan, kaynağıyla birlikte aktarılması önerilir."
- Teknik önerilerde referans dokümantasyon linki verilebilir: "Kaynak: https://web.dev/cls/". Eşik değerler öneri cümlesine gömülür: "toplam boyutun 1.600 KiB'in altında tutulması tavsiye edilir."
- Detaya yönlendirme kalıbı: "Detaylı çalışma ve tüm sıralamalar için dokümanı inceleyebilirsiniz. Link: [Doküman Adı]".
- Grafik okuma kılavuzu gerekiyorsa slaytta verilir: "Tablo altındaki G ifadeleri Google update'lerini, yeşil daireler büyük çaplı içerik değişikliklerini göstermektedir."

---

## 4. Başlık Dili

- **Nötr, kısa, açıklayıcı, premium.** İddialı/afili/anlamsız başlık yasak: "SEO gücü", "Anlık görünüm", "Havlu paradoksu", "basitçe nedir".
- Rapor slaytlarında hiyerarşik etiket şablonu: **"Marka | Konu Alanı"** + alt başlıkta araç + metrik + dönem: "Özdilekteyim | Organik Trafik Ölçümlemesi / GSC - Aylık Impression & Click".
- Bulgunun başlığa taşınması yalnızca yönetici özeti / kritik tespit katmanında kullanılır ("Sessions ile Revenue Arasında Ayrışma") ve üstte nötr eyebrow etiketiyle dengelenir.
- Soru başlıklar eğitim/vizyon sunumlarında ve bölüm açılışlarında uygundur: "Markalar için ne ifade ediyor?", "Nelere Odaklandık?".
- Düzeltme örnekleri:
  - "ölçüm aracı (hub) · iyi sıralanıyor ama iki yapısal sorun var" → "Turkcell Hız Testi Sayfası: Sıralama Durumu ve Yapısal Geliştirmeler"
  - "Rakip boşluk analizi" → "Content Gap ve Rakip İçerik Karşılaştırması"
  - "Son 6 ayın 8 başlıkta özeti" → "2026'daki Önemli Gelişmeler"
- Meta etiketler net adlandırılır: "Title tazeliği" değil "Meta Title", "Meta Description".
- Aynı sunum/rapor içinde etiket ve kategori adları tekilleştirilir; aynı kavram için iki farklı ad kullanılmaz.
