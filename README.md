# Reklam harcamaları ve satış tahmini

TV, radyo ve gazete reklam bütçeleriyle satış miktarı arasındaki ilişkiyi inceleyen bir regresyon çalışması. Bu çalışma satış tahmini içindir; reklamların nedensel etkisini veya yatırım getirisini (ROI) ölçmez.

## Veri ve yöntem

- Veri: [Advertising veri seti](https://www.statlearning.com/s/Advertising.csv), 200 pazar; TV, Radio, Newspaper bütçeleri ve Sales.
- Kod ve veri: [not defteri](reklam_etki_analizi/reklam_etki_analizi.ipynb) · [CSV](reklam_etki_analizi/Advertising.csv).
- %80 eğitim / %20 test ayrımı (random_state=42); scikit-learn LinearRegression.
- Testte üç değişkenli modelin R² değeri yaklaşık **0,90**, MSE değeri **3,17**. Gazete değişkeni çıkarıldığında test R² değeri **0,9006**.

## İş yorumu ve sınırlar

Bu veri setinde TV ve radyo bütçeleri satış tahminiyle ilişkili görünüyor. Gazete değişkeninin ek tahmin katkısı bu ayrımda düşük. Katsayılar ve korelasyonlar tek başına kanalın gerçek getirisi, nedensel etkisi veya bütçe değişikliğinin sonucunu göstermez. Bütçe kararı için kâr/maliyet verisi ve uygun bir deney ya da nedensel ölçüm gerekir.

## Çalıştırma

Python 3.10+ ile pandas, numpy, matplotlib, seaborn, scikit-learn ve jupyter paketlerini kurun. reklam_etki_analizi klasöründe Jupyter'ı başlatıp not defterini açın; not defteri CSV'yi aynı klasörden okur.
