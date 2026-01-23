# Explorer Tab Utility Window Hider - Windhawk Mod

Explorer Tab Utility programının penceresinin oluşmasını ve görünmesini engelleyen bir Windhawk modudur. Program arka planda çalışmaya devam eder ancak penceresi asla görünmez.

## Sorun

Explorer Tab Utility normalde arka planda çalışır, ancak bazen bilgisayar başlangıcında penceresi görünür hale gelir ve manuel olarak kapatılması gerekir.

## Çözüm

Bu Windhawk modu, Explorer Tab Utility'nin penceresini tamamen engeller. Program tüm işlevselliğiyle arka planda çalışmaya devam eder, ancak yapılandırma penceresi asla görünmez.

## Nasıl Çalışır

Mod aşağıdaki Windows API fonksiyonlarını hook'lar:

- **ShowWindow / ShowWindowAsync** - Pencerenin gösterilmesini engeller
- **CreateWindowExW** - Ana pencereyi oluşturulduktan hemen sonra gizler
- **SetWindowPos** - Pencerenin konumlandırma yoluyla görünür yapılmasını engeller
- **SetForegroundWindow / BringWindowToTop** - Pencerenin öne getirilmesini engeller

## Kurulum

1. [Windhawk](https://windhawk.net/)'ı indirin ve kurun
2. Windhawk'ı açın
3. "Create a new mod" (Yeni mod oluştur) seçeneğine tıklayın
4. `explorer-tab-utility-window-hider.wh.cpp` dosyasının içeriğini editöre yapıştırın
5. "Compile" (Derle) butonuna tıklayın
6. Modu etkinleştirin

## Hedef İşlem

Bu mod yalnızca `ExplorerTabUtility.exe` işlemini hedefler ve diğer programları etkilemez.

## Notlar

- Mod, pencereyi tamamen engellemek için birden fazla Windows API fonksiyonunu hook'lar
- Program arka planda çalışmaya devam eder ve tüm işlevler (kısayollar, Explorer sekmeleri vb.) çalışır
- Yapılandırma değişiklikleri yapmak için modu geçici olarak devre dışı bırakmanız gerekebilir

## Lisans

MIT License
