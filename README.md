![image](https://github.com/user-attachments/assets/856d2b40-5e3d-47fc-bfe4-e902fd44e432)

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

- Champion (Şampiyonlar): Son alışverişi yakın tarihte yapmış, sık sık alışveriş yapan ve yüksek harcama yapan müşteriler.

- Loyal Customers (Sadık Müşteriler): Düzenli alışveriş yapan ancak son alışverişi biraz eski olan, orta-yüksek harcama yapan müşteriler.

- At Risk (Risk Altındaki Müşteriler): Daha önce düzenli alışveriş yapan ancak son dönemde alışveriş sıklığı düşmüş müşteriler.

- Needs Attention (Dikkat Gerektiren Müşteriler): Son alışverişi uzak tarihte olan, alışveriş sıklığı ve harcaması orta seviyede olan müşteriler.

- New Customers (Yeni Müşteriler): Kısa süre önce alışveriş yapmış ancak alışveriş sıklığı ve harcaması düşük olan müşteriler.

- Potential Loyalists (Potansiyel Sadık Müşteriler): Kısa süre önce alışveriş yapmış ve belirli bir sıklıkta alışveriş yapan, ancak harcaması daha düşük olan müşteriler.

- Cant Lose (Kaybedilemeyecek Müşteriler): Müşteri sadakati yüksek ancak son alışverişi biraz eski olan ve yüksek harcama yapan müşteriler.

- Hibernating (Uyuyan Müşteriler): Uzun zamandır alışveriş yapmamış, düşük alışveriş sıklığı ve harcaması olan müşteriler.

- Son Alışveriş Zamanı:

Uzun Süre: 6 ay ile 1 yıl veya daha fazla süre.
Kısa Süre: Son 1-3 ay.
Alışveriş Sıklığı:

Düşük Sıklık: Ayda 1 defadan daha az.
Orta Sıklık: Ayda 1-3 defa.
Yüksek Sıklık: Ayda 4 defa veya daha fazla.
Harcama Miktarı:

Düşük Harcama: Aylık harcama ortalamasının en alt yüzde 20'si.
Orta Harcama: Aylık harcama ortalamasının orta seviyesinde.
Yüksek Harcama: Aylık harcama ortalamasının en üst yüzde 20'si.
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

