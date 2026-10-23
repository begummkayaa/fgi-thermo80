# Safety 4.0 Bootcamp – Laboratuvar Föyleri (FGI Thermo 80 Sürümü)

**Ad Soyad:** Begüm Kaya  
**Grup:** Gece B  
**Tarih:** 22.10.2026

## Seçilen Makine
**FGI Kapı ve Yükleme Teknolojileri – Thermo 80 mm Seksiyonel Endüstriyel Kapı**

80 mm galvaniz çelik sandviç panelli, burulma yayları ve çelik halatlarla dengelenen, dişli elektrik motoruyla çalışan endüstriyel seksiyonel kapı (maks. 8000 x 6000 mm). T75/T100 kumanda panosu ile deadman, otomatik veya **uzaktan kumanda** ile kullanılabilir. Senaryoda bir lojistik deposunun yükleme kapısıdır; forklift ve yaya aynı açıklıktan geçmektedir.

**Teknik veri sayfasındaki temel özellikler:**
- T75/T100 kumanda panosu (IP54): 3 buton (aç-dur-kapat), 7 segmentli ekran, servis ve işletme modu
- Kablosuz uzaktan kumanda, radar, manyetik alan detektörü, paralel buton ve çekme anahtarı girişleri
- 2 adet reflektörlü fotosel
- Yay kırılma emniyeti ve halat gevşeme emniyeti
- EN 13241 uygunluğu

> Not: Makine bilgileri FGI "Thermo 80 mm" teknik veri sayfasından alınmıştır. Uzaktan kumandanın kodlama tipi ve panoya erişim yetkisi belgede belirtilmediği için föylerde "belgede yok, sahada kontrol edilmeli" olarak ele alınmıştır.

## Laboratuvarlar

| Lab | Konu | Çıktı | Dosya |
|-----|------|-------|-------|
| 1 | Safety Architecture | Safety Function Map | `Lab1_Safety_Architecture.pdf` |
| 2 | IEC 62443 Mini Workshop | Zone / Conduit Diagram | `Lab2_IEC62443_Mini_Workshop.pdf` |
| 3 | Threat & Risk + Risk Matrix | Risk Register | `Lab3_Threat_Risk_Matrix.pdf` |
| 4 | Secure Remote Access | Secure Architecture | `Lab4_Secure_Remote_Access.pdf` |

## Özet
- **Tehlikeler:** kapanan kapının altında ezilme, yay/halat kopmasıyla kapının düşmesi, paneller arasında sıkışma, gergin burulma yayları, 400 V pano
- **Emniyet fonksiyonları:** kapanırken engel algılanınca durma (fotosel), kapının düşmesini engelleme (yay kırılma ve halat gevşeme emniyeti), bakımda beklenmedik hareketi önleme (servis modu + LOTO)
- **Kritik bulgu:** fotosel ile kablosuz uzaktan kumanda aynı T100 panoya bağlı; yay ve halat emniyeti ise mekanik olduğu için komutlardan bağımsız
- **Hedef mimari:** merkezi geçiş kontrolü, değişken kodlu kumanda + kart/PIN, kişiye kayıtlı kumanda, açma-kapama kaydı, varsayılan kapalı erişim

*Bu föyler bir eğitim çıktısıdır; resmî denetim veya uygunluk değerlendirmesi değildir.*
