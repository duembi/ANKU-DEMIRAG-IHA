TR
# 🚀 ANKÜ-DEMİRAĞ İHA - TEKNOFEST 2024 Savaşan İHA Yarışması

Bu repo, **TEKNOFEST 2024 Savaşan İHA Yarışması**na katılan **ANKÜ-DEMİRAĞ İHA** takımının kod ve dokümantasyonunu içermektedir. Projemiz, hava aracının kritik otonom görevleri yüksek doğruluk ve hızla gerçekleştirmesini hedeflemektedir.

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



--------------------------------------------------------------------------------------------------------------------------------------------------------------------





EN
# 🚀 ANKÜ-DEMİRAĞ İHA - TEKNOFEST 2024 Combat UAV Competition

This repository contains the code and documentation for the **ANKÜ-DEMİRAĞ İHA** team participating in the **TEKNOFEST 2024 Combat UAV Competition**. Our project aims for the aircraft to perform critical autonomous missions with high accuracy and speed.

## 🌟 Project Summary

The ANKÜ-DEMİRAĞ İHA is a fixed-wing Unmanned Aerial Vehicle system capable of autonomously executing two main missions (Combat UAV and Kamikaze UAV) and one side mission (Avoidance of No-Fly Zones).

| Feature | Value |
| :--- | :--- |
| **Airframe Model** | X-UAV Talon (Ready-to-fly kit)  |
| **Flight Control Board** | Pixhawk The Cube Orange  |
| **Mission Computer** | Raspberry Pi 5 8GB  |
| **Estimated Flight Time** | Approx. 20.2 minutes (Fixed Flight)  |
| **Total Weight** | 3200 gr  |

### Autonomous Missions

The autonomous capabilities of our project are primarily achieved through advanced image processing algorithms running on the mission computer (Raspberry Pi 5)[cite: 226].

1.  **Autonomous Lock-On (Combat UAV Mission):** Real-time detection and tracking of rival UAVs.
    * **Detection Algorithm:** **YOLOv8**, optimized for high accuracy and speed.
    * **Tracking Algorithm:** **Deep-SORT**, used to maintain tracking during collisions or temporary loss of sight.
2.  **Kamikaze Mission:** Diving toward a QR code, reading the message, and executing a safe go-around maneuver.
3.  **Air Defense System (Side Mission):** Autonomous avoidance of no-fly zones (Geofence).

## 💻 My Contribution: Image Processing / Artificial Intelligence

I took an active role in one of the most critical and challenging parts of the project: the **Image Processing and Artificial Intelligence** sub-system[cite: 209]. My responsibilities included:

* **Model Selection and Optimization:** Selecting and integrating the optimal model, **YOLOv8**, after comparing the FPS and accuracy values of real-time object detection algorithms.
* **Hardware and Integration:** Selecting and integrating the **Raspberry Pi 5 8GB** mission computer, chosen for its high processing power, low power consumption, and compact size to run the image processing algorithms.
* **Dataset Preparation:** Performing *data augmentation* and labeling processes to create a custom dataset consisting of **17,000 images** that simulate competition conditions.
* **Autonomous Lock-On/Tracking:** Incorporating the **Deep-SORT** object tracking algorithm to improve detection efficiency against the dynamic movements of rival UAVs.
* **QR Code Decoding:** Developing an QR code reading algorithm for the Kamikaze mission that uses a **Homography Matrix** to remove perspective distortions and a **Gaussian Filter** to reduce noise in captured images.



