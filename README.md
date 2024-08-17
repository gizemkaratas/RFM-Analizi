# Müşteri Analizi ve RFM Segmentasyonu

Bu proje, e-ticaret verilerini kullanarak müşteri analizi yapmayı ve RFM (Recency, Frequency, Monetary) segmentasyonu oluşturmayı amaçlamaktadır. RFM analizi, müşterilerin alışveriş davranışlarını daha iyi anlamak ve pazarlama stratejilerini optimize etmek için kullanılan bir tekniktir.

## Proje İçeriği

### Veri Seti

Bu projede, "online_retail_II.xlsx" dosyasındaki "Year 2010-2011" sayfasından alınan e-ticaret verileri kullanılmaktadır. Veri seti, aşağıdaki bilgileri içermektedir:

- `Invoice`: Fatura numarası
- `StockCode`: Ürün kodu
- `Description`: Ürün açıklaması
- `Quantity`: Miktar
- `InvoiceDate`: Fatura tarihi
- `Price`: Ürün birim fiyatı
- `Customer ID`: Müşteri numarası
- `Country`: Ülke

### Veri Ön İşleme

- Veri setindeki eksik değerler ve iadeler temizlenmiştir.
- Fatura numarasının başında "C" olan iadeler çıkarılmıştır.
- Müşteriler için RFM metrikleri hesaplanmıştır:
  - **Recency**: Son alışveriş tarihinden bugüne kadar geçen gün sayısı
  - **Frequency**: Toplam alışveriş sayısı
  - **Monetary**: Toplam harcama miktarı

### RFM Skorları ve Segmentasyon

- **Recency**, **Frequency** ve **Monetary** metriklerine göre RFM skorları hesaplanmıştır.
- Müşteriler 1-5 arası skorlarla değerlendirilmiş, ardından segmentlere ayrılmıştır:
  - `hibernating`
  - `at_Risk`
  - `cant_loose`
  - `champions`
  - `loyal_customers`
  - `need_attention`
  - `new_customers`
  - `potential_loyalists`

### Sonuçlar

- Segmentlerin ortalama recency, frequency ve monetary değerleri analiz edilmiştir.
- Her segmentin genel müşteri davranışları detaylandırılmıştır.

## Kullanılan Kütüphaneler

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

## Kurulum ve Kullanım

1. Bu projeyi yerel bilgisayarınıza klonlayın:
   ```bash
   git clone [repo_url]

2. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas numpy matplotlib seaborn

3. Jupyter Notebook veya Python ortamında RFM_Analizi.ipynb dosyasını açın ve adımları takip ederek analizi gerçekleştirin.

