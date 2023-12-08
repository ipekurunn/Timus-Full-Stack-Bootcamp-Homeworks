## JWT
JWT(jsonwebtoken) web uygulamalarında kimlik doğrumala ve yetkilendirme süreçlerini kolaylaştırmak için kullanılır.

3 bölümü vardır:

header: bu bölüm kullanılan algoritmanın ve tokenın belirtildiği bir json nesnesidir.

Payload:JWT içinde taşınan verileri içeren bir Json nesnesi. Kullanıcı kimliği, yetkiler ve token süresi gibi bilgileri içeriyor.

Verify signature: doğrulama yapar. Yani bana gelen tokenin gerçek token olduğunu anlamamızı sağlar. 

Decode işlemi, bu bölümlerden elde edilen verileri okunabilir bir formata dönüştürmek anlamına gelir.
## Nullish Operator
Null veya undefined değerleri kontrol etmek için kullanılan bir operatördür. ?? olarak temsil edilir.

Gerçek hayatta, bir kullanıcının profilinde eksik veya tanımsız bir alanı kontrol ederken nullish operatörünü kullanabilirsiniz. Örneğin, kullanıcının profilinde bir fotoğrafı var mı yok mu kontrol etmek ve yoksa varsayılan bir fotoğraf göstermek için nullish operatörünü kullanabilirsiniz.
## Expire
Belirli bir verinin veya belgenin geçerlilik süresinin sona ermesi durumunda da "expire" ifadesi kullanılabilir. Örneğin, bir web sitesindeki oturumunuzun süresinin dolması veya bir şifrenin belirli bir süre sonra geçerliliğini yitirmesi gibi durumlarda "expire" terimi kullanılabilir.
##Body-parser
body-parser, Node.js ortamında Express gibi web uygulama çatılarıyla birlikte gelen bir middleware'dir. Bu modül, gelen isteklerin gövde verilerini ayrıştırmak ve kolayca erişilebilir hale getirmek için kullanılır.

Özellikle HTTP POST isteklerinde veya diğer istek türlerinde, isteğin gövdesinde bulunan verilere erişmek için body-parser kullanılır.
## Router.use() 
isteği karşıla
## Env.SECRET_KEY
Özellikle güvenlikle ilgili hassas bilgiler ve kod içinde doğrudan belirtilmemesi gereken veriler olduğu zaman çevresel değişkenleri kullanırız. Bu verilere sadece bunu oluşturan kişiler ulaşabilir. Ve dotenv ile oluştuduğum verileri github takip edemez. Örneğin, bir web uygulamasında kullanıcı şifrelerini veya kimlik doğrulama anahtarlarını saklamak için kullanılabilir.
## httpOnly
httpOnly, tarayıcıda bir HTTP cookie'sinin nasıl işleneceğini belirleyen bir özelliktir. Bir cookie httpOnly olarak işaretlendiğinde, tarayıcı bu cookie'yi yalnızca HTTP veya HTTPS üzerinden erişilebilecek şekilde işler.  Yani, httpOnly özelliği, cookie'nin yalnızca sunucu tarafından okunabilir ve istemci tarafı betikler tarafından erişilemez hale getirilmesini sağlar, böylece güvenlik açıklarını azaltır.
## SomeSite
"someSite" genellikle bir örnek veya soyut bir terim olarak kullanılır ve gerçek bir web sitesini işaret etmez; daha çok öğretici veya örnek materyallerde yer alan varsayımsal bir siteyi temsil eder.
## AccessToken
Bir kullanıcının kimliğini doğrulamak için bir sunucudan alınan access token, belirli bir süre boyunca geçerlidir. Bu token, sunucu tarafından belirli bir kaynağa (örneğin, bir API'ye) erişmek için kullanılır.
## RefreshToken
Access tokenın sınırlı bir geçerlilik süresi vardır ve bu süre dolduğunda erişimin yenilenmesi gerekir. Burda da refreshRoken devreye girer. Yani Access tokenın süresi doluğunda kullanılarak yeni bir accesstoken almak için kullanılır. Yani örnek vermek gerekirse, kullanıcının oturumu açıkken tekrar kimlik doğrulaması yapmasını gerektirmeden arka planda oturumu sürdürmek için kullanılır. Böylece güvenlik ve erişim kontrolü sağlanmış olur.
## İlişkisel Veri Tabanı(SQL)
İlişkisel veritabanları (SQL tabanlı veritabanlar), verileri tablolar halinde organize eden ve bu tablolar arasında ilişkiler kuran yapılarıyla bilinir. SQL (Structured Query Language) kullanılarak yönetilen bu veritabanları, tablolar arasında ilişkiler kurarak verileri depolar ve ilişkilendirir.

Gerçek hayatta bir örnek olarak, bir e-ticaret sitesini düşünelim. İlişkisel veritabanları, bu tür bir e-ticaret sitesinde ürünler, müşteriler, siparişler gibi verilerin depolanması ve bu veriler arasındaki ilişkilerin yönetilmesi için kullanılabilir.

Ancak daha ilişkisel yapılar gerektiren bankacılık, e ticaret, sağlık alanlarında sql kullanılır.
## NoSQL
ilişkisel olmayan veritabanı sistemlerini ifade eder. NoSQL veritabanları, geleneksel SQL tabanlı ilişkisel veritabanlarından farklı olarak, esneklik, ölçeklenebilirlik ve farklı veri modelleri sağlama konusunda öne çıkar.

Örneğin bigdata, iot, veya sosyal medya platformlarında NoSQL tercih edilir.
## SQL – NoSQL
NoSQL, belirli durumlarda SQL'e göre daha yüksek hızda veri işleme kapasitesine sahiptir. Esnek veri modelleri ve yatay ölçeklenebilirlik sayesinde büyük miktarda veriye hızlı bir erişim sağlar. Ayrıca, çeşitli veri tiplerini saklamak konusunda daha esnektir.

Ancak, NoSQL'in bazı dezavantajları da vardır. Örneğin, NoSQL sistemleri tutarlılık konusunda SQL veritabanları kadar sıkı değil. Ayrıca, yedekleme zamanında SQL'e göre bazı farklılıklar ve daha karmaşık yapılar ortaya çıkarabiliyor.
bir proje hızlı büyüme ve ölçeklendirme ihtiyacı duyuyorsa NoSQL, daha katı veri bütünlüğü ve sıkı ilişkisel yapılar gerekiyorsa SQL tercih edilebilir.

Örneğin bigdata, iot, veya sosyal medya platformlarında NoSQL tercih edilir.

Ancak daha ilişkisel yapılar gerektiren bankacılık, e ticaret, sağlık alanlarında sql kullanılır.
## MongoDB
NoSQL (ilişkisel olmayan) bir veritabanıdır. Genellikle büyük veri hacimlerini ve esnek veri yapılarını yönetmek için kullanılır. Örnek olarak, IoT, Web ve mobil uygulamalarını verebiliriz.
## useNewUrl, Parser useUrl, Parser useUnifiedTopology
MongoDB için yapılandırma seçeneklerini belirten parametrelerdir. MongoDB bağlantılarını yönetmek ve belirli özellikleri etkinleştirmek veya devre dışı bırakmak için kullanılır.

useNewUrlParser: MongoDB bağlantı URL'sini yeni ayrıştırıcı motorunu kullanarak çözümlemek için bir yapılandırma seçeneği.

useUrlParser: MongoDB bağlantı URL'sini standart bir URL ayrıştırıcı kullanarak çözümlemek için bir yapılandırma seçeneği.

useUnifiedTopology: MongoDB sunucularıyla yapılan bağlantılarda daha iyi bir bağlantı yönetimi için yeni ve birleştirilmiş bir topoloji motorunu etkinleştiren bir yapılandırma seçeneği.
