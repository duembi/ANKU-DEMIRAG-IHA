
# 🚀 ANKÜ-DEMİRAĞ İHA - TEKNOFEST 2024 Savaşan İHA Yarışması

Bu repo, **TEKNOFEST 2024 Savaşan İHA Yarışması** için tasarlanan **ANKÜ-DEMİRAĞ İHA** projesinin kod ve dokümantasyonunu içermektedir. Projemiz, hava aracının kritik otonom görevleri yüksek doğruluk ve hızla gerçekleştirmesini hedeflemektedir.

## 🌟 Proje Özeti

ANKÜ-DEMİRAĞ İHA, iki ana görev (Savaşan İHA ve Kamikaze İHA) ve bir yan görevi (Uçuşa Yasaklı Bölgelerden Kaçınma) otonom olarak yerine getirebilen sabit kanatlı bir insansız hava aracı sistemidir.

| Özellik | Değer |
| :--- | :--- |
| **Gövde Modeli** | X-UAV Talon (Hazır Kit) |
| **Uçuş Kontrol Kartı** | Pixhawk The Cube Orange |
| **Görev Bilgisayarı** | Raspberry Pi 5 8GB |
| **Tahmini Uçuş Süresi** | Yaklaşık 20.2 dakika (Sabit Uçuş) |
| **Toplam Ağırlık** | 3200 gr |

### Otonom Görevler

Projemizin otonom kabiliyetleri, özellikle görev bilgisayarı (Raspberry Pi 5) üzerinde çalışan gelişmiş görüntü işleme algoritmaları ile sağlanmaktadır.

1.  **Otonom Kilitlenme (Savaşan İHA Görevi):** Rakip İHA'ların gerçek zamanlı tespiti ve takibi.
    * **Tespit Algoritması:** Yüksek doğruluk ve hız için optimize edilmiş **YOLOv8**.
    * **Takip Algoritması:** Çarpışma ve kayıp durumlarında izlemeyi sürdürmek için **Deep-SORT**.
2.  **Kamikaze Görevi:** QR koda dalış, mesaj tespiti ve güvenli pas geçme.
3.  **Hava Savunma Sistemi (Yan Görev):** Uçuşa yasaklı bölgelerden (Geofence) otonom kaçınma.

## 💻 Görüntü İşleme / Yapay Zeka Katkım

Ben, projenin en kritik ve zorlu kısımlarından biri olan **Görüntü İşleme ve Yapay Zeka** alt sisteminde aktif rol aldım. Görevlerim şunları içeriyordu:

* **Model Seçimi ve Optimizasyon:** Gerçek zamanlı nesne tespiti için FPS ve doğruluk değerleri karşılaştırılarak en uygun model olan **YOLOv8**'in seçilmesi ve entegrasyonu.
* **Donanım ve Entegrasyon:** Görüntü işleme algoritmalarını çalıştırmak üzere yüksek işlem gücüne, düşük güç tüketimine ve küçük boyuta sahip olan **Raspberry Pi 5 8GB** görev bilgisayarının seçilmesi ve sisteme entegrasyonu.
* **Veri Seti Hazırlığı:** Yarışma koşullarını simüle eden **17.000 adet görüntüden** oluşan özel bir veri seti oluşturulması için *data augmentation* ve etiketleme işlemlerinin gerçekleştirilmesi.
* **Otonom Kilitlenme/Takip:** Rakip İHA'ların dinamik hareketlerine karşı algılama verimini artırmak için **Deep-SORT** nesne takip algoritmasının sisteme dahil edilmesi.
* **QR Kod Çözümleme:** Kamikaze görevi için, görüntülerdeki perspektif bozulmalarını gidermek amacıyla **Homografi Matrisi** ve gürültü azaltmak için **Gauss Filtresi** kullanan QR kod okuma algoritmasının
