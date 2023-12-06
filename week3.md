## HTTP Methods
-GET - Veri almak – listelemek

-POST – Kaynağa veri göndermek

2 taneparametre alır, path ve fonksiyon (request ve respons elemanlarını alır)

-PUT – Kaynaktaki verinin tamamının değiştirilmesi

-PATCH – Kaynaktaki verinin bir kısmını değiştirilmesi

-DELETE – Verilerin silinmesi

-HEAD – Get methoduna benziyor.

Yanıt sadece başlıkları içerir.

Kaynağın varlığını kontrol etmek ya da başlıkları almak için

-OPTIONS – Belirtilen kaynağa erişim seçeneklerini sorgular (Get,post,put..)

-TRACE – İsteğin sunucuya nasıl geldiğini ve geri dönüş yolunu izlemek için

Genelde hata ayıklama veya izleme için

-CONNECT – İstemci ve sunucu arasında güvenli bir iletişim kurmak için
## HTTP Status Code
### 1xx – Bilgilendirme
100 – İstek başarıyla alındı devam edilebilir.

101 – Sunucunun hangi protokolde geçtiğini belirtir.

102 – Sunucu isteği aldı ve işliyor ama henüz yanıt vermedi.

103 –

### 2xx – Başarılı
200 – Başarılı/OK

201 – Yeni kaynak oluşturuldu.

203 – Yetersiz bilgi

204 – İçerik yok

205 – İçeriği baştan al

206 – Kısmi içerik

207 – Çoklu statü

210 – Farklı içerik
### 3xx – Yönlendirme
300 - Çoklu seçenek (istemci birden fazla seçenekten birini seçmeli)

301 - Kalıcı yönlendirme

302 - Geçici yönlendirme

303 - Diğerlerine bak (kaynağın konumu farklı isteği tekrar gönder)

304 - Güncellenmemiş/Değiştirilmemiş

305 - Proxy kullan

307 - Geçici olarak yeniden yönlendirme
### 4xx – İstemci Hatası (client-frontend)
400 – Kötü istek (sunucu tarafından anlaşılmayan istek)

401 – Yetkilendirme Hatası (kullanıcı yetkisinin olmadığı bir istek atarsa)

402 – Ödeme gerekli 

403 – Yasaklanmış (erişim izni yok)

404 – Bulunamadı

405 – İzin verilmeyen yöntem

406 – Kabul edilemez
### 5xx – Sunucu Hatası (server-backend)
500 – Sunucu hatası

501 – İstek uygulanmadı 

503 – Sunucu Kullanılamıyor

504 – Ağ geçidi zaman aşımı

505 – http sürümü desteklenmiyor

## Fonksiyonlar
Cookie (çerez): Kullanıcıyı tanımlamak veya bir veri kaydetmek için kullanıcının tarayıcısına 
gönderdiğimiz paket. 3 farklı metodu var: local, session, cookie. Tüm çerezleri kabul et-reddet. Kabul 
ettiğimiz zaman bir istek göndermiş oluyoruz ve resp.cookie tarayıcıya bir cookie ekliyor.

Clear.cookie: varolan cookileri silmek için. Yani kullanıcı izinleri reddedince cookileri silmemiz 
gerekiyor.

Res.send: HTTP yanıtlarını oluşturup göndermek için kullanılan temel bir fonksiyondur. text, html 
veri, obje gbi çeşitli birçok şey gönderebiliyoruz.

Res.set: geriye gönderdiğimiz verinin tipini belirleriz. Headerları ayarlarız (headerların içerisinde de 
content tipi ve kullanıcıyı ayırt etmek için kullanıcının tokenını belirliyoruz.

Header: HTTP isteği veya yanıtının anahtar bilgilerini taşıyan öğeler. isteğin içerisinde giden gelen 
kısım
url gönderiyoruz metod gönderiyoruz aynı zamanda headerlar var. Headerlarla da content tipi ve 
kullanıcıyı ayırt etmek için kullanıcının tokenını belirliyoruz

res.type: responsu gönderirken respons typını belirliyoruz. Html, image .. çeşitli şeyler belirleyebiliriz
http isteğine nasıl veri eklerim? Query parametresi olarak (get istekleri de oluyor içinde) 
ya da body nin içine gönderip ordan kullanabiliriz.

Req.body - Veriyi nasıl yakalarım? 
Requestten gelen veriyi geriye göndermek istiyorsak – console.log(mesaage req.body)
## Query Parametreleri
Query parametreleri -kontrol için kullanılır. Yani dataları query’e gönderdiğimizde aslında bir kayıt 
yapmasını istiyoruz. Path?parametreninkeyi şeklindedir. 

? – query parametrelerinin geldiğini belirtir.

Body’ye gönderdiğimiz datalar kayıt için gönderdiğimiz datalardı. Ancak query e gönderdiğimizde bir 
kontrol yapılmasını istiyoruz.

## Query Parametre ile Parametre farkı
Parametreler, bir işlevin veya fonksiyonun aldığı değerlerdir. Query parametreleri ise URL içindeki 
verileri temsil eden ve anahtar-değer çiftleri olarak sunulan veriler. Genelde http GET istekleri ile 
iletilir.

Query parametrelerini içerde nasıl yakalarım?: Query parametrelerine erişim sağlamak için: request 
nesnesini kullanırız.
## Ara kontrolü(middleware)
HTTP taleplerini işlemek için kullanılır. Gelen isteği değiştirebilir, yanıtı değiştirebilir ya da işleyebilir.

3 adet parametre alır.

Request: Gelen HTTP talebini temsil eder.

Response: http yanıtını temsil eder.

Next: Bir sonraki middleware veya yönlendirme işlemini tetiklemek için çağırılır. Next çağırılmazsa 
isteğin işlenmesi sona erer. Yönlendirmeye geçemez çünkü.
## Client-Server Farkı
Client sunucudan hizmet veya veri talep eden tarafı ifade eder. Bu kullanıcının cihazını veya tarayıcısını 
temsil eder.

Server ise istemcilerden gelen taleplere yanıt verir, veritabanı sorgularını işler ve başka türde işlemler 
gerçekleştirir.

Kullanıcı, bir uygulamadan veya tarayıcıdan backend sunucuya veri gönderir. Bu veri, backend 
tarafında işlenir ve güncellendikten sonra istemciye yeni bir yanıt gönderilir. Örneğin, bir web 
uygulamasında kullanıcı adını değiştirdiğinizde, bu değişiklik backend tarafında işlenir ve güncellenen 
kullanıcı adını içeren bir yanıt, istemciye gönderilir.

## Business ve logici neden client tarafına koymuyoruz?
kullanıcının kontrolü altında olan ve genellikle tarayıcı veya mobil uygulama gibi bir istemci 
uygulamasını temsil eden bir ortamdır. Bu nedenle, istemci tarafında yer alan kod ve veriler, 
kullanıcı tarafından potansiyel olarak değiştirilebilir ve manipüle edilebilir. Bu yüzden sunucu 
tarafında yaparız. Server tarafı verilerin güvenli bir şekilde saklanmasını, işlenmesini ve kontrol 
edilmesini sağlar.

## Nest API standartları
1- Çoğul isim kullanılmalı

2- Fiil değil isim kullanılmalı

3- Id’ler parametreler ile ayrılmalı

4- Hiyerarşik yapı kurulmalı (parametre ile)

5- Birden falza gelime kullanacaksak – ile ayırılır.

6- Filtre istekler de query parametresi olarak kullanılmalı (örneğin bir takımdaki orta saha 
oyuncularını istiyorsak, yani bir filtreleme istiyorsak query kullanmalıyız.)

7- Eğer bir API değiştireceksek versiyonlama kullanmalıyız v1,v2 gibi.

1-(get)çoğul isim(fiil olmaz) kullanılmalı. (Örneğin fimadaki takımların geriye döndüren bir yapı 
istediğimizde team yerine teams dememiz gerekiyor)

2-(get)Belirli bir takımı getirmek için teams/parametre olarak idyi veririz yani teams/1 gibi.

3-(post) yeni bir takım oluşturmak için (delete) takımı sil, takımı update et, get belirli bir takım 
elemanını getir. Teams/1/12 

4-(Post)player oluştur. Update (put) ve sil(delete) lazım. Player-takım koleksyonları.
## Swagger
Swagger, yazılım geliştiricilerin Restful api’lerini tasarlamasına, oluşturmasına, belgelemesine 
ve rahat bir şekilde kullanmasını sağlayan doküman oluşturma tool’u dur.
## FS modüle
FS (file system) modül tüm dosya okuma, yazma, izin verme gibi işlemlerinizi 
gerçekleştirmenizi yarayan fonksiyonların bulunduğu bir modüldür. Dosya okuma, yazma, veri 
ekleme, dosyayı silme gibi birçok metodu vardır
