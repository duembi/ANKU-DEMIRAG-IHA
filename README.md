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

[cite_start]The ANKÜ-DEMİRAĞ İHA is a fixed-wing Unmanned Aerial Vehicle system capable of autonomously executing two main missions (Combat UAV and Kamikaze UAV) and one side mission (Avoidance of No-Fly Zones)[cite: 29].

| Feature | Value |
| :--- | :--- |
| **Airframe Model** | [cite_start]X-UAV Talon (Ready-to-fly kit) [cite: 96, 105] |
| **Flight Control Board** | [cite_start]Pixhawk The Cube Orange [cite: 96, 195] |
| **Mission Computer** | [cite_start]Raspberry Pi 5 8GB [cite: 96, 223, 226] |
| **Estimated Flight Time** | Approx. [cite_start]20.2 minutes (Fixed Flight) [cite: 49, 146] |
| **Total Weight** | [cite_start]3200 gr [cite: 49] |

### Autonomous Missions

[cite_start]The autonomous capabilities of our project are primarily achieved through advanced image processing algorithms running on the mission computer (Raspberry Pi 5)[cite: 226].

1.  [cite_start]**Autonomous Lock-On (Combat UAV Mission):** Real-time detection and tracking of rival UAVs[cite: 262, 264].
    * [cite_start]**Detection Algorithm:** **YOLOv8**, optimized for high accuracy and speed[cite: 287, 327].
    * [cite_start]**Tracking Algorithm:** **Deep-SORT**, used to maintain tracking during collisions or temporary loss of sight[cite: 374, 380, 406].
2.  [cite_start]**Kamikaze Mission:** Diving toward a QR code, reading the message, and executing a safe go-around maneuver[cite: 467, 481, 518].
3.  [cite_start]**Air Defense System (Side Mission):** Autonomous avoidance of no-fly zones (Geofence)[cite: 32, 522].

## 💻 My Contribution: Image Processing / Artificial Intelligence

[cite_start]I took an active role in one of the most critical and challenging parts of the project: the **Image Processing and Artificial Intelligence** sub-system[cite: 209]. My responsibilities included:

* [cite_start]**Model Selection and Optimization:** Selecting and integrating the optimal model, **YOLOv8**, after comparing the FPS and accuracy values of real-time object detection algorithms[cite: 287, 327].
* [cite_start]**Hardware and Integration:** Selecting and integrating the **Raspberry Pi 5 8GB** mission computer, chosen for its high processing power, low power consumption, and compact size to run the image processing algorithms[cite: 223, 226, 228, 229, 230].
* [cite_start]**Dataset Preparation:** Performing *data augmentation* and labeling processes to create a custom dataset consisting of **17,000 images** that simulate competition conditions[cite: 363, 365, 366].
* [cite_start]**Autonomous Lock-On/Tracking:** Incorporating the **Deep-SORT** object tracking algorithm to improve detection efficiency against the dynamic movements of rival UAVs[cite: 372, 406].
* [cite_start]**QR Code Decoding:** Developing an QR code reading algorithm for the Kamikaze mission that uses a **Homography Matrix** to remove perspective distortions [cite: 488, 490] [cite_start]and a **Gaussian Filter** to reduce noise in captured images[cite: 493, 494].



