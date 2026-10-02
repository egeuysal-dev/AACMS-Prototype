# AACMS Prototype v0.1 — Windows çalıştırma talimatları

## İndirme ve başlatma

1. GitHub Releases üzerinden `AACMS-Prototype-v0.1-Windows.zip` paketini indirin.
2. ZIP'in tamamını yazılabilir bir klasöre çıkarın.
3. `AACMS-Prototype` klasörünü açın.
4. `AACMS.exe` dosyasını çalıştırın.

EXE'yi ZIP içinden doğrudan çalıştırmayın; beraberindeki runtime dosyalarından ayırmayın. İmzasız prerelease için Windows SmartScreen yayıncı uyarısı gösterebilir.

## Sistem gereksinimleri

Windows 10/11 x64, Microsoft .NET Framework 4.6.2 veya üzeri ve Microsoft Evergreen WebView2 Runtime gerekir. Windows 11 üzerinde geliştirme doğrulaması yapılmıştır; Windows 10 test kapsamı tamamlanmamıştır. Eksik WebView2 Runtime'ı [Microsoft'un resmî sayfasından](https://developer.microsoft.com/en-us/microsoft-edge/webview2/) kurabilirsiniz. Browser runtime ZIP'e dahil değildir.

Python, Node.js, npm veya IDE kurmanız gerekmez. Windows runtime'ları hazır olduğunda prototip çevrimdışı çalışır.

## Arayüzü kullanma

- Veri kaynağı menüsünden temsili senaryo veya kayıtlı iz seçin.
- **Mühendislik** ve **MFD görünümü** arasında geçiş yapın; zaman çizelgesi ve oynatma kontrollerini kullanın.
- Yeni yerel hesaplama için **Tohum** değerini girip **Sentetik Koşu Çalıştır** düğmesine basın. Simülasyon, RWR gözlemleri, feature extraction ve model inference bu bilgisayarda çalışır; üretilen iz arayüze yüklenir.
- Ses için **Sesi aç** düğmesini kullanın; ses seviyesini ayarlayabilir veya sesi kapatabilirsiniz.
- Yeni sesleri dinlemek için **Uyarı seslerini dene → Füze sesleri · yalnız deneme** bölümünden seçim yapıp **Dinle** düğmesine basın. Bu sesler yalnız manuel denemedir; hesaplanmış füze tespiti anlamına gelmez.
- Uyumlu JSON izini **İz dosyası aç** ile yükleyin. Desteklenen biçimler `AACMS_SYNTHETIC_REPLAY_TRACE_V1` ve `AACMS_PROSPECTIVE_RWR_RESEARCH_REPLAY_V1`; dosya sınırı 5 MB'tır.

## Araştırma kapsamı

AACMS sentetik/offline bir araştırma prototipidir. Gerçek hava aracı sensörlerine bağlı değildir; operasyonel kullanım için doğrulanmamıştır ve flight-certified değildir. Model olasılığı, doğrulanmış tehdit seviyesi veya operasyonel karşı tedbir tavsiyesi anlamına gelmez. Eğitim ve otomatik karşı tedbir icrası yapılmaz.

Source code is not publicly distributed. A compiled prototype is provided for demonstration and research purposes.

[README](../README.md)
