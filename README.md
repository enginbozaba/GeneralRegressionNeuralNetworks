# GeneralRegressionNeuralNetworks <p/>

[tr]<p/>
GRYSA giriş katmanı, örüntü katmanı, toplama katmanı ve çıkış
katmanı olmak üzere dört katmandan oluşan ileri beslemeli
bir YSA modelidir. Geri beslemeli YSA’lardan farklı olarak
iteratif bir eğitim süreci gerektirmez. Yapısında bulunan her
bir katman farklı sayılarda nöronlardan oluşup, katmanlar
sırası ile bir sonraki katman ile bağlantılıdırlar [1]. GRYSA’nın
genel yapısı Şekil 1’de verilmiştir.

![Ağ yapısı](https://github.com/enginbozaba/GeneralRegressionNeuralNetworks/blob/master/grnn.JPG)

<p/>
İlk katman olan giriş katmanında, nöron sayısı verilerin
özelliklerinin sayısına, bir başka deyişle verinin boyutuna
eşittir. Örüntü katmanında, önceden de belirtildiği gibi nöron
sayısı eğitim setindeki veri sayısına eşittir. Bu katmanda
bulunan nöronlarda, eğitim verisi ile test verisi arasındaki mesafeler hesaplanır ve sonuçlar σ değeri ile birlikte radyal
tabanlı fonksiyondan geçirilerek ağırlık değerleri elde edilir.
Örüntü katmanından elde edilen bu ağırlık değerleri, toplama
katmanındaki pay ve payda nöronlarına beslenir. Payda
nöronunda, tüm ağırlık değerleri direkt toplanırken; pay
nöronunda, örüntü katmanındaki her nörondan gelen ağırlık
değerleri ile ilgili nöronda bulunan eğitim verisinin çıkış
değeri çarpılır ve bu çarpım değerlerinin toplamı, pay
nöronunun çıkış değeri olarak kabul edilir. Son olarak, çıkış
katmanında pay nöronundan gelen değer, payda nöronundan
gelen değere bölünerek ve sonuç değeri elde edilir.[1]

[1] Specht DF, Shapiro PD. “Generalization accuracy of
probabilistic neural networks compared with
backpropagation networks”. IJCNN-91-Seattle
International Joint Conference on Neural Networks,
Seattle, WA, USA, 08-12 July 1991.


General Regression Neural Networks are a forward-feed ANN model consisting of four layers.
* 
