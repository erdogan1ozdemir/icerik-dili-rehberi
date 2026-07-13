---
name: icerik-dili-rehberi
description: Müşteriye veya markaya giden profesyonel çıktılar (SEO/GEO rapor, PPTX sunum, HTML rapor, Excel audit, Word/PDF doküman) üretilirken içerik dili, ton ve üslup kurallarını uygular. VitrA, Turkcell Pasaj, Flormar, Özdilekteyim, Game+/GeForce NOW, Sephora TR gibi ajans portföyü markaları için rapor/sunum/denetim yazarken, "rapor yaz", "sunum hazırla", "audit çıkar", "değerlendirme raporu", "performans raporu", "PPTX", "Excel audit" gibi taleplerde mutlaka bu skill'i kullan. Saf kodlama/teknik geliştirme işlerinde, tüketiciye dönük blog içeriğinde (ör. Game+ blog - kendi marka sesi kurallarına tabi) ve müşteriye gitmeyecek iç metinlerde bu skill tetiklenmez.
---

# İçerik Dili Rehberi - Rapor, Sunum & Doküman Çıktıları

> **Kapsam:** Ağırlıklı olarak içerik dili, üslup ve ton kuralları. Renk, tipografi ve layout genel olarak bu skill'in kapsamı dışındadır (bkz. ilgili tema/tasarım kuralları); tek istisna, rapor tablolarının kanal-bazlı renk standardıdır (`references/kanal-ozel-kurallar.md` 7.3) - Excel'in ayrı bir tasarım dosyası olmadığı için burada sabitlenir.
> **Kaynaklar:** Geçmiş projelerdeki tüm dil/stil prompt versiyonları (Özdilek, Turkcell, VitrA, QNB, Eczacıbaşı, GeForce NOW algı raporu, Zorlu, reklam sektörü sunumu) + 14 örnek çıktının (sunumlar + audit Excel) satır satır dil denetimi.
> **Kullanım akışı:** Her bölüm yazılmadan önce ilgili kurallar hatırlanır → yazıldıktan sonra `references/hatalar-ve-selfcheck.md`'deki self-check çalıştırılır → kural ihlali varsa bölüm yeniden yazılır.

**Uygulama önceliği:**
1. Bu dosyadaki temel prensipler (Bölüm 1) her koşulda geçerlidir.
2. Dil rejimi (Bölüm 0) ve tür-özel ton ayarları (`references/kanal-ozel-kurallar.md`) genel kuralları ezmez, örnekler.
3. Rakam/kaynak standardı (`references/insight-rakam-format.md`) tüm sayısal içerikte bağlayıcıdır.
4. Self-check (`references/hatalar-ve-selfcheck.md`) her çıktı öncesi çalıştırılır.
5. Kullanıcının işe özel açık talimatı bu rehberin üzerindedir; çelişki fark edilirse yazmadan önce sorulur.

---

## 0. Dil Rejimleri (önce bunu belirle)

Aynı standart, işin türüne göre iki rejimde uygulanır. Bölüm yazmadan önce hangi rejimde olduğunu belirle:

| Rejim | Kapsam | Karakter |
|---|---|---|
| **[A] Kurumsal rapor & sunum** | SEO/GEO değerlendirme, denetim, performans analizi, migrasyon, rakip analizi, pitch, strateji dokümanı | Soft, nötr, ihtiyatlı, iddiasız. Pasif ton, 3. tekil şahıs. İngilizce sektör terimleri KORUNUR. |
| **[B] Sosyal dinleme / algı raporu** | Kullanıcı tepkisi, marka algısı, kriz izleme raporları | Sade, günlük Türkçe + [A]'nın ihtiyatı. Jargon TÜRKÇEYE ÇEVRİLİR. Kullanıcı alıntıları BİREBİR korunur; yumuşatma yalnızca raporun kendi sesine uygulanır. Her veri derin linkli kaynağa bağlanır. |

İşaretsiz kurallar her iki rejimde geçerlidir; rejim-özel kurallar [A]/[B] ile işaretlidir.

---

## 1. Temel Prensipler (her çıktıda geçerli)

1. **Kesin vaat yok.** "Garantiliyoruz / kesin / mutlaka / %X artış olacak / 1. sıra çok kolay" kullanılmaz. Yerine: "potansiyel / fırsat / gözlemlenebilir / değerlendirilebilir / hedeflenebilir". Sayısal hedef verilecekse **bant** verilir ("150-250K ek aylık tık"), tek sayı verilmez.

2. **Olumsuz / keskin kelime yok.** "Kötü, berbat, yanlış, başarısız, hata, sorun, ciddi, zayıf" yerine nötr: "geliştirme alanı, gözden geçirilebilir, değerlendirilmeye değer, ele alınabilir, sınırlı kalmıştır". (Teknik terim istisnası: "canonical hatası", "404 hatası" gibi teknik adlandırmalar serbesttir; yargı kelimesi olarak kullanılmaz.)

3. **Emir kipi yok.** "-in / -yin / -iniz / -ınız" yerine "-ebilir / -abilir / önerilebilir / değerlendirilebilir". [B]'de emir yerine soru/öneri formu: "Sınırı kaldır" yerine "Sınırın kaldırılması mümkün mü?"

4. **"Meli / malı" yumuşatılır.** "Schema eklemelisiniz" yerine "Schema eklenmesi fayda sağlayabilir." Tek istisna (gözlemlenen ve kabul edilen kullanım): veri güvenilirliği / doğrulama gibi kritik konularda "-malıdır" bir kademe sertliğe çıkılabilir ("GA4 attribution denetimi ile doğrulanmalıdır"). Bu istisna aksiyon önerilerine taşınmaz.

5. **Pasif ton, 3. tekil şahıs [A].** "Biz / siz" yerine genel ifade: "Sizin siteniz yavaş" yerine "Sitenin açılış süresinde geliştirme alanı bulunuyor." Bulgu kipi "-mıştır / -mektedir"; yorum kipi "görülmektedir / göstermektedir / işaret etmektedir / dikkat çekmektedir". Aynı sunum içinde konuşma diline ("çiziyor", "diyebiliriz") kayma yapılmaz - register tutarlılığı korunur.
   **Üç kip reyonu birbirine karıştırılmaz:** (a) müşteriye dönük veri anlatımı = resmi-edilgen "-mıştır/-mektedir"; (b) Excel audit önerisi = kişisiz-normatif "-malıdır"; (c) statü/çalışma toplantısı ve pitch = birinci çoğul "biz" serbest. Bir çıktı hangi reyondaysa baştan sona orada kalır. (Detaylar: `references/kanal-ozel-kurallar.md`)

6. **Nicel ifadeler bağlamlı ve yumuşak.** Çıplak sayı bırakılmaz: "DR 18" değil "DR 18 (rakip ortalaması ~34 civarı)". Exact sayılar yuvarlanabilir: 434 → "400+", "1.2K / 1.3M". Gözlem net yazılır, hedging yalnızca öneri/tahmin katmanına uygulanır (detaylar: `references/insight-rakam-format.md`).

7. **Türkçe karakterler zorunlu.** ç ğ ı İ ö ş ü Ç Ğ Ö Ş Ü - ASCII'ye dönüştürme yok, mojibake (Ã, Ä±, Â·) yok. Marka/ürün adları doğru: "iPhone", "İstanbul". Yaygın imla tuzakları: "doküman" (dökümantasyon değil), "halihazırda", "korele".

8. **Em dash (—) kesinlikle yasak.** Yerine kısa tire "-" veya "&". Etiket/footer ayracı olarak "·" kullanılabilir. Teslim öncesi `grep "—"` = 0 olmalı. Not: " - " (boşluklu tire) em dash işlevinde cümle bölmek için de aşırıya kaçırılmaz; mümkünse iki nokta, virgül veya parantez tercih edilir.

9. **Emoji yok.** Çıktılarda emoji kullanılmaz (✓, ▲, ↑, ↓ gibi işlevsel semboller kullanılabilir).

10. **Gereksiz ünlem yok.** Ünlem yalnızca gerçek not/uyarı taşıyorsa.

11. **Boş / dolgu cümle yok.** Hiçbir bilgi taşımayan klişe kullanılmaz: "Rakamlar bağlamda değerlendirildiğinde dikkat çekmektedir" gibi cümleler yazılmaz. Her cümle somut bilgi taşır. Devrik / "düşük" cümle yok; yüklem sonda, tam kurulu cümle.

12. **Meta yorum yok.** Sunum kendini/sürecini anlatmaz: "Analizi yeniden çerçeveledik", "Bu bulgu bize gösterdi ki" yazılmaz; doğrudan olgu verilir.

13. **Uydurma / spekülasyon yok.** Bilgi yoksa boş bırakılır veya "-" yazılır; "eklenebilir/gelecek" gibi spekülasyon yapılmaz. Her önemli sayı bir kaynağa bağlanır. Varsayım rakamı verilmez; gerçek veri yoksa metrik çıkarılır. (Veri eksikliği politikasının tamamı: `references/kanal-ozel-kurallar.md` Bölüm 10.)

14. **Çiğ / afili / zorlama kelime yok.** "Doğrulanmış fırsat, çekirdek, kanıt, mercek, anılmak, panorama, havlu paradoksu" kullanılmaz. "Kanıt" → "örnek / ekran görüntüsü / dayanak"; "mercek" → "perspektif".

**Kapak kuralı:** Doküman, HTML rapor ve Excel çıktıları kapak süsü, dekoratif ayraç çizgisi veya "Hazırlayan / Prepared by" bölümü içermez; doğrudan içerikle başlar. Sunumlarda (PPTX) ise kapak slaytı + "SUNUM AKIŞI" ajandası ev standardıdır ve korunur.

---

## Detaylı referans dosyaları

Bu dosya yalnızca değişmez temel kuralları içerir. Aşağıdaki referans dosyalarını, ilgili bölümü yazmadan hemen önce oku:

- **`references/terminoloji-ve-sozluk.md`** - İngilizce/Türkçe terim politikası, terim tanıtma yöntemi, yasak→tercih edilen ifade sözlüğü, rozet/etiket eşlemeleri.
- **`references/insight-rakam-format.md`** - Insight yazım formatı (➔ iskeleti, renk vurgulama), rakam/tarih/kaynak standardı, öneri dili (advisory tone) hiyerarşisi.
- **`references/kanal-ozel-kurallar.md`** - Marka-güvenli çıktı kuralları, sunum yapısı ve akış ritüelleri, sunum/doküman türüne göre ton ayarları (çeyreklik rapor, migrasyon, GEO, pitch, PageSpeed, statü sunumu vb.), HTML rapor & Excel audit kanal kuralları, negatif bulgu çerçevelemesi, rakip dili, veri eksik/ölçüm kısıtı politikası.
- **`references/hatalar-ve-selfcheck.md`** - Sık düşülen hatalar listesi (geçmiş denetimlerden) ve her çıktı sonrası çalıştırılacak self-check.

Küçük/basit bir tek cümlelik talep için tüm referansları okumak gerekmez; ama tam bir bölüm/slayt/tablo/sheet yazılıyorsa ilgili referans dosyaları mutlaka kontrol edilir.
