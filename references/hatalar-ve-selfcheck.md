# Sık Düşülen Hatalar ve Self-Check

## 1. Sık Düşülen Hatalar (örnek sunum denetiminden)

Geçmiş çıktılarda fiilen tespit edilen hata sınıfları; teslim öncesi özellikle taranır:

1. **Yüzde formatı karışıklığı:** aynı sunumda "+%197", "+248.1%", "%-3,3" bir arada. → Tek format: `+%X` / `-%X`, ondalık nokta.
2. **Ondalık ayırıcı karışıklığı:** metinde nokta, tabloda virgül ("2,75%"). → Her yerde nokta.
3. **Register kayması:** resmi "-mektedir" akışı içinde tek slaytta konuşma dili ("çiziyor", "diyebiliriz"). → Tek register.
4. **Marka/araç adı yazım tutarsızlığı:** VitrA/Vitra, SEOmonitor/SEOMonitor, Non-branded/Nonbranded. → Tek yazım seçilir, tüm çıktıda korunur.
5. **Typo yoğunluğu:** "sııralama", "avantaklı", "araştrması", "tamanında", "çıkabiliiz", "prefered", "Accessability", "snipppet". → Teslim öncesi imla taraması.
6. **İmkansız / kontrolsüz rakam:** "-%131 düşüş", çelişen hedef rakamları (500K vs 650K), kapakta yanlış yıl. → Rakam tutarlılık kontrolü.
7. **Yarım cümle / kalıntı metin:** "… ile " diye biten cümle, kopyalanan slaytta kalan eski başlık, çift slayt. → Son okuma.
8. **Görünmez karakter / bozuk metin:** ZWNBSP bulaşması ("JavaS criptHTML/CSS"), yapışık metin blokları. → UTF-8 temizliği.
9. **Sembol enflasyonu:** ➔, →, ⇒, ➜, ⬆, 📈 karışık kullanımı; pozitif içerikte 📉. → Standart sembol setine sadık kalınır (bkz. `references/insight-rakam-format.md` Bölüm 3.2).
10. **Kaynaksız iddialı istatistik:** "AI Overview çıktığında 1. sıra CTR'ı %34 düşüyor" (kaynaksız). → Her istatistiğe kaynak.
11. **"3th party"** → "3rd party".
12. **Tarih/çeyrek yazımı çeşitliliği:** "Q1 26", "'26 Q1", "Q 1". → "2026 Q1".
13. **Çift boşluk salgını:** "968  keyword", "mobil  visibility", "Audit  |". → Teslim öncesi çift boşluk taraması.
14. **Konuşmacı notu sızıntısı:** (Shared) destede [NOTES] alanında kalan iç açıklamalar ("cannibalization'a dayalı dalgalanma mevcut"). → Paylaşım öncesi notlar taranır.
15. **İç etiket/dosya adı sızıntısı:** "Blocked / In Progress" durum etiketleri, "(Shared) … // Inbound" link adları müşteri destesinde. → Türkçe şeffaf durum + temiz link adı.
16. **Ajanda-bölüm uyumsuzluğu ve şablon kalıntısı:** ajandada 3 bölüm varken destede 4 bölüm, "02" numarasının iki kez kullanılması, silinmemiş "SECTION TITLE" placeholder'ı. → Numara ve ajanda eşleşmesi kontrol edilir.
17. **Dönüşümlü terim kullanımı:** aynı destede "gösterim/Impression", "oturum/session", "görünürlük/visibility" karışık. → Deste başına tek karşılık seçilir.
18. **Hal eki - edilgen çatı uyumsuzluğu:** "kodları kaldırılabilir", "kaymalar yaşadığımız alan". → "kodlar kaldırılabilir", "kaymaları yaşadığımız alan".
19. **Mantık ters dönmesi:** "kaymalardan dolayı site açılış hızı artmaktadır" (azalma kastedilmiş). → Kopyala-yapıştır sonrası anlam kontrolü.
20. **Kaynaksız çarpıcı oran:** "%36 daha fazla AI atıfı", "2.5x referans" gibi iddiaların "gözlemleniyor" ile geçiştirilmesi. → Kaynak verilir ya da oran çıkarılır.
21. **Konuşma dili başlık:** ifade başlığı "-iyor" ile biter ("Citation'lar hangi kaynaklara gidiyor"). → Soru başlığıysa "?" eklenir (soru başlığı serbest); değilse nominal yapıya çevrilir ("Citation kaynak dağılımı").
22. **Coined kelime / ham İngilizce etiket:** grafik-tablo etiketinde "Duallik", "weak topic clusters". → Türkçeleştirilir veya yerleşik terime çevrilir; etiketler gövde metniyle aynı denetime tabidir.
23. **Keskin analitik betimleme:** "ters profildedir", "açık ara önde", "en zayıf halka". → Nötr formal karşılık ("tersine dönen örüntü", "belirgin biçimde önde", "en az işlenen başlık").
24. **"garanti" negatif/deyim kullanımı:** "mention garantisi vermemekte". → "beraberinde getirmemekte"; "garanti" olumsuz kalıpta bile kaçınılır.

---

## 2. Self-Check (her bölüm/sunum sonrası)

### 2.1. Dil ve biçim
- [ ] Em dash (—) var mı? → `grep "—"` = 0; "-" veya "&" ile değiştir.
- [ ] Mojibake / bozuk karakter (Ã, Ä±, Â·, ZWNBSP) var mı?
- [ ] Türkçe karakter ASCII'ye çevrildi mi? (yukselen, sozluk vb.)
- [ ] "ss." / "pik" geçmiş mi? → "session" / "peak".
- [ ] Paid için "talep artışı" mı yazıldı? → "yatırım artışı".
- [ ] Typo ve çift boşluk taraması yapıldı mı? (yukarıdaki Bölüm 1 listesi)
- [ ] Emoji sızmış mı? Gereksiz ünlem var mı?

### 2.2. Ton
- [ ] Emir kipi var mı? ("-in / -yin / -iniz / -ınız")
- [ ] Kesin vaat var mı? ("garanti, mutlaka, kesin, %X olacak")
- [ ] Olumsuz/keskin kelime var mı? ("kötü, hata, sorun, ciddi, berbat, yanlış, başarısız, zayıf")
- [ ] Pazarlama jargonu / abartı var mı? ("patlama, büyüme motoru, dramatik, kat kat")
- [ ] Çiğ/afili kelime var mı? ("doğrulanmış fırsat, çekirdek, kanıt, mercek, panorama")
- [ ] Meta ifade var mı? ("yeniden çerçeveledik, analiz gösterdi ki")
- [ ] Boş/dolgu veya devrik cümle var mı?
- [ ] Gözlem gereksiz yumuşatılmış mı? (ölçülmüş etki "-mektedir/-maktadır" ile net mi; çifte yumuşatma var mı?)
- [ ] Register tutarlı mı? (tek kip, tek şahıs; üç kip reyonu karışmış mı?)
- [ ] Rakip aşağılayıcı dil var mı? → Marka fırsatına çevir.
- [ ] Grafik/tablo etiketleri, cluster/eksen adları da dil denetiminden geçti mi? (coined "Duallik", ham İngilizce "weak topic clusters" yok mu?)
- [ ] İfade başlıkları "-iyor" ile bitmiyor mu? (soru başlığıysa "?" var mı?)

### 2.3. Rakam / kaynak
- [ ] Yüzde formatı tek mi? (+%X, ondalık nokta, tabloda da aynı)
- [ ] Nicel ifadelerde bağlam var mı? (çıplak sayı yok)
- [ ] Gerçek olmayan maliyet/bütçe rakamı var mı? → Çıkar, trafik bazlı yüzdeye çevir.
- [ ] İmkansız/çelişen rakam var mı?
- [ ] Kaynak notu her veri slaytında/tablosunda var mı? Format "Kaynak:" mı?
- [ ] Eksik veri raporda maskelenmiş mi? (Çekilemeyen veri chat'ten bildirildi mi, manuel istendi mi, eklenemiyorsa alan kaldırılıp chat'te belirtildi mi?)
- [ ] Dramatik kıyas ifadesi ("X kat küçümseme") var mı?
- [ ] [B] Her veri derin linkli mi? Alıntılar birebir mi? "Yön gösterir, kesin değil" uyarısı var mı?
- [ ] Kapsam (global/ülkeye özel, örneklem, kısmi dönem) belirtildi mi?

### 2.4. Terminoloji ve yapı
- [ ] [A] İngilizce terim yanlışlıkla çevrildi mi? (mention, anchor text, machine-readable)
- [ ] [B] Jargon Türkçeleştirildi mi? (jargon taraması = 0)
- [ ] Her insight ➔ ile mi başlıyor? Sembol seti standart mı?
- [ ] Artış yeşil, düşüş kırmızı, anahtar terim coral, rakamlar bold mu?
- [ ] HTML'de teknik terimler .term span'lı mı? Glossary dışına span verilmiş mi?
- [ ] Başlıklar nötr, anlaşılır, iddiasız mı?
- [ ] Otomasyon aracı adı veya iç kısıt ifadesi ("ölçülemiyor") sızmış mı? (İç kısıt varsa sunacak kişiye chat'ten iletildi mi?)
- [ ] Konuşmacı notları, iç durum etiketleri (Blocked vb.) ve "(Shared)" link adları temizlendi mi?
- [ ] Terimler tekilleştirildi mi? (gösterim/Impression karışımı yok)
- [ ] Aksiyon planı Öncelik/Faz ile mi verilmiş (gün/hafta değil)?
- [ ] Kapanış bir sonraki adımla mı bitiyor (özet dolgusuyla değil)?

**Herhangi bir kural ihlal edildiyse bölüm yeniden yazılır.**
