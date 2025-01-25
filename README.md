# Doğal Dil İşleme Teknolojileri ve Günlük Hayattaki Kullanımları
NLP yani Doğal Dil İşleme, doğal dillerin kurallı yapısının çözümlenerek anlaşılması veya yeniden üretilmesi amacıyla insanların kendi aralarında anlaşmak için kullandıkları dili insan-bilgisayar etkileşimini en üst düzeye çıkarabilmek veya farklı doğal dilleri kullanan insanlar arasında iletişimi güçlendirmek üzere çözümler üreten bilim alanıdır.

Doğal dil işlemenin amacı yalnızca kurallı bir dil yapısının çözümlenerek anlaşılmasını olmayıp aynı zamanda çözümlenebilen bir dile ait yapının yeniden üretilebilmesini sağlamaktır. Doğal dil alanında yapılan çalışmalar doğrudan dil bilimiyle ilgili olduğu için her bir özel dil için ayrı ayrı çalışmaların yürütülmesi ve analiz süreçlerinin ayrışık bir biçimde yeniden yapılması gerekmektedir. Bu nedenle bir dil üzerinde yapılan doğal dil işleme süreçleri başka bir dile doğrudan aktarılamayabilir.

>"Günümüzde kuruluşlar; e-postalar, metin mesajları, sosyal medya haber akışları, videolar ve ses dosyaları gibi çeşitli iletişim kanallarından büyük hacimli ses ve metin verilerine sahiptir. Bu verileri otomatik olarak işlemek, mesajdaki niyeti veya duyguyu analiz etmek ve insan iletişimine gerçek zamanlı olarak yanıt vermek için NLP yazılımı kullanırlar."(amazon web services)

## Doğal Dil işleme Prensipleri
Doğal dil işleme kavramını ele aldığımızda karşımıza biçimbilimi olarak bilinen morfoloji karşımıza çıkıyor. Morfoloji, dilbilimin bir dalı ve özünde bir dilin anlam taşıyan en küçük birimlerinin yapısını inceliyor.

NLP üzerinde literatür üzerindeki bazı anahtar kelimeler

* **Söz Dizimi (Syntax)** : Dillerdeki cümle kurma ilke ve kurallarını, cümlelerin esnekliğini inceleyen dilbilim dalı.
* **Anlamsal Analiz (Semantic):** Sözcük ve cümlelerin anlamı, aynı sözcüklerin farklı anlamları ve dile getirilen bağlamı inceleyen dilbilim dalı.
* **Anlam Belirsizliği (Disambiguation):** Bir kelimenin hangi bağlamda ne anlama geldiğine karar verilmesi süreci.
* **Doğal dil :** Kullanıcılar tarafından bilinçli bir planlama olmaksızın tekrar edilerek evrilmiş dil.

Doğal dilden üretilen metinler veya ses(konuşma) verileri belirli adımlardan geçirilerek işlendikten sonra bilgisayar sistemlerinin anlayacağı formata geldikten sonra işlenip analiz edilmektedir.
Doğal dil işlenmesi sırasında metnin gereksiz ifadelerden ve noktalamalardan ayrıştırılması, morfolojik analiz, söz dizimsel analiz ve anlam bilimsel analiz adımları sırasıyla yapılmaktadır. Bu sürece dilin matematik analizi de denmektedir.
<!--  IMAGE -->
! [DDL] (https://www.hasanbaskin.com/wp-content/uploads/2021/01/1.png)

 ## Doğal Dil Ön İşleme Süreci
 Bilgisayar ortamında aldığımız metin veya ses verileri direkt olarak doğal dil işleme sürecine sokulmaz. Çünkü aldığımız verinin her zaman düzenli , anlam karışıklığı olmayan , doğru noktalama işaretleri ile ayrılmış bir şekilde bulamıyoruz. Bu doğrultuda aldığımız verilerin bir ön işleme adımlarından geçerek girdi olarak aldığımız metnin en doğru şekilde işlenmesine yardımcı olacaktır.

 Doğal Dil ön işleme adımlarından ilki sözcüksel analiz(lexical)dir. Sözcüksel analiz , bir metnin tüm yığınlarının daha küçük parçalara, paragraf, cümle ve kelimelere ayrıştırılarak kelimerin yapısını tanımlamayı ve analiz etmeyi sağlar. Doğal dil ön işlemenin amacı ham veri analiz öncesinde bir takım ön işlemlerden geçirilerek daha sonra asıl doğal dil işleme modüllerinde işlenmek üzere hazır hale getirilmesidir. Daha sonra dört farklı ön işlem aşamasından geçirilen metinler doğal dil işlemenin asıl modüllerinde işlenmektedir. Bahsi geçen ön işlemler şunlardır;

 1. **Tokenizasyon:** Bir metni kelimeler, deyimler ve cümleler gibi daha küçük birimlere ayırma işlemidir. Bu süreç, metnin daha anlamlı bir şekilde analiz edilmesini sağlar.
Metnin işlenebilmesi için kelimere (word2vec) veya gerektiği durumlarda cümlelere ayrılması gerekmektedir. Bu aşamada bütün bir metni oluşturan her bir sözcük tek tek ayrılmaktadır. Makine Öğrenmesi ile elde edilen vektörlerin doğal dil işleme tarafından kelimenin doğru temsil edilmelerini etkileyen üç temel etken vardır. Bu temel etkenler şunlardır:
    * **Eğitimde Kullanılan Derlemin Büyüklüğü:** Derlem büyüklüğünün artması kelime vektörlerinin ağırlıkları üzerinde yapılacak olan hata düzeltme işlemleri arttıracaktır. Dolayısıyla eğitim süreside artacaktır.
    * **Eğitilen Vektörlerin Boyutu:** Word2vec’te vektörlerin boyutu 300 ile 1000 arasında olacak şekilde belirlenmesi optimum verimlilik için tavsiye edilmektedir.
    * **Komşu Kelimelerin Sayısı:** Word2vec için 5 ile 10 komşuluk adetleri önerilmektedir.

2. **Stop Words:** Anlam olarak gereksiz veya etkisiz kelimeler olarak adlandırılır. Aldığımız metnin anlam içermeyen kelimeleri , kelime gruplarını belirleyerek bu kelimeleri metinden ayıklama işlemedir.
Bilgisayar dilinde, etkisiz kelimeler, doğal data dilinin (text) işlenmeden önce veya sonra filtrelenmiş kelimeleridir.[1] Genelde etkisiz kelimeler bir dildeki sık kullanılan kelimeleri kapsar, etkisiz kelimeler için işleme araçları tarafından kullanılan tek evrensel bir liste bulunmamaktadır, hatta tüm araçların böyle bir liste kullandığı bile söylenemez. Bazı kullanılan araçlar cümle aramalarını daha iyi destekleyebilmek için etkisiz kelimelerin çıkarılmasından kaçınmaktadır.(vikipedia)

    Verilen metne göre etkisiz kelimeler grubu değişmektedir. Türkçede de bazı etkisiz kelimeler “hangi, acaba, ve, böylece, madem, elbette, kadar, ise, henüz, hem” vs. örnek verilebilir.  

3. **Stemming:** Dilsel morfolojide ve bilgi erişiminde, kök oluşturma(stemming) Çekimli (veya bazen türetilmiş) kelimeleri kelime köküne, tabanına veya köküne indirgeme süreci biçimi genellikle yazılı bir sözcük biçimidir. Kökün, kelimenin morfolojik kökü ile aynı olması gerekmez; Bu kök kendi başına geçerli bir kök olmasa bile, ilgili kelimelerin aynı kökle eşleşmesi genellikle yeterlidir. (vikipedia) 

    Yani stemming işlemi metindeki kelimelerin köklerini bulma işlemidir. Bunun için çeşitli algoritmalar kullanılmaktadır. Aynı kelimelerden türeyen kelimelerin farklı anlamlarda kullanılmasının önüne geçmek için kullanılır ve oldukça önemlidir.

4. **Named Entity Recognation (NER):** Adlandırılmış varlık tanıma, yapılandırılmamış metinde belirtilen adlandırılmış varlıkları kişi adları, kuruluşlar, konumlar, tıbbi kodlar, zaman ifadeleri, miktarlar, parasal değerler, yüzdeler vb. . Wikipedia (İngilizce)
NER , bir metinde o metini anlamak için varlık sınıflarını ayırma işlemidir. Bu sayede metnin daha iyi anlaşılmasını sağlanıp belirlenen anahtar kelimeler ile o metinde varlıkları eşleştirerek metni anlamamızı kolaylaştırır.

    ! [NER] (https://kimola.com/images/mh/posts/f3267499-be36-4770-84ad-5e24fa82484f.webp)

    Örnek metinde görüldüğü üzere metinden NER modeli üzerinden tanıtılmış olan event , org , person , gpe , time niteliklerini metin üzerinde gezerek ilgili etiketi ilgili kelimenin üzerine atıyor. Temel olarak NER modelinde iki aşamalı süreç vardır bunlar adlandırılmış bir varlığı algılama ve varlığı kategorilere ayırma işlemidir.
    Varlıkları oluşturup modelimize tanımlatıp ardından iyi bir eğitim sürecine tabi tutmalıyız. Bu şekilde metinlerde yüksek başarı ile gruplandırma işlemi gerçekleştirilir.

# Normalizasyon
Doğal dil işleme aşamaları arasında verinin analiz edilmesi sürecinde sahip olan kelimelerin köklerinin tespit edilmesi işlemidir. Ön işlemler arasında yer alan Stemming uygulaması bir normalizasyon yöntemidir. Yalnızca basit fiil formları ile çalışmaktadır ve kelimelerin eklerini kaldırarak sezgisel ilerleyen bir süreçtir. Kelimelerin köklerine erişilmesi sırasında kullanılan iki farklı yöntem bulunmaktadır.

 1. **Stemming:** Ek almış olarak bulunan kelimede ön eklerin ve son eklerin bulunduğu bir listeyi referans alarak kelimenin başlangıcını veya sonunu kesmeye çalışmaktadır. Stemming normalizasyon aşamasının amacı ön işlem olarak ek almış olan aynı kelimelerin köklerinin tespit edilmesi ve bu kelimelerin farklı kelimeler olarak anlaşılmasının önüne geçilmesi için gerçekleştirilmektedir.
 2. **Lematizasyon :** Kelime kökü (lemma), bir dildeki sözcüklerin sözlüklerde yer alan standart biçimidir. Lematizasyon adı verilen süreç, çekimli sözcüklerin kelime köküne indirgenmesini sağlar. Lematizasyon, çeşitli diller için doğal dil işleme (DDİ) araçlarında metinlerin ön işleme aşamasında sözcüklerin farklı yapılarından normal biçimlerine dönüştürülmesinde kullanılır.

 ## Doğal Dil İşleme Süreci

 ! [DDL Piramid] (https://www.hasanbaskin.com/wp-content/uploads/2021/01/3-640x298.png)

 ## Morfolojik Analiz
 Biçimbirimsel (Morphological) Analiz, bir metin içerisinde yer alan herkelimenin bilgisayar tarafından otomatik olarak çözümlenmesi işlemidir. Kelimelerin, kök ve eklerine ayrıştırılıp, görevlerinin belirlenmesi ilgilenir.

**Örnek:** çiçekler -> çiçek (kök) + ler (çoğul eki) [‘çiçek’ ve ‘ler’ birer morfemdir]
Morphem ‘ler gövdeler (stem) (kelimenin ana morpheme dir ve kelimeye anlamını verir) ekler (affixes) (kelimenin anlamı şekil değiştirir.)

![Morfolojik Analiz] (https://www.hasanbaskin.com/wp-content/uploads/2021/01/4.png)

## Syntactic Analiz (Söz Dizimsel Analiz)
Sözdizimsel analiz, sözdizimini (syntax) veya tümceyi/cümleyi oluşturan morfolojik öğelerin özne , nesne , yüklem vs. hiyerarşik kurallara uyumunu karşılaştırarak ölçümlemektir. Böylece söz dizimin anlamlı olup olmadığının ölçülebilmesi için düzenleyici bir süreç gerçekleşmiş olur.

Morfolojik analiz sonuç çıktıları kullanılarak cümle içerisindeki kelimelerin ve kelimeler arasında ilişkinin analizinin yapıldığı süreçtir.

![Sözdizimsel Analiz] (https://www.hasanbaskin.com/wp-content/uploads/2021/01/5.png)

## Anlamsal Analiz ( Semantik Analiz)
Anlambilimsel analiz, sözdizimini oluşturan morfolojik ögelerin ayrılması, yani sözdizimsel analiz ile anlam taşıyan kelimelerin sınıflandırılması işleminden sonra gelen anlamlandırma veya anlama sürecidir.Bu süreçte anlam taşıyan kelimelerin, ekler ve cümle hiyerarşisi içindeki konumlarının saptanması sayesinde birbirleri ile ilişkileri kurulabilir. Bu ilişkiler anlam çıkarma, fikir yürütme gibi ileri seviye bilişsel fonksiyonların oluşturulmasında ham bilgi olarak kullanılacaktır.(vikipedia)

## Kaynakça 
https://aws.amazon.com/tr/what-is/nlp/

https://tr.wikipedia.org/wiki/Do%C4%9Fal_dil_i%C5%9Fleme

https://yapayzeka.itu.edu.tr/arastirma/dogal-dil-isleme

https://miuul.com/not-defteri/dogal-dil-islemede-temel-kavramlara-hizli-bir-bakis

https://www.hasanbaskin.com/dogal-dil-isleme-natural-language-processing/#onislemler

https://tr.wikipedia.org/wiki/Etkisiz_kelimeler

https://en.wikipedia.org/wiki/Stemming

https://en.wikipedia.org/wiki/Named-entity_recognition

https://kimola.com/blog/named-entity-recognition-ner-nedir-ve-nerelerde-kullanilir

https://dergipark.org.tr/tr/download/article-file/1974051

https://tr.wikipedia.org/wiki/Do%C4%9Fal_dil_i%C5%9Fleme#:~:text=EF%3A%20ek%20fiil-,Anlambilimsel%20(semantik)%20analiz,gelen%20anlamland%C4%B1rma%20veya%20anlama%20s%C3%BCrecidir
