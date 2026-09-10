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
24. **Sade dil katmanı atlanmış teknik bulgu:** bulgu yalnızca terimle yazılmış ("Sayfada BreadcrumbList bulunmamaktadır"), okuyucunun terimi bilmesi varsayılmış. → Yanına mekanizma + sonuç cümlesi eklenir; analiz/denetim Excel'lerinde "Ne anlama geliyor" sütunu açılır.
25. **Karşılıksız terim yığılması:** dosyada onlarca teknik terim geçerken ne sözlük ne de ilk geçiş açıklaması bulunuyor. → Teslim öncesi terim taraması yapılır; 10'dan fazla terim varsa "Terim Sözlüğü" sheet'i eklenir.
26. **Sektör teriminin gereksiz Türkçeleştirilmesi:** araç veya ölçüm jargonu temizlenirken yerleşik İngilizce terimlerin de çevrilmesi ("breadcrumb" yerine "yol izi", "markup" yerine "işaretleme"). → [A] rejiminde terim İngilizce kalır, sözlükte veya ilk geçişinde açıklanır. Çıkarılacak olan yalnızca gerçek ölçüm jargonudur ("token", "head terim").
27. **Metaforik kategori adı:** denetim çıktısında "İçerik hijyeni", "kod hijyeni", "sağlık skoru" gibi tıp/gıda çağrışımlı bölüm adları. → İşi tarif eden nötr karşılık ("İçerik temizliği", "Teknik tutarlılık", "Genel durum").
28. **"garanti" negatif/deyim kullanımı:** "mention garantisi vermemekte". → "beraberinde getirmemekte"; "garanti" olumsuz kalıpta bile kaçınılır.
29. **Excel/Doc'ta Office varsayılan teması:** lacivert başlık satırı, sarı koşullu biçimlendirme highlight'ı. → Excel'de `#434343` başlık + Calibri + ink teal gövde; delta sütunları dolgu yok yalnızca yazı rengi (bkz. Bölüm 7.3).
30. **Çalışmayan içindekiler (ToC):** HTML raporda ToC bağlantısı tıklandığında ilgili bölüme gitmiyor, aktif bölüm vurgusu kaydırmayla güncellenmiyor ya da vurgu bir bölüm kayıyor. Kök nedenler: yalnızca varsayılan capa davranışına güvenilmesi (statik önizleme ve sandbox'lı bağlamlarda hash gezinmesi engellenir), scroll-spy'da `getBoundingClientRect()` yerine `offsetTop` kullanılması, sticky appbar yüksekliğinin hesaba katılmaması. → Açık tıklama işleyicisi + `getBoundingClientRect()` tabanlı scroll-spy + `:target` CSS yedeği (bkz. `kanal-ozel-kurallar.md` 7.1).
31. **ToC bağlantılarının altı çizili:** kabuk CSS'indeki genel `a:hover{text-decoration:underline}` kuralı gezinme listesine sızar. → `.sidenav a, .toc-sheet__panel a{text-decoration:none}` (hover ve focus dahil); klavye erişimi `:focus-visible` outline'ı ile verilir.
32. **Logo bandının iki kez basılması:** sticky üst barda ve hero/kapak bloğunda aynı "Marka | Hazırlayan" bandının tekrarlanması; ekranda üst üste iki kimlik satırı görünür. → Bant raporda bir kez bulunur; sticky bar varsa bant üst bardadır.
33. **Kabuk / etiket yığını gibi iç adlandırmalar:** teknik denetim çıktısında "kabuk sayfaları", "uygulama kabuğu", "Google etiket yığını" gibi çeviri ya da iç jargon ifadeleri. → Ortak şablonu paylaşan sayfalar için **template** ("aynı template'deki sayfalar"), ölçümleme kodları için **tag** ve **tag stack** kullanılır.
34. **Açıklamasız sütun başlığı:** okuyucu "3 yıllık değişim"in hangi pencereleri karşılaştırdığını ya da "Tahmini trafik"in neyi ölçtüğünü tabloya bakarak anlayamaz. → Her `<th>` için `data-t` açıklaması yazılır; üretim betiği açıklaması eksik başlık kaldığında çıktı üretmez (bkz. `kanal-ozel-kurallar.md` 7.1).
35. **Kırpılan açıklama balonu:** `th` içine `::after` ile konan balon `.tw{overflow-x:auto}` sarmalayıcısı tarafından kesilir ve yarısı görünmez. → Sayfada tek bir `position:fixed` `#tt` öğesi kullanılır; ekran kenarında içeri çekilir.
36. **Değeri okunamayan grafik:** çizgi grafikte okuyucu tepe ya da dip noktanın kaç olduğunu göremez, yalnızca eksenden tahmin eder. → Her veri noktası için görünmez hover bandı + gömülü JSON değerler; balon dönem etiketini ve tüm serileri listeler.
37. **Madde imi çiftlenmesi:** ✓ veya ▲ ile başlayan madde, `<ul>` varsayılan `list-style: disc` ile birlikte ekranda "• ✓ …" olarak iki imli görünür. → İşaret taşıyan listeler `ul.marks{list-style:none;padding-left:0}` ile yazılır, işaret `.mk` span'ında mutlak konumlanır.
38. **Marka adının yanlış yazımı:** VitrA yerine "Vitra" veya "VITRA". → Marka adı her koşulda `VitrA`; yalnızca arama kelimeleri ve alan adları kendi yazımını korur.
39. **Hover işareti verip içerik göstermeyen öğe:** `.term` span'ı ya da `cursor:help` taşıyan başlık üzerine gelindiğinde soru işareti imleci çıkıyor ama açıklama açılmıyor; tanım yalnızca sondaki Terim Sözlüğü bölümünde duruyor. → İşaret veren her öğe `#tt` balonundan ya da CSS `::after` ile açıklama basar; basmayacaksa imleç ve noktalı alt çizgi kaldırılır.
40. **Tıklanamayan adres hücresi:** tabloda hedef sayfa yazılı ama düz metin; okuyucu adresi kopyalayıp tarayıcıya yapıştırmak zorunda kalıyor. → URL, sayfa yolu ve sayfa adı geçen hücreler `<a href>` ile tam adrese bağlanır (`target="_blank" rel="noopener"`). Yayında olmayan önerilen adresler düz metin bırakılır.
41. **Tarihsiz dönem ifadesi:** karo etiketinde "3 ay", "son çeyrek" yazıyor ama hangi 3 ay olduğu belirtilmiyor. → Tarih aralığı karo etiketinde ya da hover künyesinde verilir ("1 Haz - 31 Ağu 2026").
42. **Mobilde bozulan rapor:** masaüstünde düzgün görünen HTML rapor telefonda yatay kaydırıyor, içindekiler sayfanın başında dev bir blok olarak duruyor, grafikler 90 px yüksekliğe ezilmiş oluyor. → 940 / 720 / 520 px kırılımları, mobil içindekiler için yüzen düğme + alt sayfa, grafiklere taban genişlik ve kendi kaydırması (bkz. `kanal-ozel-kurallar.md` 7.1).
43. **Mobil içindekilerin masaüstünden ayrışması:** alt sayfada kümeler ya da numara rozetleri düşürülüp yalın bir bağlantı listesine dönülmesi. → Alt sayfa masaüstü içindekilerin birebir kopyasıdır; scroll-spy her iki listeyi birlikte günceller.
44. **Yarım çevrilmiş ikinci dil:** dil düğmesi gövde metnini çeviriyor ama sütun başlığı açıklaması, grafik balonundaki sabit etiket ("Üç yıllık değişim"), tema düğmesinin `title`'ı ya da sayfa başlığı Türkçe kalıyor. → Nitelikler, grafik JSON'u ve JS içindeki sabit etiketler de dil katmanına bağlanır; eksik ifade kalırsa çıktı üretilmez.
45. **İkinci dilde Türkçe sayı biçimi:** İngilizce sürümde `12.100` ve `%56,7` bırakılması; okuyucu `12.100`'ü ondalık sanabilir. → Binlik/ondalık ayracı ve `%` konumu dile göre çevrilir, sıra bildiren `23.` `23rd` olur; tarihler dönüştürülmez.
46. **Arama kelimesinin çevrilmesi:** `dusch wc` ifadesinin İngilizce sürümde "shower toilet" olarak yazılması. → Arama kelimesi veridir, olduğu gibi kalır; karşılığı yalnızca hover balonunda verilir.
47. **Hover işareti verilen yabancı terimin karşılıksız kalması:** `Streckengeschäft` noktalı alt çizgiyle işaretli ama balon açılmıyor. → İşaret veren her öğe içerik basar; basmayacaksa imleç ve noktalı alt çizgi kaldırılır.

---

## 2. Self-Check (her bölüm/sunum sonrası)

### 2.1. Dil ve biçim
- [ ] Em dash (—) var mı? → `grep "—"` = 0; "-" veya "&" ile değiştir.
- [ ] Şapkalı a (â) var mı? → `grep "â"` = 0. (Yalnız bu rehberin çıktıları için; blog metnine uygulanmaz.)
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
- [ ] "çıplak" geçiyor mu? → anlamına göre jenerik (marka araması, ad), yalın (kısaltma) ya da bağlamsız sayı
- [ ] Çiğ/afili kelime var mı? ("doğrulanmış fırsat, çekirdek, kanıt, mercek, panorama")
- [ ] Rapor kendi yapısını anlatan meta cümle var mı? ("altı başlığın her birine ayrı bölümde yanıt verilmektedir", "ilgili bölümde ele alınmaktadır")
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
- [ ] HTML raporda kart/blok kenarına renkli dekoratif şerit (border-left/top coral vb.) var mı? → Kart ayrımı ince kenarlık veya sade arka plan tonuyla yapılır (bkz. HTML rapor kanal kuralı: parantez/ayraç biçimli süs öğesi yasak).
- [ ] HTML raporda büyük harfli etiketlerde İngilizce terimler hatalı "İ" ile mi geliyor? (lang=tr + CSS uppercase → VİSİBİLİTY / MENTİON / GEMİNİ). → Etiketler kaynakta doğru büyük harfle yazılır (İngilizce düz I, Türkçe İ).
- [ ] Excel'de Office varsayılan teması (lacivert başlık, sarı highlight) kullanılmış mı? → Başlık `#434343`, gövde Calibri + ink teal, delta sütunları yalnızca yazı rengi (bkz. Bölüm 7.3).
- [ ] HTML raporun başında **marka logosu ve Inbound logosu birlikte** var mı? İkisi de `data:` URI olarak gömülü mü (dış adresten çekilen logo yok)? Bant **yalnızca bir kez** mi basılmış (sticky bar + hero'da tekrar yok)?
- [ ] **HTML raporda ToC fiilen test edildi mi?** (a) Bağlantıya tıklayınca ilgili bölüme gidiyor ve başlık sticky barın altında kalıyor mu? (b) Kaydırırken aktif bölüm vurgusu doğru bölümü mü işaretliyor (bir bölüm kaymıyor mu)? (c) JavaScript çalışmadığında `:target` yedeği aktif durumu koruyor mu? (d) Mobil ToC panelinde de aynı davranış var mı?
- [ ] **`cursor:help` ya da noktalı alt çizgi taşıyan her öğe hover'da gerçekten içerik gösteriyor mu?** (terim işaretlemeleri, sütun başlıkları, karolar tek tek denendi mi? Göstermiyorsa ya tooltip eklenir ya işaret kaldırılır)
- [ ] **URL, sayfa yolu ve sayfa adı geçen hücreler tıklanabilir mi?** (`<a href>` tam adres, `target="_blank" rel="noopener"`; yayında olmayan önerilen adresler düz metin)
- [ ] **Karo, KPI ve alt başlıklardaki dönem ifadeleri tarihli mi?** ("3 ay" değil, "1 Haz - 31 Ağu 2026")
- [ ] **Üst bar ve içindekiler ev şablonuna uyuyor mu?** (açık yarı saydam üst bar · solda marka logosu + iki satır başlık · sağda tarih/kapsam rozetleri, XLSX indirme, tema anahtarı, Inbound logosu · içindekiler yüzen kart, grup etiketli, iki haneli numara rozetli)
- [ ] **Tema anahtarı çalışıyor mu?** (koyu temada zebra satırı, tablo başlığı ve ajans logosu da doğru mu; seçim saklanıyor mu?)
- [ ] **Mobilde içindekiler paneli masaüstü listesinin birebir klonu mu?** Üst bar sarınca tıklanan başlık barın altında kalıyor mu (`--appbar-h` ölçülüyor mu)?
- [ ] **ToC bağlantılarının altı çizili mi?** → `.sidenav a, .toc-sheet__panel a{text-decoration:none}` (hover/focus dahil), erişilebilirlik `:focus-visible` ile.
- [ ] **HTML raporda her tablo sütun başlığında hover açıklaması var mı?** Açıklaması olmayan `<th>` kaldı mı? Aynı başlık farklı tablolarda farklı şey anlatıyorsa açıklama ayrıştırıldı mı?
- [ ] **Sütun başlığı balonu kırpılıyor mu?** `.tw{overflow-x:auto}` içindeki `th::after` balonu kesilir; `position:fixed` tek balon kullanıldı mı, ekran kenarında içeri çekiliyor mu?
- [ ] **Grafiklerde veri noktasına gelince sayısal değer açılıyor mu?** Çizgi grafikte tüm seriler seri rengiyle listeleniyor mu, sayılar Türkçe binlik ayracıyla mı yazılıyor?
- [ ] **İşaretçi grafikten çıktığında** balon, imleç çizgisi ve nokta işaretleri birlikte temizleniyor mu?
- [ ] **Madde imi çiftlenmiş mi?** ✓ / ▲ taşıyan listelerde tarayıcının kendi nokta imi kapatıldı mı (`ul.marks{list-style:none}`)? Sunum ve dokümanda da otomatik im ile elle yazılan im üst üste binmiş mi?
- [ ] Başlıklar nötr, anlaşılır, iddiasız mı?
- [ ] **İçindekiler kümelere ayrıldı mı?** Ara başlıklar var mı, kümeye atanmamış bölüm kaldı mı, küme sırası belge sırasıyla uyuşuyor mu?
- [ ] **İçindekiler kaydırmasız sığıyor mu?** Kırpılan başlık var mı, kısa etiketler `title` ile tam başlığı taşıyor mu?
- [ ] **Açık ve koyu tema birlikte çalışıyor mu?** Tema düğmesi var mı, her iki temada kart, tablo başlığı, rozet ve çubuk renkleri doğru mu?
- [ ] **Veri dosyası rapordan indirilebiliyor mu?** Düğme hem üst barda hem altbilgide mi, gömülü içerik diskteki dosyayla birebir mi?
- [ ] **Uzun tablolar kendi içinde mi kaydırılıyor?** Başlık satırı sabit kalıyor mu?
- [ ] **Ölçek çubukları zeminli mi?** Küçük değerler görünüyor mu?
- [ ] **Bağlantılar sıralamada görünen birebir adrese mi gidiyor** (domaine düşen kısaltma var mı)?
- [ ] **Sekmeli tablolarda örnek veri listesi var mı?**
- [ ] **Yabancı dildeki terimler ve arama kelimeleri hover'da karşılığını gösteriyor mu?** İşaret verilen her ifade balon açıyor mu, karşılık raporun o anki diline göre mi geliyor?
- [ ] **İki dilli raporda dil düğmesi her katmanı çeviriyor mu?** (gövde, başlık, içindekiler ve küme etiketleri, tablo hücreleri, `data-t` sütun açıklamaları, `data-term` tanımları, sekme adları, grafik seri adları ve grafik balonundaki sabit etiketler, `title` / `aria-label` / `alt`, sayfa başlığı, `<html lang>`) Sözlükte karşılığı olmayan ifade kaldı mı?
- [ ] **Dil değişince sayı biçimi de değişiyor mu?** (`12.100` / `12,100` · `%56,7` / `56.7%` · `23.` / `23rd`) Tarihler ve pozisyon listeleri bozulmuş mu?
- [ ] **Arama kelimeleri ve marka adları iki dilde de korunuyor mu?** Dil değiştirip geri dönüldüğünde metin birebir eski haline dönüyor mu?
- [ ] **HTML rapor 375 px'de fiilen açıldı mı?** Gövde yatay kaydırma yapıyor mu (`scrollWidth > innerWidth`)? Geniş tablo ve grafikler sayfayı değil kendi sarmalayıcısını mı kaydırıyor?
- [ ] **Mobilde içindekiler yüzen düğme ve alt sayfa olarak mı açılıyor?** Kümeler, numara rozetleri ve aktif vurgu masaüstüyle aynı mı? Açıkken arka plan kaydırması kilitleniyor, örtü / bağlantı / `Escape` kapatıyor mu?
- [ ] **Grafikler mobilde okunur mu?** Taban genişlik verilip kendi içinde kaydırılıyor mu, yoksa yüksekliği ezilmiş mi?
- [ ] **`@media print` ve `prefers-reduced-motion` kuralları yazıldı mı?**
- [ ] **VitrA büyük A ile mi yazılmış?** Gövde metni, başlık, tablo ve grafik etiketlerinde `Vitra` / `VITRA` kalmış mı? (Arama kelimeleri ve alan adları istisnadır.)
- [ ] Teknik bulguların yanında sade dil katmanı var mı? (mekanizma + sonuç; analiz/denetim Excel'inde "Ne anlama geliyor" sütunu)
- [ ] Sektör terimi gereksiz Türkçeleştirilmiş mi? (breadcrumb, markup, canonical, passage gibi terimler İngilizce kalmalı)
- [ ] Terim taraması yapıldı mı? Her teknik terimin ya sözlükte ya ilk geçişinde karşılığı var mı? (10+ terim varsa "Terim Sözlüğü" sheet'i)
- [ ] Kategori ve bölüm adları metaforik mi? ("İçerik hijyeni", "kod hijyeni", "sağlık skoru") → İşi doğrudan tarif eden nötr karşılık kullanılır (bkz. `terminoloji-ve-sozluk.md` 2.7).
- [ ] Otomasyon aracı adı veya iç kısıt ifadesi ("ölçülemiyor") sızmış mı? (İç kısıt varsa sunacak kişiye chat'ten iletildi mi?)
- [ ] Konuşmacı notları, iç durum etiketleri (Blocked vb.) ve "(Shared)" link adları temizlendi mi?
- [ ] Terimler tekilleştirildi mi? (gösterim/Impression karışımı yok)
- [ ] Aksiyon planı Öncelik/Faz ile mi verilmiş (gün/hafta değil)?
- [ ] Kapanış bir sonraki adımla mı bitiyor (özet dolgusuyla değil)?

**Herhangi bir kural ihlal edildiyse bölüm yeniden yazılır.**
