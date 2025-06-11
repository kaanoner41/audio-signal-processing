# audio-signal-processing

# 🎧 Kuş Sesi Sınıflandırması — FFT ve STFT ile Gerçek Zamanlı Ses Analizi

Bu projede, Python kullanılarak Kakapo ve Finch kuşlarının sesleri gerçek zamanlı olarak analiz edilip sınıflandırılmıştır. İki farklı frekans analiz yöntemi kullanılmıştır: **FFT (Hızlı Fourier Dönüşümü)** ve **STFT (Kısa Zamanlı Fourier Dönüşümü)**.

## 📌 Projenin Amacı

Farklı frekanslara sahip kuş türlerinin seslerini frekans-temelli analizle ayırt etmek ve bunu anlık olarak kullanıcıya sunmak. Uygulama, ses akışını işleyerek hangi kuşun öttüğünü tespit eder ve görselleştirir.

## 🛠️ Kullanılan Yöntemler

### 🔹 FFT (Fast Fourier Transform)

- Ses sinyali 1 saniyelik bloklara ayrılır.  
- Her blokta FFT uygulanarak zirve frekans (peak frequency) tespit edilir.  
- Frekansa göre sınıflandırma yapılır:  
  - <100 Hz → Sessizlik  
  - <800 Hz → Kakapo  
  - ≥2000 Hz → Finch  

Avantajları: Hızlı, gerçek zamanlı çalışabilir.  
Dezavantajları: Sadece en yüksek frekansa odaklandığı için hatalı sınıflandırma yapabilir.

### 🔹 STFT (Short-Time Fourier Transform)

- Tüm sinyale STFT uygulanır.  
- Zaman-frekans düzleminde 100–600 Hz arası Kakapo, 2000–6000 Hz arası Finch enerji seviyeleri hesaplanır.  
- Normalize edilmiş enerjiye göre anlık sınıflandırma yapılır.

Avantajları: Daha doğru ve kapsamlı analiz.  
Dezavantajları: Daha fazla işlem gücü gerektirir.

## Sonuç
FFT hızlıdır ama hassas değildir.

STFT daha detaylıdır ama yavaştır.

İkisini hibrit olarak kullanmak daha güçlü ve dengeli bir sistem sağlar.

## Geliştiriciler
Hüseyin Kaan Öner — h.oner2021@gtu.edu.tr

Muhittin Hamza Hanedar — m.hanedar2020@gtu.edu.tr

Kağan Alper — k.alper2021@gtu.edu.tr

