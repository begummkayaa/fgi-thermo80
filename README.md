# Safety 4.0 Bootcamp – Laboratuvar Föyleri (FGI Thermo 80 Sürümü)

**Ad Soyad:** Begüm Kaya  
**Grup:** Gece B  
**Tarih:** 22.10.2026 (Lab 1-4), 06.11.2026 (Lab 5-7 ve SWOT)

## Seçilen Makine
**FGI Kapı ve Yükleme Teknolojileri – Thermo 80 mm Seksiyonel Endüstriyel Kapı**

80 mm galvaniz çelik sandviç panelli, burulma yayları ve çelik halatlarla dengelenen, dişli elektrik motoruyla çalışan endüstriyel seksiyonel kapı (maks. 8000 x 6000 mm). T75/T100 kumanda panosu ile deadman, otomatik veya **uzaktan kumanda** ile kullanılabilir. Senaryoda bir lojistik deposunun yükleme kapısıdır; forklift ve yaya aynı açıklıktan geçmektedir.

**Teknik veri sayfasındaki temel özellikler:**
- T75/T100 kumanda panosu (IP54): 3 buton (aç-dur-kapat), 7 segmentli ekran, servis ve işletme modu
- Kablosuz uzaktan kumanda, radar, manyetik alan detektörü, paralel buton ve çekme anahtarı girişleri
- 2 adet reflektörlü fotosel
- Yay kırılma emniyeti ve halat gevşeme emniyeti
- EN 13241 uygunluğu

> Not: Makine bilgileri FGI "Thermo 80 mm" teknik veri sayfasından alınmıştır. Uzaktan kumandanın kodlama tipi, panoya erişim yetkisi, yazılım bileşen listesi (SBOM) ve yazılım sürümü belgede belirtilmediği için föylerde "belgede yok, sahada kontrol edilmeli" olarak ele alınmıştır.

## Laboratuvarlar

| Lab | Konu | Çıktı | Dosya |
|-----|------|-------|-------|
| 1 | Safety Architecture | Safety Function Map | `Lab1_Safety_Architecture.pdf` |
| 2 | IEC 62443 Mini Workshop | Zone / Conduit Diagram | `Lab2_IEC62443_Mini_Workshop.pdf` |
| 3 | Threat & Risk + Risk Matrix | Risk Register | `Lab3_Threat_Risk_Matrix.pdf` |
| 4 | Secure Remote Access | Secure Architecture | `Lab4_Secure_Remote_Access.pdf` |
| 5 | SBOM / CVE / Patch | Vulnerability Decision | `Lab5_SBOM_CVE_Patch.pdf` |
| 6 | CRA Incident Simulation | Incident Workflow | `Lab6_CRA_Incident_Simulation.pdf` |
| 7 | AI Safety Challenge | AI Fail-Safe Decision | `Lab7_AI_Safety_Challenge.pdf` |

## SWOT Analizi
7 laboratuvarın bulgularına dayanan, makinenin emniyet ve siber güvenlik açısından SWOT analizi: `SWOT_Analizi.pdf`

| | Olumlu | Olumsuz |
|---|---|---|
| **İç etken** | **Güçlü:** kapının düşmesine karşı mekanik koruma (yay kırılma + halat gevşeme emniyeti), standart fotosel, internete kapalı yapı, deadman modu | **Zayıf:** fotosel ile uzaktan kumanda aynı T100 panoda, panoya erişim kısıtı yok, kumandalar kişiye kayıtlı değil, açma-kapama kaydı yok, SBOM ve PL beyanı yok |
| **Dış etken** | **Fırsat:** katalogdaki opsiyonlar (öncü fotosel, halat kopma emniyeti), EN 12453 / IEC 62443 yol haritası, değişken kodlu kumanda, YZ'li kamera ile ek algılama, CRA'nın üreticiye getirdiği yükümlülükler | **Tehdit:** panoda yetkisiz mod değişikliği, kumanda sinyalinin kopyalanması, kayıp kumanda, sahte radar tetiklemesi, test edilmeden uygulanan yama, mevzuat baskısı (AB 2023/1230, CRA) |

## Özet
- **Tehlikeler:** kapanan kapının altında ezilme, yay/halat kopmasıyla kapının düşmesi, paneller arasında sıkışma, gergin burulma yayları, 400 V pano.
- **Emniyet fonksiyonları:** kapanırken engel algılanınca durma (fotosel), kapının düşmesini engelleme (yay kırılma ve halat gevşeme emniyeti), bakımda beklenmedik hareketi önleme (servis modu + LOTO).
- **Kritik bulgu:** fotosel ile kablosuz uzaktan kumanda aynı T100 panoya bağlı. Yay ve halat emniyeti ise mekanik olduğu için komutlardan bağımsız.
- **Hedef mimari:** merkezi geçiş kontrolü, değişken kodlu kumanda + kart/PIN, kişiye kayıtlı kumanda, açma-kapama kaydı, varsayılan kapalı erişim.
- **Zafiyet yönetimi:** üreticiden yazılım bileşen listesi (SBOM) istenir. Güncellemeler önce tek bir kapıda test edilir, ardından fotosel ve kapanma kuvveti testleri tekrarlanır. Güncelleme yoksa kablosuz kumanda girişi kapatılıp kapı elle kullanıma alınır.
- **Olay müdahalesi:** kapı mesai dışında yetkisiz açılırsa ilk iş insanları korumak (kapı altını boşaltmak, fotoselin çalıştığını test etmek), ardından panodaki ayarların fotoğrafını çekerek kanıtı saklamaktır. Panoyu resetlemek değiştirilmiş ayarları, yani kanıtı siler. Resmî CRA bildirimini üretici (FGI) yapar, depo olayı FGI'ye bildirir.
- **Yapay zekâ:** kapıya forklift ve yayayı algılayan yapay zekâlı bir kamera eklenirse, kamera yalnızca "dur" diyebilmeli, "kapan" diyememeli. Kamera yanılsa ya da bozulsa bile fotosel ve mekanik emniyetler kapıyı durdurmaya devam eder.

*Bu föyler bir eğitim çıktısıdır; resmî denetim veya uygunluk değerlendirmesi değildir.*
